---
title: Custom feed item template
menu_order: 4
taxonomy:
    doc_category: wordpress-plugins
---

The PRO version of the plugin includes the "custom template" feature with which the feed item template can be customized. With this the order of the feed item content like item title, date, author, description and thumbnail order can be changed.

Custom template field also supports HTML with which the placeholders can be wrapped in custom HTML tag to enable custom styling as required.

This option can found in the widget under the `General` tab -> `Feed item template`

## Placeholders

Every feed item content has a placeholder tag which are be used to design the template.

1. `%%title%%` - Title of the feed item
1. `%%thumbnail%%` - Thumbnail of the feed item
1. `%%metadata%%` - Metadata of the feed item like item date and author.
1. `%%description%%` - Description of the feed item

## Example

Below example value will position the thumbnail above the feed title, the feed title is wrapped inside heading tag and the metadata below the description.

```
%%thumbnail%%
<h3>%%title%%</h3>
%%description%%
%%metadata%%
```

## Using in shortcode

Feed item template can be changed in shortcodes too. The above mentioned example can be used in shortcode like below.

    [print_sc sc='{srr_feed urls="https://feeds.feedburner.com/Makeuseof" show_author=1 show_date=1 template="%%thumbnail%% <h3>%%title%%</h3> %%description%% %%metadata%%" thumbnail_position="cover" thumbnail_size="150px" display_type="normal"}']

Above shortcode will give a beautiful output like below.

![Super RSS Reader - PRO custom template example](https://i.snipboard.io/8ybHPp.jpg)