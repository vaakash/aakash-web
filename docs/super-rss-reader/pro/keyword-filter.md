---
title: Filter by Keyword
menu_order: 7
taxonomy:
    doc_category: wordpress-plugins
---

With the "Keyword filtering" feature you can show or hide feed items based on feed URL, title and description. You can build rules and every feed items will be filtered based on those rules.

This is useful if you want to display only specific feed items on your website. This feature is available for both Widget and for Shortcodes.

## Filtering in Widget

To configure filters in widget, please find the steps below.

1. Navigate to `Widgets` page and add/edit Super RSS Reader widget to your sidebar.
2. Select the `Super RSS Reader` -> `Filter` tab.
3. Select the type of filtering to happen under "Filter type" field.
    - `No filtering` - No filters are applies
    - `Show items based on filter` - Only feed items which match the rules are displayed.
    - `Hide items based on filter` - Only feed items which does not match the rules are displayed.
4. Click `View/edit filter rules` to open the rules editor. See below for more information on building rules.

## Filtering in Shortcode

To apply filters in Shortcode, the rules must be created first. To create rules, please follow the steps below.

You can create multiple keyword filtering rules to use in shortcodes.

1. Go to `Settings` -> `Super RSS Reader - PRO`.
2. Click `Generate keyword filters`
3. Under the `Keyword filters` section, add a new keyword filter.
4. Enter a name for the filter rules for identification. This name is used in the Shortcode.
5. Click `Edit filter` to open the rules editor. See below for more information on building rules.

### Setting the filter rules to a Shortcode

After creating filter rules they can be applied to a shortcode using the below shortcode parameters.

- `filter_type` - The type of filtering to happen
- `filter_name` - The name of the keyword filter which was created in previous section.

#### Example

    [print_sc sc='{srr_feed urls="https://feeds.feedburner.com/Makeuseof" filter_type="show", filter_name="onlyandroid"}']

Here "onlyandroid" is the name of the keyword filter created. It has rules to filter feed items.

## Building keyword filter rules.

The keyword filter rules are built/edited in the "Keyword filter" popup editor.

![Super RSS reader PRO - Keyword filter editor](/_images/srrp-doc-keyword-filter-editor.png)

In this editor, 

- Click `Add rule` to add different rules
- Click `and` to add more conditions to the rule(s)
- Click `-` to delete a rule.

A rule contains 3 fields.

1. Type of rule - Feed title, description, item URL, feed URL. This decides the feed item property where the keywords will be searched.
2. Operator - contains/does not contain.
3. Keyword - Enter the keyword you want to search separated by comma. The keywords are case insensitive.

Click `Save filter` to save the rules which are built.

In the above screenshot, there are two rules created. Feed items will be show/hidden if any one of them is met.

1. Rule 1 - If the feed items has the description `offers` and the feed URL contains the words `xbox` or `playstation`
2. Rule 2 - If the feed title contains the word `deals`

The type of filtering to happen i.e show/hide is decided on the Widget's `Filter type` settings or `filter_type` parameter in case of Shortcodes.