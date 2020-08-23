---
title: FAQ
menu_order: 2
taxonomy:
    doc_category: wordpress-plugins
---

### Q: RSS feed is not refreshing

A: Super RSS Reader uses WordPress's default feed reading module. By default WordPress caches the RSS feed for 12 hours. You can change this default value by adding the below code to your theme's function.php file.

    add_filter( 'wp_feed_cache_transient_lifetime', create_function('$a', 'return 600;') );

Here 600 indicates 10 minutes in seconds. Please note that setting lower value will increase the load on the server to refresh the RSS cache. You can also refer [this post](https://wordpress.org/support/topic/rss-not-updating-no-matter-which-plugin-i-try/#post-10123881) to change the refresh time for particular feed URL.

### Q: How can I customize the RSS widget externally ?

A: You can use the `super-rss-reader-widget` class in your stylesheet to control the widget styling. Other classes are,

1. `srr-tab-wrap` - the tab's class.
2. `srr-wrap` - the wrapper of the widget.
3. `srr-item.odd` - to control the odd feed items.
4. `srr-item.even` - to control the even feed items.

### Q: Does this plugin support horizontal ticker ?

A: No, Super RSS Reader only supports vertical support feature for now.

### Q: What fields are shown in the feed output by default ?

A: By default the plugin shows fields like title, author, description, thumbnail. Other fields are not supported currently.

### Q: Will the additional ticker effect slows the site ?

A: No. the additional effect needs only 3.4 Kb of additional file. I think that's not too heavy to slow down the site.

### Q: How to create a tabbed mode ?

A: Just enter the RSS feed URLs separated by comma in the widget, the plugin automatically renders the tab.

[sc name="donateForm" title="Donation for Super RSS Reader plugin"]