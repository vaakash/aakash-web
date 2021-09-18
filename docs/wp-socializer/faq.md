---
title: FAQ
menu_order: 1
taxonomy:
    doc_category: wordpress-plugins
---

### Can I insert share icons anywhere in a custom location ?

Yes, you can use Shortcodes. WP Socializer has shortcodes for share icons, profile icons and for share links. Using those shortcodes you can add social sharing features anywhere in your site.

### Is this plugin GDPR complaint ?

Yes, WP Socializer does not collect any personal information of you or your visitors. If you have any concerns please do let me know.

### Does the plugin slow down my website ?

No. WP socializer is a lite an fast plugin. It is a bloat free, no-nonsense plugin compared to others in the WordPress market. Except font icons, no external resources are loaded. Also the JS are loaded dynamically only when needed. Since all the resources are loaded locally, if you have a minify plugin you can merge JS/CSS files with other resources of your theme.

### Can I change the icon for the share icons ?

Yes. You can click the "cog" icon after the icon is added to open the Advanced settings. In the advanced settings form enter the URL of the image or the fontawesome icon name under the "custom icon" field.

### How to add custom icon ?

You can add custom icon in the [PRO version](/wordpress-plugins/wp-socializer/) of the plugin easily.

### Can I add twitter timeline/tweets to the sidebar ?

Yes, the plugin has out of the box widgets for Facebook, Twitter and social profile links. You can use them and add those widgets to the sidebar.

### Is it possible to automatically hide share icons in small screens upon resize ?

Yes. WP Socializer uses JS to detect the screen size so you can resize the window to see how responsive the icons are on desktop and mobile devices.

### How to change the image shown in social network websites ?

Social networks fetch the image from something called "open graph tags" - You can set those information for every page like image, title etc. Please find this page on [more info](https://www.wpbeginner.com/wp-themes/how-to-add-facebook-open-graph-meta-data-in-wordpress-themes/).

### How to change/hide the "Share & Enjoy" text ?

Under "Share icons" -> Miscellaneous tab you can change the text for the field "Heading text". It supports HTML.

### Some icons are not displayed correctly and a empty square is seen

This happens when the font icon used by the theme and the plugin are of different fontawesome icon versions (v4 and v5). You can try going to WP Socializer --> Settings --> Font icon and select a different font icon version (or) you can disable font icon being loaded completely by `fa_icons` to "CSS/JS to not to load in any page". Please raise a support topic if issue still exists.

### Share icons are not displayed in the page !

Share icons or other feature may be hidden if the option "Hide in all pages" option is selected in "Conditions to display" section. Please select "Show in all pages" option to display the buttons. If the buttons are still not displayed, please raise an issue in the Support forum.

### How to disable a feature in specific page alone ?

WP Socializer has a feature called "conditional display" where a feature can be made to shown only at desired places by creating rules. Please look for the section "Conditions to display the template" under every feature page to add rules as per the requirement.

### How to disable/hide share icons in all pages ?

Please select "Hide in all pages" option under "conditions to display the template" section in all the templates to hide them being displayed. For other features like floating sharebar, follow bar, text sharebar and mobile sharebar can be hidden by "disabling" them from the top most section available at their respective pages.

### Can I add custom HTML between share icons ?

Yes, you can use the "Custom HTML" icon for this. Insert the icon and paste the HTML. You can also use `{url}` and `{title}` placeholders in the HTML for the share URL and title respectively.

### Facebook share count is not working.

Please ensure Facebook APP ID and app secret is configured. Also, Facebook has recently made a change to the API to return only like/share count more than 100. See [comment from Facebook support](https://developers.facebook.com/support/bugs/318897266426699/?comment_id=319463206370105) team here.

### How to center the share icons ?

Under "Share icons" -> Miscellaneous tab you can find the option to "center the icons".

### How to set Twitter username in the tweet link ?

Under WP Socializer -> Settings page you can change the "Twitter username".

### How to change the text of the tweet ?

You can change the sharing text, title, excerpt and tweet text in the [PRO version](/wordpress-plugins/wp-socializer/) of the plugin.

### How to track shares with Google Analytics & Google Tag Manager ?

In the [PRO version](/wordpress-plugins/wp-socializer/) of the plugin, you can enable Google Analytics feature. Once enabled, shares will be tracked in Google Analytics.