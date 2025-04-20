---
title: Changelog
menu_order: 10
taxonomy:
    doc_category: wordpress-plugins
---

### 5.3
* New: Option to choose between media sizes from the feed.
* PRO: Keyword editor missing nonce.
* PRO: Keyword editor crashing on certain themes.

### 5.2
* Fix: Order whole RSS feed by date.
* Fix: Handle `null` returns.
* PRO: Pull description from the source URL for Google news and Google alerts.

### 5.1
* Fix: Restrict admin ajax calls with nonce.
* Fix: Enhancements to pick thumbnail from srcsets and skip remote relative thumbnails.
* Fix: Comment user avatar is added to comments RSS feed.

### 5.0
* New: Option to show/hide feed item title.
* New: Option to link description text with the feed item URL.
* New: Option to offset/skip RSS feed items.
* New: Option to set different width and height for the thumbnail.
* Fix: PHP 8 warnings.
* Fix: Additional ellipsis are now stripped from the description text.
* PRO: Support for 6 grid columns.
* PRO: Google news and Google alerts RSS feeds will now fetch thumbnail image.

### 4.9
* New in PRO: Paginated display type.
* New in PRO: Wildcard value is now supported as filter value.
* New: Option to set fixed height for the feed with scrollbar.
* New: RSS feeds are now fetched with Chrome user agent.
* Fix: `<b>` tag is now included in the rich text description.

### 4.8
* New in PRO: Merge multiple RSS feeds into one.
* New: Color theme (Modern 2).
* Fix: Padding issue in one column layout.

### 4.7.1
* Fix: Template field was stripping away some characters.

### 4.7
* New: Support for lazy loading is enabled for thumbnails.
* New: WordPress requirement is updated.
* Fix: Enhancements to widget form and feed output sanitization.

### 4.6
* New in PRO: Option to fetch thumbnail directly from the feed URL if not available.
* New: Option to choose timezone for the date of feed items.
* New: Error logging system in the PRO version.
* Fix: Set default link URL when feed item has no link.
* Fix: Break tags are retained in the feed description.

### 4.5
* New: Display feed item date in relative format.
* Fix: Minor enhancements to widget admin UI.
* New in PRO: Filter by category.
* Fix in PRO: Feed items count was incorrect when filter was applied.

### 4.4.1
* Fix: All feed items were displayed when "Order by" is selected as "default"

### 4.4
* New in PRO: Filter feed items by keyword.
* New: Option to prefer full content or summary to display as feed description.
* New: Default ordering option.
* New: Option to change no feed item text.
* Fix: Bug with select field in widget form.
* Fix: Read more link being displayed when description is empty.

### 4.3
* New: Option to order/sort feed items by date, random.
* New: Filter hook to customize thumbnail URL.

### 4.2
* Fix: Ticker sometimes gets stuck when browser tab is switched or not viewed.
* New: Featured image is automatically inserted into local RSS feed to show as thumbnail if the post has no image in it.

### 4.1
* New: Option to change date format
* New: Date will now be in the same language as the site.
* New: Option to set default thumbnail image if not present.
* New: Filter hook to customize the feed item's HTML.

### 4.0.1
* Fix: Added hover style for the tabs and on active style when no theme is selected.
* New: Tested with WordPress 5.6

### 4.0

* New: Reliable thumbnails. Thumbnails will now be taken from multiple places like feed content.
* New: Thumbnail positions (align left, right and cover mode) and size can be changed.
* New: Widget options are now more refined, easy to find and use.
* New: Plugin is now translation ready.
* New: `noreferrer` added to the feed links.
* New: Stripe of feed items is now done using CSS class `srr-stripe` instead of `even`.
* New in PRO: Shortcodes
* New in PRO: 4+ Color themes
* New in PRO: Grid layout
* New in PRO: Custom template for the feed content.