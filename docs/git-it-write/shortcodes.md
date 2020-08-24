---
title: Shortcodes
menu_order: 3
taxonomy:
    doc_category: wordpress-plugins
---

## Edit link shortcode

Git it write plugin has a shortcode `[print_sc sc="{giw_edit_link}"]` to add "Edit this page" to your posts. This will add a link to the markdown file in the Github repository allowing users to fork and contribute to the repository.

This shortcode can be added in plugin repository settings page under "post content template"

## Supported attributes

* `post_id` - The ID of the post to display edit link for. Default: Current post.
* `text` - The link text. Default: "Edit this page"
* `icon` - The icon to display inside link. Default: A fontawesome icon `<i class="fas fa-pen"></i> &nbsp; `
* `auto_p` - To wrap the link inside paragraph tag. Default: `false`

## Using in themes

The shortcode can be used in theme directly using the `do_shortcode` function `echo do_shortcode( '[print_sc sc="{giw_edit_link}"]' );`