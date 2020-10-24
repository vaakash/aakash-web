---
title: FAQ
menu_order: 5
taxonomy:
    doc_category: wordpress-plugins
---

__Note:__ Super RSS Reader PRO is a standalone plugin and it includes more features than the Super RSS Reader free version. The documentation of the free version still applies to it. Below FAQ is specific to the PRO version features. You can find the FAQ of the free version [here](../faq.md)

### Q: Is Super RSS reader PRO is a feed aggregation plugin ?

A: No, super RSS Reader is not a feed aggregation plugin i.e it won't create new posts. It will display the RSS feed in widgets and in posts using shortcodes.

### Q: How many columns are supported in the grid layout ?

The plugin supports 2, 3 and 4 columns in the grid layout.

### Q: Is it possible to have columns more than 5 in the grid layout ?

Right now the plugin supports only 4 columns considering the reason that beyond 4 columns the content is too small for any width.

### Q: Is it possible to use ticker along with grid layout ?

Grid layout is another option to the display type. Hence only one display type can be selected and we cannot add vertical ticker to the grid layout.

### Q: Can I add custom CSS styling to the grid layout ?

Yes, absolutely ! Please refer the [custom styling](./grid-display.md) to refer the CSS classes specific to grid. You can also refer the [FAQ](../faq.md) for the complete list of CSS classes supported.

### Q: Will the grid layout shrink in mobile/smaller screens ?

Yes. Grid layout reduce in columns in smaller screens gradually ending up with single column in the smallest screen size.

### Q: Are there any special themes for the grid layout ?

All the color themes support grid layout and they are optimized for it.

### Q: How to use the Shortcode in theme files ?

The shortcode can be used in theme template using the `do_shortcode` function. Please refer more details on it [here](https://developer.wordpress.org/reference/functions/do_shortcode/)

### Q: How to insert the shortcode in the classic/block editor ?

Currently there is no toolbar icon or block which you can click to insert the shortcode. The shortcode is self served. The shortcode and it's parameters can be referred from the Settings -> Super RSS Reader - PRO page and it can be inserted in the posts (in classic editor) or in the shortcode block (in block editor) or in any location which supports execution of shortcode.

### Q: Can I customize the template when using shortcode ?

Yes, the `template` parameter can be used to customize the template of the feed item. Please make sure to use single quote `'` inside the template tag instead of double quote to avoid the clash with the shortcode attribute's double quote itself.

__Note:__ There is a known issue when shortcode is used in the block editor's "shortcode block." and when HTML is used in the `template` attribute of the shortcode. In this case, unbalanced paragraph tags are added causing some inconsistencies to the output. To avoid this, the shortcode can be inserted in the classic editor block.

### Q: The default color themes does not suit my website, can I customize the colors ?

Yes ! The default color themes available out of the box are carefully designed in such a way considering the diverse nature of themes available. If you do not like any theme, you can consider the color theme as a template and customize the colors as you like using the [CSS classes](../faq.md).