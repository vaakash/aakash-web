---
title: FAQ
menu_order: 5
taxonomy:
    doc_category: wordpress-plugins
---

<div class="accordion" markdown="1">

### Q: My shortcode is not working !
<div markdown="1">
A: Please check the following if you notice that the shortcode content is not printed or when the output is not as expected.

- Please verify if the shortcode content is printed. If shortcode content is not seen printed, check the shortcode settings to see if any option is enabled to restrict where and when shortcode is printed. Also confirm if the shortcode name is correct and there is no duplicate `name` attribute for the shortcode.
- If shortcode is printed but the output is not as expected, please try the shortcode content in an isolated environment and confirm if the shortcode content is working correctly as expected. Sometimes it might be external factors like theme, other plugin might conflict with the shortcode content being used.
- There is a known limitation in shortcodes API when there is a combination of unclosed and closed shortcodes. Please refer [this document](https://codex.wordpress.org/Shortcode_API#Unclosed_Shortcodes) for more information.
</div>

### Q: My shortcode is not working in my page builder !

A: Please check with your page builder plugin to confirm if the block/place/area where the shortcode is being used can execute shortcodes. If yes, then shortcode should work fine just like regular WordPress shortcodes.

### Q: Do I need to enclose any content within the shortcode ?

A: The content enclosed within the shortcoder will be used only when the shortcoder parameter `$$enclosed_content$$` is used in the shortcode content. This parameter will be replaced with the enclosed upon execution.

### Q: What are the allowed characters for shortcode name ?

A: Allowed characters are alphabets, numbers, hyphens and underscores.

### Q: How to export/import shortcodes (applies to shortcoder v5.0+) ?

A: WordPress provides an inbuilt import/export tool for posts/pages. The same tool can be used for shortcodes also. To export shortcodes navigate to Tools --> Export and select "Shortcoder" to export. Please save this file to import/restore shortcodes later. To import shortcodes navigate to Tools --> Import and select "Run importer" under WordPress and follow the instructions.

### Q: How to import shortcodes which were create before v5.0 ?

A: Currently there is no feature provided to import shortcodes exported as CSV in old shortcoder.

### Q: Can I change the name of the shortcode ?

A: Yes, shortcode name can be changed. But please note that the shortcodes which are already used may print blank if the shortcode does not exist.

### Q: Can I use shortcode in my WordPress theme ?

A: Yes, please use the `do_shortcode` function provided by WordPress to execute shortcodes. Please [refer here](https://developer.wordpress.org/reference/functions/do_shortcode/#comment-1958) for usage example.

### Q: How can I remove shortcodes from the posts/pages ?

A: Currently there is no tool provided to identify and delete shortcodes. You can use the post/page search functionality in admin page to locate the posts and remove the shortcode.

### Q: Can I use the ID instead of name to identify the shortcode ?

A: Yes, please use `[print_sc sc='{sc sc_id="ID_of_shortcode"}']`

### Q: Can I use any other shortcode inside shortcode content ?

A: Yes, you can use any shortcode. Please make sure the same shortcoder shortcode itself is not used as shortcode content as it might lead to recursion and page not working.

### Q: Can I set custom shortcode name instead of `sc` ?

A: No, this is not supported. Shortcodes created via shortcoder are identified via `sc` and cannot be changed. Please refer the [shortcoder API](https://codex.wordpress.org/Shortcode_API) to create custom shortcodes.

### Q: Do we need to close all shortcodes with `[/sc]`?
<div markdown="1">
A: No, but this is dependent on how many shortcodes inserted in a post. When there is a mix of open and closed shortcodes in a post, WordPress cannot parse the shortcode in the right order. This will lead to some shortcodes considered as nested shortcodes.

```
Paragraph 1
[[sc name="my-shortcode-1"]]

Paragraph 2
[[sc name="my-shortcode-2"]]

Paragraph 3
[[sc name="my-shortcode-3"][/sc]]
```

❌ Here, everything between my-shortcode-1 and my-shortcode-3 won't be displayed because my-shortcode-3 has a closing shortcode.

It is always a good practice to close all the shortcodes or keep all shortcodes open. A mix of both will cause the above issue.

Learn more about how [nested shortcodes here](https://codex.wordpress.org/Shortcode_API#Unclosed_Shortcodes)
</div>

### Q: Why a chunk of post content is missing (or) shortcode not executed in my post?
<div markdown="1">
A: This might be because, there would a mix of open and closed shortcoder shortcodes in your post. Please ensure all shortcodes are either closed with `[/sc]` tag or all shortcodes are fully open. A mix of both will cause parsing issue.

```
Paragraph 1
[[sc name="my-shortcode-1"][/sc]]

Paragraph 2
[[sc name="my-shortcode-2"][/sc]]

Paragraph 3
[[sc name="my-shortcode-3"][/sc]]
```

✅ Close all the Shortcoder's shortcodes in a post with `[/sc]`.
</div>

### Q: Can other users create/modify/use shortcodes ?

A: Yes, other users can create/modify shortcodes when the user's role has the capability to create/edit shortcoder admin page. Plugins like [user role editor](https://wordpress.org/plugins/user-role-editor/) can be used to set the necessary capabilities on the shortcode admin page to make the users create/edit shortcodes. Please note that shortcodes created by any user can be used by any user in posts and pages.

### Q: Can I use PHP as shortcode content ?

A: No, it is not supported. Shortcoder content only supports HTML, CSS and JavaScript.

### Q: Can I use `if/else` conditions in shortcode content ?

A: No, it is not supported. But you can achieve something similar using JavaScript.

## v5.0+ Upgrade FAQs

### Q: After v5.0 upgrade all my shortcode names have hyphens

A: Yes. After v5.0 upgrade, all the shortcodes are upgraded to a format where spaces are replaced with hyphens. This is because, v5.0+ does not plan to support spaces in shortcode names.

### Q: Do I need to update my posts with the new shortcode name since spaces are replaced with hyphens ?

A: No. There is no need to make any changes. For example, before v5.0 if you had used a shortcode `[print_sc sc='{sc name="i have space"}']` in your posts then after v5.0, shortcoder will automatically find and execute the correct shortcode which has the name `i-have-space`. You can make changes if needed but it is not necessary. Going forward it is better to use the current name whatever is given for the shortcode.

### Q: After v5.0 upgrade, I have duplicate shortcodes.

A: v5.0+ is entirely a new version and the shortcodes created in old format will be migrated to the new format. During the process, duplicates are not expected to be added. If in case it is seen, please do report the issue in the [support forum](/forum/discuss/wordpress-plugins/shortcoder/).

### Q: Are old shortcoder data retained after the upgrade ?

A: Yes, old shortcoder data is not deleted after the upgrade.

### Q: Is it possible to move to v4.x ?

A: Yes. Old shortcoder data is not deleted and it is retained. So if in case there are any temporary issues with v5.0 you can revert back to the old version. But please note that the interface and features seen will be retained going forward so please do report any issues faced.

</div>