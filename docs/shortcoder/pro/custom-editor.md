---
title: Custom Editor
menu_order: 2
taxonomy:
    doc_category: wordpress-plugins
---

Custom editor is a feature in Shortcoder PRO using which you can use any* editor in WordPress to set Shortcode content. By default Shortcoder includes visual, text and code editor. With custom editor you can use block editor (Gutenberg editor) or other visual builder editors like Elementor, WP Bakery etc.

***tested with Block editor, Elementor and WP Bakery only**

### Table of Contents

1. [Getting started](#getting-started)
    1. [Enabling Block editor](#enabling-block-editor)
    2. [Enabling Elementor](#enabling-elementor)
    3. [Enabling WP Bakery](#enabling-wp-bakery)
2. [Using the custom editor](#using-the-custom-editor)
    1. [Screenshot of block editor in use](#screenshot-of-block-editor-in-use)
    2. [Screenshot of elementor in use](#screenshot-of-elementor-in-use)
    3. [Screenshot of WP Bakery in use](#screenshot-of-wpbakery-in-use)
3. [Importing content between custom and default editor](#importing-content)

## Getting started

To use a custom editor for shortcode content, you must enable the editor of your choice for Shortcoder. You can follow the steps below to enable one or more editor(s) for Shortcoder.

### Enabling Block editor

Block editor is enabled by default for the shortcode content. There are no special changes required.

### Enabling Elementor

To enable "Elementor" editor for Shortcoder, follow the steps below.

1. Make sure **Shortcoder - PRO** plugin is installed and **activated**.
2. Go to _Elementor_ -> _Settings_.
3. Under the _General_ tab, select **Shortcoder Editor** for _Post types_.
4. Click _Save changes_ to save the settings.

![Enabling Shortcode editor for Elementor](/_images/scp-custom-editor-elementor.png)

### Enabling WP Bakery

To enable "WP Bakery" editor for Shortcoder, follow the steps below.

1. Make sure **Shortcoder - PRO** plugin is installed and **activated**.
2. Go to _WPBakery Page Builder_ -> _Role Manager_.
3. For every user role required, choose _Custom_ for _Post types_ and select _shortcoder_editor_.
4. Click _Save changes_ to save the settings.

![Enabling Shortcode editor for WPBakery](/_images/scp-custom-editor-wpbakery.png)

## Using the custom editor

After enabling the custom editor of your choice, you can edit the Shortcode content using that.

1. Go to _Shortcoder_ and edit a Shortcode.
2. Select **Custom editor** and click **Open editor** to launch the editor to set Shortcode content.

![Selecting custom editor from Shortcode edit page](/_images/scp-custom-editor.png)

3. In the "Edit shortcode content" page, you can choose any of the active editor and to set the shortcode content.
4. You can Publish the post to save the content.
5. When the editor is set as "Custom editor" then shortcode will use the custom editor post content as shortcode content.
6. You can find the name of the associated shortcode on the right side under _Shortcode Editor_ -> _Details_ panel.

![Selecting custom editor from Shortcode edit page](/_images/scp-custom-editor-2.png)

#### Screenshot of Block editor in use

![Using the block editor to set Shortcode content](/_images/scp-block-editor.png)

#### Screenshot of Elementor in use

![Using the Elementor editor to set Shortcode content](/_images/scp-elementor.png)

#### Screenshot of WPBakery in use

![Using the WPBakery editor to set Shortcode content](/_images/scp-wpbakery.png)

## Importing content

When you are using custom editor, you might have to import the content from the default editors or vice versa. Shortcoder PRO provides options to perform this.

To import content from default editor to custom editor, use the _Import content_ button inside the _Details_ panel on the right side in the _Edit Shortcode content_ page.

Similarly, to import content from custom editor to the default editors, use the _Import content from Custom editor_ button inside the _Custom editor_ metabox in the Shortcode editing page.

![Importing content from default editor to custom editor in Shortcoder PRO](/_images/scp-import-content.png)