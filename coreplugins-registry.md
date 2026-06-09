# e107 core plugins — `pluginpack.xml` registry
Registry for Find Plugins (multisource). Contains the **29** upstream plugins that ship an `e107_plugins/{folder}/plugin.xml` (info is fetched from it).
- `organization="e107Inc"`, `repo="e107"`, `branch="master"` — constant for all.
- `compatibility="2.3"` = minimum e107 version (the show/hide gate), **not** the plugin version.
- `name` / `description` come from the upstream `plugin.xml` (6 descriptions were written by hand — see Note 1b below).

---

## Full corepack.xml (copy all at once)
```xml
<?xml version="1.0" encoding="utf-8"?>
<e107Release>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="_blank"
    branch="master"
    name="Blank Plugin"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>A Blank Plugin to help you get started in plugin development. More details can be added here.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="alt_auth"
    branch="master"
    name="Alternate Authentication"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin allows for alternate authentication methods.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="banner"
    branch="master"
    name="Banners"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Add advertising banners to your e107 website</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="chatbox_menu"
    branch="master"
    name="Chatbox"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Chatbox Menu</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="contact"
    branch="master"
    name="Contact"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>A contact form for your e107 website.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="download"
    branch="master"
    name="Downloads"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin is a fully featured file download system</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="faqs"
    branch="master"
    name="FAQs"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>A simple plugin to add Frequently Asked Questions to your website.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="featurebox"
    branch="master"
    name="Featurebox"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Displays an animated area on the top of your page with news-items and other content you would like to feature.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="forum"
    branch="master"
    name="Forum"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin is a fully featured forum system</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="gallery"
    branch="master"
    name="Gallery"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>A simple image gallery</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="gsitemap"
    branch="master"
    name="Google Sitemap"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Generates a Google Sitemap</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="hero"
    branch="master"
    name="Hero"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Image and text slider, animated bullet points for the hero area of your home page.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="import"
    branch="master"
    name="Import into e107"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Import data from Wordpress, Joomla, Drupal, Blogpost, RSS and other formats.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="linkwords"
    branch="master"
    name="Linkwords"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin will link specified words with a defined link and/or tooltip.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="list_new"
    branch="master"
    name="List Latest"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin allows you to view a list and/or menu of recent additions in all e107 categories. You can either view the list with data since your last visit, or view a general latest additions list.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="navigation"
    branch="master"
    name="Navigation"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Sitelinks-based navigation menus for your e107 website.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="news"
    branch="master"
    name="News"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>The e107 news content system.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="newsfeed"
    branch="master"
    name="Newsfeeds"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin will retrieve rss feeds from other websites and display them according to your preferences.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="newsletter"
    branch="master"
    name="Newsletter"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Provides a quick and easy way to configure and send newsletters.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="page"
    branch="master"
    name="Pages"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Create and manage custom pages and page menus.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="pm"
    branch="master"
    name="Private Messenger"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin is a fully featured Private Messaging system.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="poll"
    branch="master"
    name="Poll"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>The poll plugin allows you to define polls in either a menu or forum post.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="rss_menu"
    branch="master"
    name="RSS"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>RSS Feeds from your site.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="signin"
    branch="master"
    name="Signin"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>A sign-in / login menu for your e107 website.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="siteinfo"
    branch="master"
    name="Siteinfo"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Displays site information and statistics in a menu.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="social"
    branch="master"
    name="Social"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Adds options to replace the e107 comment engine with Facebook. Add Twitter feeds to your site. etc.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="tagcloud"
    branch="master"
    name="Tag Cloud"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Add a Tag Cloud to your site.</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="tinymce4"
    branch="master"
    name="TinyMce4"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>TinyMce4 CDN version</description>
  </plugin>

  <plugin
    organization="e107Inc"
    repo="e107"
    folder="user"
    branch="master"
    name="User"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Theme and Language Menus</description>
  </plugin>


</e107Release>
```

---

## Individual plugin entries (copy one at a time)

### Blank Plugin — `_blank`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="_blank"
    branch="master"
    name="Blank Plugin"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>A Blank Plugin to help you get started in plugin development. More details can be added here.</description>
  </plugin>
```

### Alternate Authentication — `alt_auth`
> not in protected core (`$_core_plugins`) → shows as `external` in the badge
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="alt_auth"
    branch="master"
    name="Alternate Authentication"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin allows for alternate authentication methods.</description>
  </plugin>
```

### Banners — `banner`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="banner"
    branch="master"
    name="Banners"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Add advertising banners to your e107 website</description>
  </plugin>
```

### Chatbox — `chatbox_menu`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="chatbox_menu"
    branch="master"
    name="Chatbox"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Chatbox Menu</description>
  </plugin>
```

### Contact — `contact`
> description written by hand (upstream `plugin.xml` has none)
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="contact"
    branch="master"
    name="Contact"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>A contact form for your e107 website.</description>
  </plugin>
```

### Downloads — `download`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="download"
    branch="master"
    name="Downloads"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin is a fully featured file download system</description>
  </plugin>
```

### FAQs — `faqs`
> not in protected core (`$_core_plugins`) → shows as `external` in the badge
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="faqs"
    branch="master"
    name="FAQs"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>A simple plugin to add Frequently Asked Questions to your website.</description>
  </plugin>
```

### Featurebox — `featurebox`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="featurebox"
    branch="master"
    name="Featurebox"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Displays an animated area on the top of your page with news-items and other content you would like to feature.</description>
  </plugin>
```

### Forum — `forum`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="forum"
    branch="master"
    name="Forum"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin is a fully featured forum system</description>
  </plugin>
```

### Gallery — `gallery`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="gallery"
    branch="master"
    name="Gallery"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>A simple image gallery</description>
  </plugin>
```

### Google Sitemap — `gsitemap`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="gsitemap"
    branch="master"
    name="Google Sitemap"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Generates a Google Sitemap</description>
  </plugin>
```

### Hero — `hero`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="hero"
    branch="master"
    name="Hero"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Image and text slider, animated bullet points for the hero area of your home page.</description>
  </plugin>
```

### Import into e107 — `import`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="import"
    branch="master"
    name="Import into e107"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Import data from Wordpress, Joomla, Drupal, Blogpost, RSS and other formats.</description>
  </plugin>
```

### Linkwords — `linkwords`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="linkwords"
    branch="master"
    name="Linkwords"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin will link specified words with a defined link and/or tooltip.</description>
  </plugin>
```

### List Latest — `list_new`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="list_new"
    branch="master"
    name="List Latest"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin allows you to view a list and/or menu of recent additions in all e107 categories. You can either view the list with data since your last visit, or view a general latest additions list.</description>
  </plugin>
```

### Navigation — `navigation`
> not in protected core (`$_core_plugins`) → shows as `external` in the badge; description written by hand (upstream `plugin.xml` has none)
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="navigation"
    branch="master"
    name="Navigation"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Sitelinks-based navigation menus for your e107 website.</description>
  </plugin>
```

### News — `news`
> description written by hand (upstream `plugin.xml` has none)
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="news"
    branch="master"
    name="News"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>The e107 news content system.</description>
  </plugin>
```

### Newsfeeds — `newsfeed`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="newsfeed"
    branch="master"
    name="Newsfeeds"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin will retrieve rss feeds from other websites and display them according to your preferences.</description>
  </plugin>
```

### Newsletter — `newsletter`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="newsletter"
    branch="master"
    name="Newsletter"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Provides a quick and easy way to configure and send newsletters.</description>
  </plugin>
```

### Pages — `page`
> description written by hand (upstream `plugin.xml` has none)
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="page"
    branch="master"
    name="Pages"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Create and manage custom pages and page menus.</description>
  </plugin>
```

### Private Messenger — `pm`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="pm"
    branch="master"
    name="Private Messenger"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>This plugin is a fully featured Private Messaging system.</description>
  </plugin>
```

### Poll — `poll`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="poll"
    branch="master"
    name="Poll"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>The poll plugin allows you to define polls in either a menu or forum post.</description>
  </plugin>
```

### RSS — `rss_menu`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="rss_menu"
    branch="master"
    name="RSS"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>RSS Feeds from your site.</description>
  </plugin>
```

### Signin — `signin`
> not in protected core (`$_core_plugins`) → shows as `external` in the badge; description written by hand (upstream `plugin.xml` has none)
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="signin"
    branch="master"
    name="Signin"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>A sign-in / login menu for your e107 website.</description>
  </plugin>
```

### Siteinfo — `siteinfo`
> description written by hand (upstream `plugin.xml` has none)
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="siteinfo"
    branch="master"
    name="Siteinfo"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Displays site information and statistics in a menu.</description>
  </plugin>
```

### Social — `social`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="social"
    branch="master"
    name="Social"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Adds options to replace the e107 comment engine with Facebook. Add Twitter feeds to your site. etc.</description>
  </plugin>
```

### Tag Cloud — `tagcloud`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="tagcloud"
    branch="master"
    name="Tag Cloud"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Add a Tag Cloud to your site.</description>
  </plugin>
```

### TinyMce4 — `tinymce4`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="tinymce4"
    branch="master"
    name="TinyMce4"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>TinyMce4 CDN version</description>
  </plugin>
```

### User — `user`
```xml
  <plugin
    organization="e107Inc"
    repo="e107"
    folder="user"
    branch="master"
    name="User"
    compatibility="2.3"
    infourl="https://github.com/e107Inc/e107"
  >
    <description>Theme and Language Menus</description>
  </plugin>
```

---

## Note 1 — 7 core plugins WITHOUT `plugin.xml`
These are in `$_core_plugins` but have no `plugin.xml` (legacy menu plugins). The marketplace cannot fetch their `name`/`version`/`description`, so they are **not** in the registry. They can be added once upstream ships a `plugin.xml` for them (this is what the Feature Request targets).
- `admin_menu` — Admin Menu
- `blogcalendar_menu` — Blog Calendar Menu
- `comment_menu` — Comment Menu
- `login_menu` — Login Menu
- `newforumposts_main` — New Forum Posts
- `online` — Online Users Menu
- `search_menu` — Search Menu

## Note 1b — 6 hand-written descriptions
Upstream `plugin.xml` has no `<description>` for these; the text in the registry was authored manually — review and adjust as needed:
- `contact`
- `navigation`
- `news`
- `page`
- `signin`
- `siteinfo`

## Note 2 — 4 registry plugins that are NOT protected core
These ship a `plugin.xml` and are in the 29, but are **not** listed in `$_core_plugins`. In the type badge they therefore appear as **`external`** (not `core`), even though they are by e107inc and bundled with e107.
- `alt_auth`
- `faqs`
- `navigation`
- `signin`
