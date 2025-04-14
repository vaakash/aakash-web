---
title: Translation with WPML
menu_order: 6
taxonomy:
    doc_category: wordpress-plugins
---

Shortcoder PRO supports **WPML**, allowing you to translate your shortcode content into multiple languages. If you're using WPML to translate your posts or pages, the shortcodes created with Shortcoder can now display content based on the selected language.

## Step 1: Enable Translation for Shortcoder Custom Post Types

Shortcoder PRO uses two custom post types:

- `shortcoder`
- `shortcoder_editor`

To allow WPML to handle translations for them:

1. Go to **WPML → Settings**.
2. Scroll down to the **Post Types Translation** section.
3. Find the post types:
   - **Shortcoder**
   - **Shortcoder Editor**
4. Set both to **"Translatable – only show translated items"**.

![Screenshot showing WPML settings with both post types set to "Translatable"](/_images/scp-wpml-cpt.png)

## Step 2: Translate a Shortcode

Once translation support is enabled, you can translate each shortcode just like any other post or page.

1. Go to **Shortcoder → All Shortcodes**.
2. Find the shortcode you want to translate.
3. In the **language column**, click the **“+”** icon next to the language you want to translate to.

![Screenshot showing the "+" icon for translation next to a shortcode](/_images/scp-wpml-edit-sc.png)

4. Translate the shortcode content using WPML translation editor or using the WordPress editor.

![Screenshot of the shortcode content being translated with WPML editor](/_images/scp-wpml-edit-translation.png)

## Step 3: Use the Shortcode on a Translated Page/Post

You can now use the shortcode in post and pages like normal. Ensure the translates posts also have the shortcode in them.

![Screenshot of the shortcode used a post which has translations](/_images/scp-wpml-post-edit.png)

![Post with the shortcode inserted](/_images/scp-wpml-out-orig.png)

Below is a screenshot of the translated post with the shortcoder automatically picking the translated shortcode content.

![Translated post with the translated shortcode content](/_images/scp-wpml-out-translated.png)