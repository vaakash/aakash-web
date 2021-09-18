---
title: Shortcodes
menu_order: 3
taxonomy:
    doc_category: wordpress-plugins
---

WP Socializer supports Shortcodes for below features. With this you can insert them in any location where shortcode will work.

- Share icons
- Follow icons
- Share links

### Share icons

With this shortcode, you can insert "Share icons". The syntax of the shortcode is below,

    [print_sc sc='{wpsr_share_icons parameter1="value" parameter2="value" ...}']

__Example:__

    [print_sc sc='{wpsr_share_icons icons="facebook,twitter,pinterest,email" icon_size="40px" icon_bg_color="red" icon_shape="drop"}']

__Parameter reference:__

The latest list of supported parameters for this shortcode are listed in the WP Socializer administration page in _WP Socializer_ → _Shortcodes_ → _Share icons_ tab.

### Follow icons

With this shortcode, you can insert "Follow icons". The syntax of the shortcode is below,

    [print_sc sc='{wpsr_follow_icons parameter1="value" parameter2="value" ...}']

__Example:__

    [print_sc sc='{wpsr_follow_icons facebook="https://facebook.com/aakashweb" twitter="https://twitter.com/aakashweb" instagram="https://instagram.com/aakashweb" bg_color="green" shape="circle"}']

__Parameter reference:__

The latest list of supported parameters for this shortcode are listed in the WP Socializer administration page in _WP Socializer_ → _Shortcodes_ → _Follow icons_ tab.

### Share link

With this shortcode, you can insert "Share links". Using this shortcode you can create a link that can share the current page on social media website. The syntax of the shortcode is below,

    [print_sc sc='{wpsr_share_link parameter1="value" parameter2="value" ...}']

__Example:__

    [print_sc sc='{wpsr_share_link for="twitter"}Tweet about this page{/wpsr_share_link}']

__Parameter reference:__

The latest list of supported parameters for this shortcode are listed in the WP Socializer administration page in _WP Socializer_ → _Shortcodes_ → _Share link_ tab.

### Haven't got the plugin yet ?

If you haven't downloaded the plugin yet, please visit the plugin homepage to purchase and download the plugin using the link below.

[Get WP Socializer](/wordpress-plugins/wp-socializer/) {.button}