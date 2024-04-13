---
title: Writing posts
menu_order: 2
taxonomy:
    doc_category: wordpress-plugins
---

With Git it write plugin you can write your WordPress posts in markdown format at the comfort of your favorite IDE.

This document itself is written using the plugin. You can see [this repository](https://github.com/vaakash/aakash-web/tree/master/docs) for reference.

## Supported file formats

Right now only "markdown" files `.md` are supported by the plugin. Please refer [markdown guide](https://www.markdownguide.org/basic-syntax/) page for more information on markdown and the syntax.

## File name

Git it write considers the file name as the post slug i.e if the name of the file is `getting-started.md` then the post slug is `getting-started`. 

It is recommended to use standard characters and avoid space as file names as the file name and post slug are used as identifiers. Having a standard name will maintain same post slug as the file name.

__Note:__ Only markdown files will be taken for publishing. These files must end with `.md`.

## Folders

For every folder present in the repository, a post will be created. The content of the folder post will be taken from the `index.md` file present under the directory. See [this repository](https://github.com/vaakash/aakash-web/tree/master/docs) for an example.

If there is no `index.md` file under the folder then the post content will be blank.

## Setting post properties like post title, tags, custom fields etc

Post properties like post title, tags can be set easily in the markdown file itself. They are added to the top of the file between two `---` triple hyphen lines. This is called "front matter" is follows the YAML syntax. See [YAML syntax](https://docs.ansible.com/ansible/latest/reference_appendices/YAMLSyntax.html) for more details.

__Note:__ Post property field names are case-sensitive.

Below post properties are supported right now.

* `title` - The post title
* `menu_order` - The menu order
* `post_status` - The status of the post. Supported values: publish, draft, pending, future
* `post_excerpt` - The post excerpt
* `post_date` - The post date to set. Supported format: `2022-09-01 20:14:59`
* `comment_status` - The comment status for the post. Supported values: `open`, `closed`
* `page_template` - The page template to set for the post
* `stick_post` - Mark the post as sticky. Supported values: `yes` to mark as sticky, `no` to unstick the post.
* `taxonomy` - The taxonomies like post tags, categories etc. For custom post type please use the custom taxonomy name.
* `custom_fields` - The custom fields of the post.
* `skip_file` - Skip the file from being published. Supported value: `yes` to skip the file.
* `featured_image` - The path of the image under `_images` directory to set as featured image. Remote image URLs are not supported. Example: `_images/post-image-1.png`

### Example

```
---
title: Title of the post
menu_order: 1
post_status: publish
post_excerpt: This is a post excerpt
featured_image: _images/post-image.jpg
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

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec a lacinia orci.
Nunc sodales massa enim, nec consectetur orci tempus ac.

### Section with image

![alt text for the image](/_images/pic4.jpg "Caption for the image")

Nam rutrum ultricies sapien id rhoncus. In pellentesque efficitur suscipit.
Aliquam vel est consectetur lectus malesuada mollis sit amet non neque. 

### Section with link

This is a [relative link](../sub-dir1/post3.md) which links to another markdown post w.r.t the current file.
This is an [absolute link](/folder1/sub-dir1/post3.md) which links to another post w.r.t the root directory.

### Section with HTML

<section id="home">
    <h2>Welcome to Our Website!</h2>
    <p>This is a sample HTML page with JavaScript and CSS styling.</p>
    <button type="button" onclick="showMessage()">Show message</button>
</section>

<script>
    function showMessage() {
        alert('Thank you for contacting us!');
    }
</script>

<!-- Sample CSS Style -->
<style>
    h1 {
        color: red;
    }
</style>

### Section with Shortcodes

[gallery ids="3052,3050,2952" columns="3" size="medium"]

```

## Using images

Images can be inserted into markdown files normally. All images should be present in the `_images` folder. Images can be organized in folders. They can be then used in the files relatively like `![alt text](/_images/pic4.jpg "Caption for the image")`.

All the images in the `_images` folder will be uploaded to the WordPress library and the images will be linked automatically to the post as they are uploaded.

The images will be uploaded only once and they will be reused whenever the post is updated or the same image is used in another post.

Please refer [this repository](https://github.com/vaakash/test/) for an example of images.

## Using links

Links can be added normally as per markdown syntax. It is preferred to use relative links to refer any post in the repository i.e to refer any post in the same directory use `./faq.md` as the link value. Git it write will convert it to `/faq/` before publishing. By doing this, the markdown files are linked correctly both in the github page and in your main website.

**Example:** `../guide/doc1.md` will link a `doc1.md` file from the `guide` folder one level up relatively. Similarly `.` can be used for current directory and `/` to refer the file from the root of the repository i.e `/folder1/folder2/doc2.md`.

## Using HTML

HTML can be used inside the markdown file like normal. An example is demonstrated above. Note that file must still remain `.md`. All tags are supported and there are no explicit filtering as of now.