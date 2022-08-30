---
title: Actions and Filters
menu_order: 4
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
* `$feed_item` __(SimplePie_Item)__ - The current feed item's [SimplePie_item](http://simplepie.org/wiki/reference/simplepie_item/start) object.

#### Example

    <?php
        add_filter( 'srr_mod_item_html', 'my_srr_modifier', 10, 3 );

        // This example modifies the title tag and appends a text to it.

        function my_srr_modifier( $html, $feed_url, $feed_item ){
            $html[ 'title' ] = $html[ 'title' ] . ' extra text';
            return $html;
        }
    ?>

### `srr_mod_thumbnail_url`

This filter allows to change the feed item's thumbnail URL.

#### Parameters

    apply_filters( 'srr_mod_thumbnail_url', $thumbnail_url, $item, $feed, $default_url );

* `$thumbnail_url` __(string)__ - The thumbnail URL retrieved from the feed.
* `$item` __(SimplePie_Item)__ - The current feed item's [SimplePie_item](http://simplepie.org/wiki/reference/simplepie_item/start) object.
* `$feed` __(SimplePie)__ - The feed's [SimplePie](http://simplepie.org/api/class-SimplePie.html) object.
* `$default_url` __(string)__ - The default thumbnail URL as mentioned in settings.

#### Example

    <?php
        add_filter( 'srr_mod_thumbnail_url', 'srr_change_thumbnail_url', 10, 4 );

        // This example sets the feed's top level image as the thumbnail for all items. If not present then sets the default thumbnail URL.

        function srr_change_thumbnail_url( $thumbnail_url, $item, $feed, $default_url ){
            $feed_level_image = $feed->get_image_url();
            if( !empty( $feed_level_image ) ){
                return $feed_level_image;
            }else{
                return $default_url;
            }
        }
    ?>

## Actions

Actions allows to execute function at specific point during the execution. Right now Super RSS Reader does not have any actions.