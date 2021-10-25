---
title: Share Icons
menu_order: 3
taxonomy:
    doc_category: wordpress-plugins
---

_With Share icons feature, you can add share icons at the top and bottom of the posts. Visitors can click the share icons and share the page on the respective social media website/app._

WP Socializer supports all the popular social media services. You can find the complete list in the [plugin homepage](/wordpress-plugins/wp-socializer/).

![WP Socializer - Social media share icons plugin - Share icons](https://ps.w.org/wp-socializer/assets/screenshot-2.png?rev=2343242) {.wp-post-image}

## Adding share icons

To insert share icons to your posts, [install WP Socializer](./installation.md) WordPress plugin on your website.

1. Go to _WP Socializer_ → _Share icons_
2. Under _Enable/disable share icons_ click the toggle to enable the feature.
3. Share icons can be configured for 2 different templates. You can click _Template 1/2_ and make the following configurations
4. Under _Choose the share icons_ click _Add social icon_
5. Select the share icon you would like to add.
6. Click __Save settings__ at the bottom of the page to save the settings.
7. Share icons will now be added to the bottom of posts and pages.

## Changing individual icon settings

![Adding share icons using WP Socializer](/_images/wpsr-doc-share-icons-choose.png)

- _Share icons_ feature settings page, under _Choose the share icons_ section you can change advanced settings for individual icon.
- Click and drag the icons to change the order the icons.
- Click the _cog_ icon to open the icon's advanced settings. In the icon advanced settings you can change,
    1. Text to show next to the icon.
    2. Text to show on hovering the icon.
    3. Custom image for the icon. With an image URL (including `svg`) starting with `http` or a fontawesome icon name.
- Click the _x_ icons to delete the icon.

## Customizing the look of share icons

WP Socializer provides a variety of options to customize the share icons on your website. You can customize it as you like to match with your theme.

![Customizing share icons in WP Socializer](/_images/wpsr-doc-share-icons-customization.png)

Under _Customization_ section you can change the icon's
1. Layout (normal or full width)
2. Size
3. Shape
4. Icon color
5. Icon background color
6. Hover effect
7. Space between the icons
8. Heading to show above the icons (Under _Miscellaneous_ tab)
9. Center the icons (Under _Miscellaneous_ tab)
10. Custom HTML before/after the icons (Under _Miscellaneous_ tab)
11. Share counter settings (Under _Share counter_ tab)
12. Position of the share icons (Above/below the post, under _Position_ tab)

Under _Responsiveness_ section you can change how the share icons should behave on the wider screen (desktop) and on a smaller/narrower screen (mobile). You can change below options like below.
- On desktop → _Show/Hide_ icons.
- On mobile → _Show/Hide_ icons.
- Change the width with which the screen should be considered desktop or mobile.

## More options

### Configuring to show/hide on specific pages

You can configure share icons to shown on specific posts/pages under the _Conditions to display the template_ section. This can be configured for all the WP Socializer features. Please see the [conditional display](./location-rules.md) page for more information on this.

### Support for Shortcodes

Share icons feature of WP Socializer support shortcodes. You can find more information about it in the [shortcodes documentation page](./shortcodes.md).

## FAQ

<div class="accordion" markdown="1">

### Share icons are not displayed in the page !

Share icons or other feature may be hidden if the option "Hide in all pages" option is selected in "Conditions to display" section. Please select "Show in all pages" option to display the buttons. If the buttons are still not displayed, please raise an issue in the Support forum.

### Can I change the icon for the share icons ?

Yes. You can click the "cog" icon after the icon is added to open the Advanced settings. In the advanced settings form enter the URL of the image or the fontawesome icon name under the "custom icon" field.

### Is it possible to automatically hide share icons in small screens upon resize ?

Yes. WP Socializer uses JS to detect the screen size so you can resize the window to see how responsive the icons are on desktop and mobile devices.

### How to change/hide the "Share & Enjoy" text ?

Under "Share icons" -> Miscellaneous tab you can change the text for the field "Heading text". It supports HTML.

### Can I add custom HTML between share icons ?

Yes, you can use the "Custom HTML" icon for this. Insert the icon and paste the HTML. You can also use `{url}` and `{title}` placeholders in the HTML for the share URL and title respectively.

### How to center the share icons ?

Under "Share icons" -> Miscellaneous tab you can find the option to "center the icons".

### How to set Twitter username in the tweet link ?

Under WP Socializer -> Settings page you can change the "Twitter username".

### How to change the text of the tweet ?

You can change the sharing text, title, excerpt and tweet text in the [PRO version](/wordpress-plugins/wp-socializer/) of the plugin.

### How to track shares with Google Analytics & Google Tag Manager ?

In the [PRO version](/wordpress-plugins/wp-socializer/) of the plugin, you can enable Google Analytics feature. Once enabled, shares will be tracked in Google Analytics.

</div>

## Haven't got the plugin yet ?

If you haven't downloaded the plugin yet, please visit the plugin homepage to purchase and download the plugin using the link below.

[Get WP Socializer](/wordpress-plugins/wp-socializer/) {.button}