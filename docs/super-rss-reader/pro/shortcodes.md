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

| Parameter | Description | Default value | Supported values |
|---|---|---|---|
| urls | The URLs to display RSS feed for. Multiple RSS feed URLs can be separated by a new line or comma. |
| tab_titles | The title of the tab for the respective RSS feed. |
| count | The total number of feed items to fetch. | 5 |
| show_title | Display the title of the feed item. | 1 | 0 - Hide title, 1 - Show title |
| show_date | Display the date of the feed item. | 0 | 0 - Hide date, 1 - Show date |
| show_desc | Display the description/excerpt of the feed item. | 1 | 0 - Hide description, 1 - Show description |
| show_author | Display the author of the feed item. | 0 | 0 - Hide author, 1 - Show author |
| show_thumb | Display the thumbnail of the feed item. | 1 | 0 - Hide thumbnail, 1 - Show thumbnail |
| merge_feeds | Merge multiple feeds into one | 0 | 0 - Do not merge feeds, 1 - Merge feeds |
| show_source | Show item source name | hidden | hidden - Hidden, above_title - Above title, next_date - Next to date, below_desc - Below description |
| template | The template of the feed item. | %%title%% %%metadata%% %%thumbnail%% %%description%% |
| strip_desc | Trim the description to certain number of words. | 30 |
| strip_title | Trim the title text to certain number of words. | 0 |
| offset | The number of RSS feed items to skip from the top. | 0 |
| date_format | The format of the feed item date. | j F Y |
| date_timezone | The timezone of the feed item date. | UTC |
| order_by | The order of the feed | default | default - Default, date - Date, date_reverse - Date reverse, random - Random |
| read_more | The read more text if the description is trimmed. | [...] |
| rich_desc | Display rich description with all the formatting. Note: With rich description text cannot be trimmed. | 0 | 0 - Normal description, 1 - Rich description |
| desc_type | Type of description to prefer | summary | summary - Summary, full_content - Full content |
| link_desc | Link description text with the feed item URL | 0 | 0 - No link, 1 - Link description |
| add_nofollow | Add "nofollow" attribute to feed links. | 1 | 0 - Do not add nofollow attribute, 1 - Add nofollow attribute |
| open_newtab | Open the feed links in new tab. | 1 | 0 - Open in same tab, 1 - Open in new tab |
| thumbnail_position | The position of the thumbnail. | align_left | align_left - Align left, align_right - Align right, cover - Cover |
| thumbnail_size | The size of the thumbnail including the units. Example: 64px, 10% | 64px |
| thumbnail_force | Pick the thumbnail from page (feed URL) directly | no | no - No, when_absent - When absent in feed item, always - Always |
| thumbnail_default | The URL of the default thumbnail image if not present. Leave empty to not display any thumbnail. |
| no_feed_text | Text to display when there are no feed items | No items |
| filter_type | Type of keyword filtering for the RSS feed items | no_filter | no_filter - No filtering, show - Show items based on filter, hide - Hide items based on filter |
| filter_name | The name of the filter created | |
| color_style | The style of the feed display. | none | none - No style, grey - Grey, dark - Dark, orange - Oranges, modern - Modern 1, modern2 - Modern 2, twitter - Twitter, twitter_dark - Twitter (dark), card - Card, card_dark - Card (dark) |
| display_type | The type of feed display mode. | vertical_ticker | normal - Normal, vertical_ticker - Ticker, grid - Grid, paginated - Paginated |
| visible_items | The number of feed items to be visible when ticker is enabled. | 5 |
| ticker_speed | The speed of the ticker animation in seconds. Without units. | 4 |
| page_size | The number of items in a page. | 5 |
| page_bar | The elements of the page bar | all | all - Both number and navigation, page_num_only - Page numbers only, navigation_only - Navigation only
| grid_columns | The number of columns in the grid between 2 to 4. | 2 |

## Using the shortcode in theme templates

The shortcode can be used in PHP theme templates like below.

    <?php echo do_shortcode( '[print_sc sc='{srr_feed parameter1="val" parameter2="val"}']' ); ?>