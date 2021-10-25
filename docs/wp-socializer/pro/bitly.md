---
title: Bit.ly
menu_order: 4
taxonomy:
    doc_category: wordpress-plugins
---

_WP Socializer - PRO has integration with bit.ly URL shortening service. With this feature enabled you can share links shortened with bit.ly_

![WP Socializer - Bit.ly](/_images/wpsrp-bitly.png) {.wp-post-image}

### Requirements

- Bit.ly account

## Configuring Bit.ly

To add custom icons download and [install WP Socializer - PRO](./installation.md) WordPress plugin on your website.

1. Go to _WP Socializer_ → _Bit.ly integration_
2. Under _Enable/disable Bit.ly integration_ click the toggle to enable the feature.
3. Under _Settings_ section, configure below settings
    - _Access token_ - Your Bit.ly account's access token. You can get the access token from Bitly settings page under [API section](https://app.bitly.com/settings/api/)
    - _Group ID_ - The group ID under which the URLs have to be shortened. This is optional if you have only one Bit.ly group. To find your group ID, go to Bit.ly [account settings](https://app.bitly.com/settings/profile/) click _Groups_ under _Account settings_. Click the group you want, copy the group ID from the address bar like this `https://app.bitly.com/settings/organization/<ORG_ID>/groups/<GROUP_ID>/`
    - _Shorten links of_ - Select the pages for which Bit.ly shortening has to happen. By default all the pages except taxonomy archive pages are shortened.

### Note:

- Bit.ly is used as a replacement for the default WordPress short URL. If you want to share only with bit.ly URL then you can enable the option _Use Short URL to share this post instead of full URL_ under _WP Socializer_ in post edit page for specific post as required.

- Bit.ly has rate limit of 10 URL shortens per minute and 1000 URL shortens per hour. WP Socializer will shorten the URL when the page is loaded by any user. It will be save to the post once generated. So once URL is shortened there is no issue. If rate limit has been reached, then WP Socializer will show the normal short URL meantime for 1 hour. After 1 hour the bit.ly call will be attempted again to shorten the URL.