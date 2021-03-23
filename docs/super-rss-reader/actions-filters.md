---
title: Actions and Filters
menu_order: 4
taxonomy:
    doc_category: wordpress-plugins
---

Wordpress has the feature of "hooks" with which users can add extra functionality to WordPress and its plugins and themes. Super RSS Reader has included below hooks using which you can manipulate/customize the plugin output as needed.

## Using hooks

If you use a hook to add or manipulate code, you can add your custom code in a variety of ways:

* To a custom child theme's functions.php file.
* Using a plugin such as Code Snippets.

## Filters

This type of hook allows to tap into plugin process and manipulate/tweak before it is processed. Below are the filters supported by Super RSS Reader.

### `srr_mod_item_html`

This filter allows to tweak the feed item's HTML before it is displayed. It supports 3 parameters.

#### Parameters

    apply_filters( 'srr_mod_item_html', $html, $feed_url, $feed_item );

* `$html` __(array)__ - An array which contains the elements to modify. See supported keys below.
    * `title` - The title HTML of the feed item.
    * `meta` - The metadata HTML of the feed item.
    * `thumbnail` - The thumbnail HTML of the feed item.
    * `description` - The description HTML of the feed item.
    * `before` - HTML to display before the feed item.
    * `after` - HTML to display after the feed item.
* `$feed_url` __(string)__ - The feed URL which is under process.
* `$feed_item` __(Simplepie_Item)__ - The current feed item's [Simplepie_item](http://simplepie.org/wiki/reference/simplepie_item/start) object.

#### Example

    <?php
        add_filter( 'srr_mod_item_html', 'my_srr_modifier', 10, 3 );

        function my_srr_modifier( $html, $feed_url, $feed_item ){
            // This example modifies the title tag and appends a text to it.
            $html[ 'title' ] = $html[ 'title' ] . ' extra text';
            return $html;
        }
    ?>

## Actions

Actions allows to execute function at specific point during the execution. Right now Super RSS Reader does not have any actions.