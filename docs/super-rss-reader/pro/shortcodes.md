---
title: Shortcode
menu_order: 2
taxonomy:
    doc_category: wordpress-plugins
---

With PRO version we can use shortcode to display RSS feed items anywhere in the website. Currently as of version v4.0 the shortcode can be built manually by following the reference below.

## Syntax

    [print_sc sc='{srr_feed parameter1="val" parameter2="val"}']

## Example

Below shortcode will generate RSS feed list for two feed URLs (MakeUseOf and NASA) in two different tabs with the titles "MakeUseOf" and "NASA" respectively with the color style "dark", author and date displayed.

    [print_sc sc='{srr_feed urls="https://feeds.feedburner.com/Makeuseof, https://www.nasa.gov/rss/dyn/breaking_news.rss" tab_titles="MakeUseOf, NASA" color_style="dark" show_author=1 show_date=1}']

## Parameter reference

The shortcode parameters supported can be also referred in `Settings` -> `Super RSS Reader - Pro` page.

|Parameter|Description|Default value|Supported values|
|--- |--- |--- |--- |
|urls|The URLs to display RSS feed for. Multiple RSS feed URLs can be separated by a new line or comma.|||
|tab_titles|The title of the tab for the respective RSS feed.|||
|count|The total number of feed items to fetch.|5||
|show_date|Display the date of the feed item.|0|0 - Hide date, 1 - Show date|
|show_desc|Display the description/excerpt of the feed item.|1|0 - Hide description, 1 - Show description|
|show_author|Display the author of the feed item.|0|0 - Hide author, 1 - Show author|
|show_thumb|Display the thumbnail of the feed item.|1|0 - Hide thumbnail, 1 - Show thumbnail|
|template|The template of the feed item.|%%title%% %%metadata%% %%thumbnail%% %%description%%||
|strip_desc|Trim the description to certain number of words.|30||
|strip_title|Trim the title text to certain number of words.|0||
|read_more|The read more text if the description is trimmed.|[...]||
|rich_desc|Display rich description with all the formatting. Note: With rich description text cannot be trimmed.|0|0 - Normal description1 - Rich description|
|add_nofollow|Add "nofollow" attribute to feed links.|1|0 - Do not add nofollow attribute, 1 - Add nofollow attribute|
|open_newtab|Open the feed links in new tab.|1|0 - Open in same tab, 1 - Open in new tab|
|thumbnail_position|The position of the thumbnail.|align_left|align_left - Align left, align_right - Align right, cover - Cover|
|thumbnail_size|The size of the thumbnail including the units. Example: 64px, 10%|64px||
|color_style|The style of the feed display.|none|none - No style, grey - Grey, dark - Dark, orange - Oranges, modern - Simple modern, twitter - Twitter, twitter_dark - Twitter (dark)card - Card, card_dark - Card (dark)|
|display_type|The type of feed display mode.|vertical_ticker|normal - Normal, vertical_ticker - Ticker, grid - Grid|
|visible_items|The number of feed items to be visible when ticker is enabled.|5||
|ticker_speed|The speed of the ticker animation in seconds. Without units.|4||
|grid_columns|The number of columns in the grid between 2 to 4.|2||

## Using the shortcode in theme templates

The shortcode can be used in PHP theme templates like below.

    <?php echo do_shortcode( '[print_sc sc='{srr_feed parameter1="val" parameter2="val"}']' ); ?>