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

### Using WPML's Translation Management

1. Go to WPML → translation management page.
2. Under the translation dashboard scroll down to the section named "Shortcoder".
3. Select the shortcodes and follow the steps to translate them. Please refer WPML's documentation on [translation management"](https://wpml.org/documentation/translating-your-contents/) for more details.

![Screenshot showing the WPML translation management where shortcoder shortcodes are selected](/_images/scp-wpml-edit-translation-mgmt.png)

### Using the "plus" icons

1. Go to **Shortcoder → All Shortcodes**.
2. Find the shortcode you want to translate.
3. In the **language column**, click the **“+”** icon next to the language you want to translate to.

![Screenshot showing the "+" icon for translation next to a shortcode](/_images/scp-wpml-edit-sc.png)

4. Translate the shortcode content using WPML translation editor or using the WordPress editor.

![Screenshot of the shortcode content being translated with WPML editor](/_images/scp-wpml-edit-translation.png)

__Note:__ It is not required to translate the shortcode name (or title as displayed in WPML editor). If it is in case translated, you can call the shortcode using any of the available translated shortcode names.

## Step 3: Use the Shortcode on a Translated Page/Post

You can now use the shortcode in post and pages like normal. Ensure the translates posts also have the shortcode in them.

__Note:__ Do not translate the `name` attribute of the shortcode when translating posts.

![Screenshot of the shortcode used a post which has translations](/_images/scp-wpml-post-edit.png)

![Post with the shortcode inserted](/_images/scp-wpml-out-orig.png)

Below is a screenshot of the translated post with the shortcoder automatically picking the translated shortcode content.

![Translated post with the translated shortcode content](/_images/scp-wpml-out-translated.png)

## FAQ:

### Q: Do I need to translate all the shortcodes?
A: No, it is not required. You can translate only the required shortcode to the required language.

### Q: If a shortcode is not translated in a language, will it show any content?
A: Yes, shortcoder will always show content for a shortcode. If the shortcode did not have translation in the current language of the site, then it will display the content from the default/first language shortcode content.

### Q: Can I use the same shortcode name across all languages?
A: Yes. You can use the same shortcode name (e.g., [sc name="promo_banner"]) in all language versions of your pages or posts. Shortcoder will automatically detect the current language and show the appropriate translated content.

### Q: What happens if I update the default language shortcode content?
A: Updates made to the shortcode in the default language will not automatically sync to translations. You'll need to manually update the translated versions if you want them to reflect the new changes.

### Q: Can I use WPML's automatic translation for shortcode content?
A: Yes, WPML's automatic translation features must be used for shortcode content. Be sure to review the output manually—especially if your shortcode contains HTML or dynamic placeholders.

### Q: Will the translated shortcode content appear in WPML’s String Translation?
A: No. Since Shortcoder shortcodes are stored as custom post types, their content is translated via WPML’s post/page translation system, not the String Translation module.

### Q: Can I preview the translated shortcode content?
A: Yes. Once translated, you can preview the translated shortcode content by visiting the translated version of the page or post that includes the shortcode.