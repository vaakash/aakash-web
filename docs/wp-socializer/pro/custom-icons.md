---
title: Custom icons
menu_order: 2
taxonomy:
    doc_category: wordpress-plugins
---

_With WP Socializer - PRO version you can create custom icons. These custom icons can be added to all the features of WP Socializer i.e share icons, floating sharebar, follow icons, text sharebar and shortcodes._

This feature enable you to create your own icon which is not available with WP Socializer by default. These custom icons can have it's own color and icon image. Once created you can pick this custom icon add it to any WP Socializer feature.

This is really helpful if you have a social network profile for which WP Socializer does not have an icon for. You can create your icon, and add it to the follow icons bar. You can also use it as a share button if the social network website supports a URL where links can be shared.

![WP Socializer - Custom icons](/_images/wpsrp-custom-icon.png) {.wp-post-image}

## Creating/editing custom icons

To add custom icons download and [install WP Socializer - PRO](./installation.md) WordPress plugin on your website.

![WP Socializer - Add custom icon to share icons and follow icons](/_images/wpsrp-add-custom-icon.png)

1. Go to _WP Socializer_ → _Settings_.
2. Under _Share icons settings_ section, click _Add custom icon_.
3. In the _Add new icon_ popup, enter the following information for the custom icon.
    - _ID_ - The ID of the custom icon
    - _Name_ - The name of the custom icon
    - _Color_ - The color of the custom icon
    - _Title_ - The title of the custom icon when the icon is hovered upon.
    - _Share link_ - The share link of the custom icon. You can use below placeholders in the URL as needed by the social network website. __Example:__ `https://example.com/share?u={url}&t={title}`. When visitors click the current page URL will be shared with that link. You can also have a link without any placeholder but this custom icon will be useful only in follow icons where you will provide the URL of the social network profile.
        - `{url}` - The URL of the current page
        - `{title}` - The title of the current page
        - `{excerpt}` - The excerpt of the current post
        - `{short-url}` - The short URL of the current post
    - _Icon_ - The icon for the custom icon. It can be an URL to an image (any image including `svg`) or a name of a fontawesome icon. There are 2 different sizes can be selected for the icon as mentioned below,
        - _Fit inside_ - With this, the image will be inside the icon.
        - _Full icon_ - With this, the full image will be used as the icon.
4. Click __Add icon__ to add the icon to the custom icons list.
5. Click __Save settings__ at the bottom of the page to save the settings.
6. Now you can open any WP Socializer feature [Share icons](../share-icons.md), [Floating sharebar](../floating-sharebar.md), [Follow icons](../follow-icons.md), [Text sharebar](../text-sharebar.md), [Shortcodes](../shortcodes.md) and add the custom icons created.

To edit a custom icon, click _Edit_ next to the custom icon name to open the editing form. To delete a custom icon, click _Delete_ next to the custom icon name.

## Haven't got the plugin yet ?

If you haven't downloaded the plugin yet, please visit the plugin homepage to purchase and download the plugin using the link below.

[Get PRO version](/wordpress-plugins/wp-socializer/) {.button}