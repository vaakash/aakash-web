---
title: Extra Code
menu_order: 5
taxonomy:
    doc_category: wordpress-plugins
---

With the "extra code" feature you can set additional HTML/JS/CSS code for a shortcode. This extra code will be inserted at the bottom of the page when that shortcode is used on the page anywhere at least once.

If the shortcode is not used then it the extra code won't be inserted. Also, the extra code will be inserted only once on page even when the shortcode is used multiple times on the page.

This is really useful when you want javascript libraries to load on the page only when the shortcode content is inserted on the page somewhere. Example: A Google maps embed code will requires Google API libraries to be loaded. You can load the Google API libraries only when the Google maps shortcode is inserted in the page.

You can set any code JavaScript/CSS/HTML as a part of the extra code. It will be inserted to the bottom of the page as is.

## Setting extra code

The extra code option is available in the shortcode editing page under the "Shortcode settings" metabox.

![Setting extra code in Shortcoder PRO](/_images/scp-extra-code.png)

## FAQ

### Is it possible to insert extra code at the top of the page i.e inside `</head>` tag?

No, it is not possible to do that. Extra code will be inserted only at the bottom of the page. Since shortcodes can be inserted at any place in a page, it is not possible to insert extra code ahead at the top of the page.
