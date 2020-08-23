---
title: Advanced post navigator
taxonomy:
    doc_category: wordpress-plugins
---

## Installation

- Buy and download the plugin at Codecanyon
- You will get a zipped file named _advanced-post-navigator.zip_
- In your WordPress administration page, Go to Plugins -> Add New
- Click the "Upload" tab at the top of the page.
- Select the _advanced-post-navigator.zip_ file in the upload form and select "Install Now"
- Activate the plugin.

## Administration Page

- After activation, the plugin's configuration is accessible under Settings -> Advanced Post Navigator
- The plugin settings can configured separately under each tab.

## FAQs

(Some basic questions are answered below, for more questions you can browse the [Support forum](/forum/))

### Q: When the arrow is hovered, the bubble is not shown or it is misaligned.

A: This can be due to some Javascript problems in the page.

- The plugin is tested in various environments and it doesn't have any bug in the JS file. It works 100%.
- The not working of the plugin will be due to some other external JS files included in the page. Some other JS files collide with the plugin's source leading to errors.

This error can be corrected easily. For assistance in clearing this kind of issues please post it in the [Support forum](/forum/).

### Q: How to change the tag for the "Heading" in the bubble content.

A: By default H3 tag is used for heading. It is found optimum in most of the tested themes, hence it is used as default. Currently, there is no options provided to change that within the admin page. The forth coming versions will definitely have that feature.

### Q: The bubble content is not looking good and not uniform.

A: This issue happens because of the theme's default styling rules. Various actions are taken in the plugin to normalize the theme's default styling behavior. This problem can be rectified by adding certain CSS rules. Please use the support forum for getting immediate fixtures.

### Q: How to remove the default Next and Prev links present on the page ?

A: It varies from theme to theme.

- The default 'Twentytwelve" theme uses `wp_link_pages` function for adding the next and previous links. To remove it open the _themes/twentytwelve/content.php_ and delete the line number **39**.
- Some themes use the `next_posts_link` and `previous_posts_link` functions to add the links.
- Please use the support forum for step by step details on removing the links.

For more questions, please use the free [support forum](/forum/) to get immediate action on your issue. You can use screenshots, console texts in the forum for detailed explanation.