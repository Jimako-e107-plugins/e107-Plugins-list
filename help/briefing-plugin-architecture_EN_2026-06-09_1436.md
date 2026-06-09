# Briefing: plugin group architecture — base plugin + dependent feature plugins (e107)

**Generated:** 2026-06-09 14:36
**Type:** architecture (universal pattern, no concrete names)

> A pattern for any group of related plugins in e107. Names are generic:
> `base` = the shared base plugin, `feature` = the individual functional plugins.

---

## Principle

One domain = **one base plugin (`base`) + N feature plugins** that depend on it.
Reason for the split: e107 grants **admin permissions, dashboard entries and menu
entries PER PLUGIN** — so separate plugins give **granular admin roles** (an admin can
be granted access to a single feature only) and **per-feature visibility** of what is
done and what is not.

`base` holds the **shared code, config and common assets** so they are not
duplicated; feature plugins **reuse** them rather than copy them. This avoids the
duplication that otherwise makes a multi-plugin setup hard to maintain.

## Structure & dependencies

- `base` is installed **first**.
- Each `feature` declares a `<dependencies>` requirement on `base` in its
  `plugin.xml` (e107 then enforces install order).
- All tables of the group get a **consistent app prefix** (distinct from e107 core
  and from any other system in the same database) to avoid collisions.
- Features consume shared code via `require_once(e_PLUGIN.'base/includes/...')` or the
  e107 autoloader — **never by duplication**.

## What goes where

| Item | Where | Why |
|------|-------|-----|
| Global config / prefs | **base** | one place; features read via `e107::getPlugConfig('base')` |
| Shared model / handler classes, DB access / mapping layer | **base** | the anti-duplication core; features reuse |
| Shared / lookup (codelist) tables | **base** (`plugin.xml`) | belong to the whole group; base installs first |
| Feature-specific tables | **feature** (`plugin.xml`) | owned by the feature |
| Admin UI + admin **permission** | **feature** | e107 grants permissions per plugin → granular roles (the reason for splitting) |
| Dashboard widget / menu entry | **feature** | e107 handles these per plugin |
| **e_url (SEF routes)** | **feature** | per-plugin in e107; `e107::url('feature', …)`; independent routes, more flexibility |
| Feature frontend pages | **feature** | owned by the feature |
| Shared LAN constants | **base** | cross-cutting labels; features load them in addition |
| Feature LAN constants | **feature** | own labels; feature loads base LAN + its own |
| Shared templates (cards / grid / forms) | **base** | reuse across features |
| Feature templates / overrides | **feature** | specific; may extend base templates |
| Shared CSS / JS | **base** | reuse |
| Global admin settings | **base** (own permission, e.g. super-admin only) | separate from feature permissions |

## Decision principle

> Put it in a **FEATURE** when e107 keys it per-plugin (admin permissions, e_url
> routes, dashboard, menu) **or** when it is feature-specific.
> Put it in **BASE** when it is genuinely shared and duplication would hurt (models
> and mapping layer, config, shared LAN, shared templates, lookup tables).

## Notes on selected points

**SQL / schema.** Do not put "everything in base". Split by ownership: shared and
lookup tables in `base`, feature-specific tables in the feature. What clearly belongs
in `base` is the **shared DB access / mapping layer** (one class, one place for
parameterization and security) — not necessarily all tables.

**e_url.** Per feature. `e_url.php` is loaded per plugin and `e107::url()` is keyed by
the plugin folder, so each feature gets its own independent route namespace with full
control (its own `regex`/`sef`/`redirect`). A single base e_url would only couple the
features and remove flexibility.

**Translations (LAN).** Per plugin. Shared constants in `base`, feature constants in
the feature; each feature loads **both** — base LAN and its own
(`e107::plugLan('base')` + `e107::plugLan('feature')`). Split by ownership.

## Skeleton (typical files)

`base` plugin:

```
base/
├── plugin.xml              # manifest; shared/lookup tables; shared prefs; installed first
├── includes/               # shared classes: base model, DB access/mapping layer, shared logic
├── languages/              # shared LAN (English.php = admin, English_front.php = front)
├── templates/              # shared templates (cards, grid, forms) reused by features
├── admin_config.php        # OPTIONAL: global settings page (own permission, e.g. super-admin)
└── (css/js)                # shared assets
# e_url.php is usually NOT here — routes live per feature
```

`feature` plugin:

```
feature/
├── plugin.xml              # manifest; <dependencies> on base; feature tables; own admin permission;
│                           #   dashboard/menu registration
├── admin_config.php        # feature admin UI (e_admin_ui) — its OWN permission (granular roles)
├── e_url.php               # feature SEF routes (canonical eUrlConfig: regex/sef/redirect/legacy)
├── *_menu.php              # menu(s) the feature exposes on the front end (if any)
├── feature.php             # feature front-end page(s)
├── includes/               # feature-specific handlers (using/extending base classes)
├── languages/              # feature LAN (loads base LAN + its own)
├── templates/              # feature templates (may extend the base templates)
└── (css/js)                # feature-specific assets
```

## Security (applies across the group)

- All queries parameterized via the e107 db class; input through `$tp->toDB()`, output
  through `$tp->toHTML()`. The shared mapping layer in `base` is the central place for
  SQL-injection protection.
- File uploads through e107 media/upload handlers (validate MIME + extension), never
  raw `move_uploaded_file`.
- Table app prefix distinct from e107 core and any other system sharing the database.
