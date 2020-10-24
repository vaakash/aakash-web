---
title: FAQ
menu_order: 3
taxonomy:
    doc_category: wordpress-plugins
---

### Q: RSS feed is not refreshing

A: Super RSS Reader uses WordPress's default feed reading module. By default WordPress caches the RSS feed for 12 hours. You can change this default value by adding the below code to your theme's function.php file.

    add_filter( 'wp_feed_cache_transient_lifetime', function($a) { return 600; } );

Here 600 indicates 10 minutes in seconds. Please note that setting lower value will increase the load on the server to refresh the RSS cache. You can also refer [this post](https://wordpress.org/support/topic/rss-not-updating-no-matter-which-plugin-i-try/#post-10123881) to change the refresh time for particular feed URL.

Also, please ensure WordPress cache plugins (like W3 total cache, Super cache etc.) are configured to not cache the page where this widget is active or increase the expiry of the cache so that old cached page is not served to the users.

### Q: RSS feed is not displayed or error is shown

A: This can happen when,

- The RSS feed URL is invalid.
- The feed URL is not accessible by the server.
- The feed content is not in the expected format or corrupt. Please use a [feed validation service](https://validator.w3.org/feed/) to validate the feed.

### Q: Thumbnail is not displayed or incorrect image is picked ?

A: Thumbnails will be displayed in the feed item if the feed item has it. Below is the order in which the thumbnail image will be searched.

1. From the feed item's `<enclosure>` tag -> thumbnail URL.
1. From the feed item's `<enclosure>` tag -> URL.
1. The first image from the feed item's content.
1. From the feed item's `<image>` tag if present.

Please ensure if your feed has an image in any of the above available format.

### Q: How to make custom CSS styling to the feed like changing colors, width etc. ?

A: You can use below CSS classes to control and make custom styling as needed.

1. `super-rss-reader-widget` - to select the feed displayed in the widget.
1. `srr-main` - to select the feed wrapper element.
1. `srr-tab-wrap` - the tab wrapper class.
1. `srr-wrap` - the wrapper class of the feed.
1. `srr-item` - to select the feed items.
1. `srr-title` - to select the feed title.
1. `srr-meta` - to select the data, author wrapper element.
1. `srr-thumb` - to select the thumbnail wrapper element.
1. `srr-summary` - to select the feed description.
1. `srr-read-more` - to select the "read more" link.
1. `srr-stripe` - to select the alternate feed item.
1. `srr-style-<color_theme>` - to select make changes for one particular color theme.

### Q: What are the contents shown in the feed ?

A: By default content like title, date, author, description, thumbnail can toggled to show in the feed.

### Q: Can I change the order of the content shown in the feed ?

A: Yes, it is possible with the [PRO version](/wordpress-plugins/super-rss-reader-pro/?utm_source=docs&utm_medium=faq&utm_campaign=srr-pro) of the plugin. In the free version we can toggle the content.

### Q: Will the additional ticker effect slow down the site ?

The additional effect needs only 2.5 KB of additional JavaScript file which is very small since it is minified and optimized already.

### Q: How to display the feeds in multiple tabs ?

A: Enter the RSS feed URLs separated by comma or in new line in the widget, the plugin automatically renders the tab.

### Q: Is it possible to display the RSS feed items in a Grid format ?

A: Yes, it is possible with the [PRO version](/wordpress-plugins/super-rss-reader-pro/?utm_source=docs&utm_medium=faq&utm_campaign=srr-pro) of the plugin. In the free version the supported display types are Normal and Ticker.

### Q: Does this plugin support horizontal ticker ?

A: No, Super RSS Reader only supports vertical support feature for now.
