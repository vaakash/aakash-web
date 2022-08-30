---
title: Actions and Filters
menu_order: 6
taxonomy:
    doc_category: wordpress-plugins
---

WordPress has the feature of "hooks" with which users can add extra functionality to WordPress and its plugins and themes. Super RSS Reader has included below hooks using which you can manipulate/customize the plugin output as needed.

## Using hooks

If you use a hook to add or manipulate code, you can add your custom code in a variety of ways:

* To a custom child theme's functions.php file.
* [Using a plugin such as Code Snippets](https://www.aakashweb.com/articles/best-methods-to-insert-custom-php-code-in-wordpress/).

## Filters

This type of hook allows to tap into the plugin process and manipulate/tweak before it is processed. Below are the filters supported by Super RSS Reader.

### sc_mod_shortcode

Change the shortcode properties before it is processed.

#### Parameters

    apply_filters( 'sc_mod_shortcode', $shortcode, $atts, $enclosed_content );

* `$shortcode` __(array)__ - An array/string which contains the shortcode properties. This may contain string if the shortcode is invalid. This is the value which is modified using the filter. Return this variable after processing.
    * `id` - The post ID of the shortcode.
    * `name` - The name of the shortcode.
    * `content` - The raw shortcode content.
    * `settings` - The shortcode settings array.
* `$atts` __(array)__ - An array of parameters passed to the shortcode.
* `$enclosed_content` __(string)__ - The content which is enclosed within the shortcode.

#### Example

    <?php
        add_filter( 'sc_mod_shortcode', 'my_sc_change_properties', 10, 3 );

        // This example appends a text to the shortcode content.

        function my_sc_change_properties( $shortcode, $atts, $enclosed_content ){
            if( !is_array( $shortcode ) ){
                return $shortcode;
            }

            $shortcode['content'] = $shortcode['content'] . ' APPENDING TEXT';
            return $shortcode;

        }
    ?>

### sc_mod_output

Change the shortcode content before it is inserted on the page

#### Parameters

    apply_filters( 'sc_mod_output', $content, $atts, $sc_settings, $enclosed_content );

* `$content` __(string)__ - The processed shortcode content. This is the variable which is filtered. Return this after processing.
* `$atts` __(array)__ - An array of parameters passed to the shortcode.
* `$sc_settings` __(array)__ - An array of shortcode settings.
* `$enclosed_content` __(string)__ - The content which is enclosed within the shortcode.

#### Example

    <?php
        add_filter( 'sc_mod_output', 'my_sc_change_content', 10, 3 );

        // This example wraps the shortcode with the style tag.

        function my_sc_change_content( $content, $atts, $sc_settings, $enclosed_content ){
            $content = '<style>' . $content . '</style>';
            return $content;
        }
    ?>

### sc_mod_wp_params

Add/modify the "Insert shortcode parameters" menu which is used to insert [Shortcode parameters](https://www.aakashweb.com/docs/shortcoder/shortcode-parameters/) to the shortcode content.

#### Parameters

    apply_filters( 'sc_mod_wp_params', $parameters_list );

* `$parameters_list` __(array)__ - An array of shortcode parameters and its friendly name. Refer `wp_params_list()` in `shortcoder.php` for detailed array properties information.

#### Example

Please see this [example code](https://gist.github.com/vaakash/f4891252f698a62bb0dc21d040853e7e) which adds WooCommerce shortcode parameters using this filter.

### sc_mod_metadata

Set/modify the values of the [Shortcode parameters](https://www.aakashweb.com/docs/shortcoder/shortcode-parameters/)

#### Parameters

    apply_filters( 'sc_mod_metadata', $metadata );

* `$metadata` __(array)__ - An array of shortcode parameters as key with it's content to replace as value. Use this to set value for the new shortcode parameters introduced using `sc_mod_wp_params`. This can also be used to tweak the parameter values if needed.

### Example

Please see this [example code](https://gist.github.com/vaakash/f4891252f698a62bb0dc21d040853e7e) which adds WooCommerce shortcode parameters using this filter.

## Actions

This type of hook allows to execute custom function when a certain event is hit.

### sc_do_before

This action is triggered before the shortcode is processed (i.e replacement of parameters, custom fields etc.). You can use this to activate/deactivate other WordPress hooks before the shortcode content is processed.

#### Parameters

    do_action( 'sc_do_before', $shortcode, $atts );

* `$shortcode` __(array)__ - An array/string which contains the shortcode properties. This may contain string if the shortcode is invalid. This is the value which is modified using the filter. Return this variable after processing.
    * `id` - The post ID of the shortcode.
    * `name` - The name of the shortcode.
    * `content` - The raw shortcode content.
    * `settings` - The shortcode settings array.
* `$atts` __(array)__ - An array of parameters passed to the shortcode.

#### Example

    <?php
        function my_sc_do_before( $shortcode, $atts ){
            // something to do before shortcode execution.
        }
        add_action( 'sc_do_before', 'my_sc_do_before', 10, 2 );
    ?>

### sc_do_after

This action is triggered after the shortcode is processed (i.e replacement of parameters, custom fields etc.). You can use this to activate/deactivate other WordPress hooks after the shortcode content is processed.

#### Parameters

    do_action( 'sc_do_after', $shortcode, $atts );

* `$shortcode` __(array)__ - An array/string which contains the shortcode properties. This may contain string if the shortcode is invalid. This is the value which is modified using the filter. Return this variable after processing.
    * `id` - The post ID of the shortcode.
    * `name` - The name of the shortcode.
    * `content` - The raw shortcode content.
    * `settings` - The shortcode settings array.
* `$atts` __(array)__ - An array of parameters passed to the shortcode.

#### Example

    <?php
        function my_sc_do_after( $shortcode, $atts ){
            // something to do after shortcode execution.
        }
        add_action( 'sc_do_after', 'my_sc_do_after', 10, 2 );
    ?>
