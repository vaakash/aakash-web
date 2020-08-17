---
title: Shortcode parameters
menu_order: 2
taxonomy:
    doc_category: wordpress-plugins
---

With shortcode parameters certain dynamic values can be added to the shortcode content. There are 5 different types of shortcode parameters.

Note: WordPress information and Date parameters types will be affected if any caching plugin is used to cache the page. These two types will best work if no caching is enabled on the posts/pages.

### WordPress information

This shortcode parameter type allows to insert popular WordPress information in shortcode content. One item from the list is `$$post_modified_date$$` which gets replaced with the modified date of the post where the shortcode is inserted. The complete list of these parameters can be seen in shortcode edit/create page under Insert shortcode parameters --> WordPress Information button.

### Date parameters

This shortcode parameter type allows to insert dates in shortcode content. One item from the list is `$$year$$` which gets replaced with the live current year. The complete list of these parameters can be seen in shortcode edit/create page under Insert shortcode parameters --> Date parameters button.

### Shortcode enclosed content

With this shortcode parameter, the content which is enclosed within the shortcode can be replaced inside the shortcode content. Example: If a shortcode `[sc name="my_shortcode"]My enclosed content[/sc]` is used and then `$$enclosed_content$$` parameter used in shortcode content will be replaced with "My enclosed content"

### Custom parameters

Please refer [this page](./custom-parameters) for more info and examples on custom parameters.

### Custom fields

With this shortcode parameter, the custom field value will be replaced. Example: If the parameter is `$$custom_field:color$$`, then this parameter will be replaced with the post's custom field value of of name "color".