---
title: Shortcodes
menu_order: 5
taxonomy:
    doc_category: wordpress-plugins
---

WordPress shortcodes give the ability to insert certain feature anywhere in your website. Announcer - PRO plugin supports shortcodes which you can use to place the announcement anywhere as needed.

By default the announcement can be added to the top/bottom of the window using the settings page.

In case you want to insert the same announcement inside a post/page then you can copy the shortcode and paste the shortcode wherever needed.

![Announcer - PRO announcement inserted inside a post using shortcode](/_images/ancrp-shortcode-2.png) {.wp-post-image}

**Note:**

* When using shortcodes the properties of the announcement cannot be modified or new announcement cannot be created. The announcement shortcode is used to insert an already created announcement using the admin page anywhere.

* When you want to use an announcement only using shortcode, then you can set **Location rules** > **Hide in all pages**. Now you can use the shortcode anywhere as needed without it being automatically displayed.

## Syntax

The syntax of the announcer is as follows.

    [print_sc sc='{announcer id="<announcement_id>"}']

The shortcode only accepts the `id` as a parameter where the ID of the announcement should be passed.

You can pass this shortcode to the WordPress function `do_shortcode` in case you want to insert it directly in the theme template file.

## Copying the shortcode from the admin page

The shortcode can be found in two locations in the admin page.

1. Announcement editing page on the right side sidebar

![Announcer - PRO shortcode admin page](/_images/ancrp-shortcode.png)

2. In the announcement list page under the "Shortcode" column for easy copy pasting.

## Special CSS class

The announcement has a special CSS class name assigned when inserted using shortcode. The class name is `ancr-shortcode`.

You can use this to apply custom styling, padding, margin using CSS as needed.

### Haven't got the plugin yet ?

If you haven't downloaded the plugin yet, please visit the plugin homepage to purchase and download the plugin using the link below.

[Get PRO version](https://www.aakashweb.com/wordpress-plugins/announcer-pro/?utm_source=doc&utm_medium=shortcodes&utm_campaign=ancr-pro#purchase) {.button}