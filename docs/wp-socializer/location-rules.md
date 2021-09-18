---
title: Location rules
menu_order: 3
taxonomy:
    doc_category: wordpress-plugins
---

WP Socializer provides location rules feature with which you can create custom rules to conditionally display features like Share icons, Floating sharebar, follow icons and text sharebar.

![Location rule settings in WP Socializer WordPress plugin](/_images/wpsr-doc-location-rules.png) {.wp-post-image}

Before rules can be built there are below options which decides how the rules should act.

* _Show in all pages_ - Displays unconditionally everywhere in the site. No rules can be created.
* _Hide in all pages_ - Hides unconditionally everywhere in the site. No rules can be created.
* _Show in selected pages_ - Displays only in the pages which meet the rules. Rules have to be created.
* _Hide in selected pages_ - Hides only in the pages which meet the rules. Rules have to be created.

You can create rules with conditions for the following pages,

* `Single post` - To display in posts or specific posts by ID.
* `Page` - To display in pages or specific pages by ID.
* `Home page` - To display in home page.
* `Front page` - To display in front page.
* `Sticky posts` - To display in sticky posts.
* `Post type` - To display in specific post types.
* `Post format` - To display in posts of specific post format(s).
* `Archive pages` - To display in archive pages like category, tags, date, month.
* `Category archive page` - To display in archive page of specific post category.
* `Tag archive page` - To display in archive page of specific post tag(s).
* `Taxonomy archive page` - To display in any custom taxonomy archive page.
* `Date archive page` - To display in date archive page.
* `404 page` - To display in 404 page.
* `Categories of post` - To display in posts of specific post category.
* `Tags of post` - To display in posts of specific post tags.
* `Terms of post` - To display in posts of specific terms of the custom taxonomy.

Every rule has an operator `is/is not` which can be used to negate the rule itself.

For example, a rule like `Single post` - `is not` - `1234` under "show in selected pages" will show the feature in all the posts except post with ID `1234`.

For every rule, multiple sub rule can be added to further narrow down. For example, a rule like `Single post` - `is` - `<blank>` with sub rules like `Categories of post` - `is` - `blog` and `Tags of post` - `is` - `announcement` under "Show in selected pages" will display only in "posts" of "blog" category with the tag "announcement".

### Haven't got the plugin yet ?

If you haven't downloaded the plugin yet, please visit the plugin homepage to purchase and download the plugin using the link below.

[Get WP Socializer](/wordpress-plugins/wp-socializer/) {.button}