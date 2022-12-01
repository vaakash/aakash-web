---
title: Merge RSS feeds
menu_order: 8
taxonomy:
    doc_category: wordpress-plugins
---

With Super RSS Reader PRO, you can merge and display multiple RSS feeds as one. You can enter multiple RSS feed URLs in the URL field and select the "Merge RSS feeds into one" option.

### Demo video

<iframe width="560" height="315" src="https://www.youtube.com/embed/sbtIn3qkWYU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Shortcode option

If you are displaying RSS feed using Shortcode, then you can provide multiple RSS feed URLs to the `urls` parameter and set the parameter `merge_feeds` to `1`. You can show the RSS feed source name using the `show_source` option.

You can find all the supported option for [shortcode documentation page](./shortcodes.md).

    [print_sc sc='{srr_feed urls="https://feeds.feedburner.com/Makeuseof, https://www.nasa.gov/rss/dyn/breaking_news.rss" merge_feeds="1" show_source="above_title"}']