---
title: FAQ
menu_order: 4
taxonomy:
    doc_category: wordpress-plugins
---

### What is this plugin for ?

Git it Write plugin allows to publish posts in WordPress using the files present in a Github repository

### What is the use of this plugin ?

Using this plugin you can manage the post content in a Github repository and work on it. The files will be pulled and published in WordPress automatically whenever the repository is updated. With this concept, if you need to maintain a documentation site, then you can create a Github repository, write your docs in markdown format and use this plugin to publish them as posts in your website. You can now ask your users to contribute to the documentation repository, accept suggestions etc. from the community.

### When a post is edited in WordPress will that update the file in the Github repository ?

No. This plugin won't sync post content. It is a one way update. Only changes made to the Github repository will update the posts and not otherwise.

### Which Git hosting services are supported ?

Right now Github is only supported.

### Can I use a private Github repository ?

No. Right now only public Github repositories are supported.

### What all files in the repository will be published ?

All markdown files will be published as posts. HTML is not supported right now, but there are plans to add support in the future.

### What are not published ?

Any folder/file starting with `_` (underscore), `.` (dot) won't be considered for publishing.

### From which branch files will be picked ? Can I select a branch ?

Right now files are picked only from the `master` branch and there is no option to select other branches.

### How will be the posts published ?

If a repository has files in the below structure,

```
docs\\
    guide\\
        introduction.md
        getting-started.md
help\\
    faq.md
```

Then below posts will be created like below (if permalinks are configured and the post type supports "hierarchy" i.e creating posts level by level (example: pages))

```
https:\\\\example.com\\docs\guide\\introduction\\
https:\\\\example.com\\docs\guide\\getting-started\\
https:\\\\example.com\\help\\faq\\
```

Note that the post's slug will be the name of the file (without extension)

### What will happen if the post type does not support hierarchy ?

If the post type does not support hierarchy then then all posts will be published at the same level. If there files with same name in different directories then there are chances of posts getting overwritten.

### Can I pull posts from a specific folder in the repository ?

Yes, if you want to pull posts from the a folder in a repository then you can specify it in the plugin's repository settings page. For example, if a repository has a folder `website\main\docs` and if you want to pull only from docs folder, then you can specify `website\main\docs` in the plugin settings.

### What about images and how to use in them ?

You can still use images in the markdown files. All images should be present in the `_images` folder at the root of the repository without organized as folders. They can be then used in the files relatively like `![alt text](/_images/pic4.jpg "This is pic4")`.

All the images in the `_images` folder will be uploaded to the WordPress library and the images will be linked automatically in the post as they are uploaded.

The images will be uploaded only once and they will be reused whenever the post is updated or the same image is used in another post.

### What about links and how to link posts ?

Posts within the repository can be linked relatively like `[My test post](/test/references/article.md)` or even using the double dot notation.

### How to set post properties like post title, tags, custom fields etc

They can be set at the top the file like below (YAML syntax). This is called front matter.

```
---
title: Title of the post
menu_order: 1
post_status: publish
post_excerpt: This is a post excerpt
taxonomy:
    category:
        - category-slug-1
        - category-slug-2
    post_tag:
        - tag-1
        - tag-2
custom_fields:
    field1: value 1
    field2: value 2
---

## My post content

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec a lacinia orci. Nunc sodales massa enim, nec consectetur orci tempus ac. Phasellus dapibus vitae lectus quis consectetur
```

### What will be the post slug ? Can I change it ?

Post slug will the name of the file. For example, if the name of the file is `product-reference.md` then post slug will be `product-reference`.

No the post slug cannot be changed in front matter. If the file name is changed, then a new post will be created.

### When files are deleted/renamed/moved will the posts be deleted ?

No, the posts won't be deleted. Manual action is needed to delete the affected posts.

### How to set content for the posts created for the folders ?

If a folder has a file named `index.md` then it's content will be set as post content for the posts of the folder. If it is not present, then the post content will be empty.

### How many repositories can be configured ?

There is no restriction on the number of repositories that can be configured

### Can anyone publish post if a repository is configured ?

The plugin settings page is accessible only to administrator users. Posts will be published only when repository is updated automatically when files are updated in the repository either by the repository owner or by accepting any pull request. The file committer won't be set as post author. The author of the post is fixed as configured in the plugin repository settings page.

### Can publish posts from any repository not owned by me ?

Yes. In that case, webhook configurations cannot be made only manual pull operation will publish the posts and the latest repository changes.

### Can I edit the published post inside WordPress ?

Yes, the post can be edited as needed. But when the source markdown file has changed in the repository then during the next update the manually made changes will be overwritten. Though posts can be edited as needed, tt is preferred to edit the markdown file.

### Post is not updating automatically when files in the repository are updated

Posts will be updated whenever Github sends an event to your WordPress site that files are added/updated. Please ensure that webhook related settings are set correctly both in the plugin and at the Github repository settings.

Go to logs page and view logs for any errors or failures while processing the event.

You can also view Github webhook settings page for all the events sent and the response received for various times.

### Does it support Gutenberg ?

Since HTML files are not supported right now, Gutenberg is not supported. When HTML supported is added, the Gutenberg block HTML template can be used.

### Can I use shortcodes in file content ?

Yes, shortcodes can be used as is like normal.

### How to display the Github edit link in the post ?

There is an inbuilt shortcode `[g2w_edit_link]` which can be added to the post content template in the repository settings page. This will return an output like `Edit this page`. Below shortcode attributes are supported.

- post_id - The ID of the post to display the edit link for. Default is the current post where it is used.
- text - The text to display. Default is "Edit this page"
- icon - The icon to display next to the text. Default is a "pend" icon from fontawesome icon pack. (Note: Fontawesome icon font is not loaded by the plugin, it is assumed the theme already has it or it has to be loaded manually.)

### Can we create custom post type using this plugin while configuring the repository ?

No. Custom post types can be created using other plugins like "Custom post type UI" and they can be only selected while configuring the repository.

### Webhook request is seen as timed out in Github webhook history

The webhook request sent by Github expects a reply in 10 seconds else considers th event as timed out. In case of this plugin, it is normal to take more than 10 seconds for creating/updating multiple posts. This time out message can be ignored as the plugin will continue to post in the background. You can see the plugin logs for more information WRT to the webhook delivery.