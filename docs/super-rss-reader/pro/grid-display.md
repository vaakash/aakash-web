---
title: Grid display
menu_order: 3
taxonomy:
    doc_category: wordpress-plugins
---

Grid display is one the display type available in the PRO version of the Super RSS Reader plugin. With grid display type you can display the feed items in multiple columns. The feed items can be displayed in 2 to 4 columns based on the setting.

This grid display type works well when the feed is displayed in wider content areas like posts/pages using shortcode. In this display type more feed item can be displayed in one row which expands the use case of how RSS feed like displaying the recent posts of your blog below posts/pages or displaying the top comments on your blog using the feed URL.

![Super RSS reader PRO - Grid display of feed items](/_images/srrp-doc-grid.png)

### Note:

- Grid display works well in wider content areas. On smaller content areas like widget the grid will be cramped since the sidebar is usually small. It is better to use this display type in wider areas.

- Since grid is one of the option along with vertical ticker. So if grid is selected then ticker cannot be enabled.

## Enabling Grid display type

### In Widget

The grid display type can be selected in the widget under the `Display` tab -> `Display type` -> `Grid`

### Using shortcode

The parameter `display_type` hsa to be set to the value `grid`. Example `[print_sc sc='{srr_feed display_type="grid"}']`

## Custom styling

When grid display type is enabled there are specific CSS class added to the feed which can be used to customize the feed display as needed.

1. `srr-grid` - To the feed wrap element
1. `srr-g-col-2/3/4/5/6` - To the feed wrap element depending on the number of columns chosen. Example `srr-g-col-3`.
1. `srr-last-row-item` - To the last feed item in the row.

### Alternating colors

With grid display type the feed items are striped alternatively both row and column wise depending on the color theme selected. Some color themes do not stripe the alternating colors.

In case you want to select and customize the striped item you can use the CSS class `.srr-stripe` to style on your own.

