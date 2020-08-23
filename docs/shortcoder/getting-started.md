---
title: Getting started
menu_order: 1
taxonomy:
    doc_category: wordpress-plugins
---

## Syntax of shortcodes created by shortcoder

Shortcodes created by shortcoder follow the standard WordPress shortcode syntax. They have the name `sc` and a `name` attribute. The `name` attribute is used to identify the shortcode content to execute.

If custom parameter placeholders are used in shortcode content, then the custom parameters can be used as attributes for the shortcode to replace the placeholder with the value in the content as provided in the shortcode.

    [print_sc sc='{sc name="your-shortcode-name" param1="value" param2="value"}']

## Installation

1. You can install the plugin via WordPress administration page or by uploading the `shortcoder` folder to `wp-content/plugins/` directory
2. Navigate to WordPress plugin administration page and activate the plugin.
3. Shortcoder will be activated and the shortcoder administration page link will be on the left navigation bar below "Comments" page.

## Creating and using shortcodes

1. To create or edit shortcodes, navigate to shortcoder administration page which can be seen on the main left navigation menu.
2. In the shortcode create/edit page, enter the desired name of the shortcode. This is used to identify the shortcode and it is the one provided as value for the shortcode `name` attribute. Allowed characters are alphabets, numbers, hyphens and underscores.
3. Enter the content of the shortcode in the content box. Please see below note for the shortcode content.
4. In "shortcode settings" panel you can configure various shortcode settings.
5. You can finally create/edit the shortcode by clicking "Publish" on the top right side panel.
6. This shortcode can now be used in posts/pages/widgets or places where shortcode can be executed like `[print_sc sc='{sc name="your-shortcode-name"}' ]`
7. While editing posts/pages the "Insert shortcode" toolbar icon can be seen in the classic editor and shortcoder block in Gutenberg editor to select and insert shortcode within the post editing page itself.

### Note:

Shortcode content can be HTML/CSS/JavaScript. Please make sure the HTML/CSS/JavaScript used as shortcode content is valid. The shortcode content will be used as is and is not modified when it is executed. For any issues with the shortcode content, please try the shortcode content in an isolated environment and verify if the script works as expected. This exact behavior should be seen when the used as shortcode content. If there is any issue noticed because of shortcoder, please do report the issue in the [forum](/forum/discuss/wordpress-plugins/shortcoder/).

[sc name="donateForm" title="Donation for Shortcoder plugin"]