---
title: URL Metadata
menu_order: 8
taxonomy:
    doc_category: wordpress-plugins
---

When an RSS feed does not have thumbnail image, then Super RSS Reader - PRO can fetch the thumbnail directly from the feed URL page.

## Using the feature

You can select the feature from both widget and from shortcode. To select in the widget, switch to the `Content` tab and scroll down to the `Thumbnail` section. Select the desired option for this feature for the field `Fetch thumbnail from page directly`

Similarly, you can use the shortcode parameter `thumbnail_force` and set values `no`, `when_absent` and `always` as needed.

Below are the options and how they function,

- `No` - Disables the feature.
- `When absent in feed item` - The thumbnail is fetched from the feed URL page only when the feed item does not have an image as [searched in the mentioned order](/docs/super-rss-reader/faq/#q-thumbnail-is-not-displayed-or-incorrect-image-is-picked).
- `Always` - Always fetches the thumbnail from the feed URL even though the feed item has the URL

## Requirements

- CURL must be enabled on the server
- The feed item URL must accessible directly i.e it must not blocked by cloudflare or other firewall services.
- The feed item URL must contain `og:image` meta property.

## How does it work?

The plugin uses CURL to crawl the page and looks for the `og:image` meta property. No other image is picked from the page.

### Caching

- Once the thumbnail URL is fetched from the page, it is cached for `7 days` in the database.
- When there is any error crawling the page, the next attempt is made after `1 day`.

### Note

- When the feature is enabled for the first time, then it may take some time to fetch the image for all the feed items. Once it is cached, crawling won't happen and results come from the cached result.
- When the crawled feed item URL does not have any thumbnail, then the default thumbnail will be taken if provided.

## Debugging

In case the thumbnails are not displayed even after enabling the feature, then you can enable debugging logs.

- Go to Settings > Super RSS Reader - Pro > Debugging logs
- Click "Enable debugging"
- Now refresh the page where the RSS feed is inserted.
- Go to Settings > Super RSS Reader - Pro > Debugging logs. You can see the crawling result for every URL. Below are the meaning for the status codes,
    - `0` - Unable to open the feed URL. It is incorrect/invalid/not accessible by your server
    - `404` - Feed URL is not found
    - `403` - Feed URL access is forbidden for your server. It may be behind cloudflare or other firewall service. You can request the feed owner to whitelist your server IP.
    - `50x` - Some server error on the feed URL side.
- Click "Disable debugging" to stop logging.

### Note:

Do no forget to disable debugging after collecting the necessary information because when debugging is enabled, crawling results are not cached.