---
title: Custom parameters
menu_order: 3
taxonomy:
    doc_category: wordpress-plugins
---

Custom parameters in Shortcoder provide an ability to change shortcode content when the shortcode is used. Custom parameters are tokens enclosed within `%%` and are placed in shortcode content. These tokens can be replaced with whatever value when the shortcoder is used by passing an attribute of the same name of the parameter.

With custom parameters simple templates can be created and later the parameters can be changed when shortcode is used. Custom parameters cannot have spaces and must be wrapped in `%%` double percentage signs. Example `%%text%%`. This custom parameter can be replaced like below.

    [print_sc sc='{sc name="my_shortcode" text="My custom text"}']

Now all instances of `%%text%%` will be replaced in the shortcode content with "My custom text" and the content will be printed.

Note: Custom parameter "name" is not allowed as the same attribute name is used to identify the shortcode itself.

In a shortcode content any number of custom parameters can be used. While using if any custom parameter attribute is not provided, the custom parameter tokens will be replaced but with blank content.

Shortcoder also provides an easy interface to set values for custom parameters in the "Insert shortcode" popup in the post/page editors.

## Examples

### #1: Simple

The shortcoder "**myMood**"s content is "**My mood is _%%misc1%%_** ". Here `%%misc1%%` is the custom parameter.

Now you should use the parameter **misc1** with your shortcoder syntax.

In post :

    [print_sc sc='{sc name="myMood" misc1="Happy"}']

This will produce the output as

`My mood is Happy`

or use in post as

    [print_sc sc='{sc name="myMood" misc1="Sad"}']

will give output as

    My mood is Sad

### What happens above ?

In the above example the shortcoder content has a attribute `%%misc1%%` . Now you should use `[print_sc sc='{sc name="myMood" misc1="Happy"}']` in the post. See that the attribute misc1 has been given a value **Happy** within quotes. Now the output will be `My mood is Happy`

### #2: Embed YouTube video

Name = `youtubeVideo`

Content =

    <iframe width="%%width%%" height="%%height%%" src="//www.youtube.com/embed/%%id%%" frameborder="0" allowfullscreen></iframe>

In Post =

    [print_sc sc='{sc name="youtubeVideo" width="560" height="340" id="GOfhmzNLWzY" }']

Output =

### #3: a simple donation box

Name = `donateBox`

Content =

    <h3>Make some donation to %%myname%%</h3>  
    <p>If you like <strong>%%myname%%</strong>, just buy me a coffee !!</p>  
    <p>Click this link to donate: <a href="%%link%%">%%mybutton%%</a></p>

In post =

    [print_sc sc='{sc name="donateBox" myname="Project 1" link="https://www.paypal.com/" mybutton="Donate by PayPal" }']

Output =

### Make some donation to Project 1

If you like **Project 1**, just buy me a coffee !!

Click this link to donate: [Donate by PayPal](https://www.paypal.me/vaakash)