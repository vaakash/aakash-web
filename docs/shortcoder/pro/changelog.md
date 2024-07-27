---
title: Changelog
menu_order: 6
taxonomy:
    doc_category: wordpress-plugins
---

### 6.4

* New: Option to set shortcode display name next to shortcode name.
* New: Option to execute WordPress block HTML in shortcode content.
* Fix: Shortcoder roles are registered when plugin is activated.
* PRO: Using `do_blocks` to execute block editor content.
* PRO: Custom editor post title is set with the shortcode name.

### 6.3.2
* PRO: Custom editor option not saving sometimes.
* Fix: Admin ajax vulnerability with nonce.
* Fix: Verify permissions while closing Shortcoder changelog.

### 6.3
* PRO: Custom editor preview works only for editor authors.
* New: Set default value for the custom field parameters.
* New: Custom parameter default value is shown in the insert shortcode popup.
* Fix: Restrict access to admin-ajax calls.
* Fix: Some admin texts were missing translation.
* Fix: Removed the note in the insert popup for fully closed shortcode.
* Fix: Debug comment line now has the name of the shortcode.

### 6.2
* PRO: Dutch translation is now available for the PRO version.
* PRO: WP Bakery CSS styles were not inserted along with the shortcode content.
* PRO: Open custom editor from the shortcode list page via action links.
* New: Option to show shortcode content in "All shortcodes" page.
* Fix: Some texts were not translated.
* Fix: Error in WP Bakery page builder while picking images.

### 6.1
* New: Custom editors management page added to Shortcoder menu.
* Fix: HTML is escaped in the editor sometimes.
* Fix: Support for WordPress 6.1

### 6.0
* PRO: Edit Shortcode content using block editor and page builder plugins like Elementor, WPBakery.
* PRO: Revisions support for Shortcode content.
* PRO: Include extra code to the footer when a Shortcode is used in a page.
* PRO: Locate the usage of shortcode in posts and pages.
* New: Prevent same shortcode nested loop.
* New: New actions and filters introduced.
* Fix: Post excerpt shortcode parameter now prints full post excerpt.
* Fix: Enhancements to input and output data sanitization.