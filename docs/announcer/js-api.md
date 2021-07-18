---
title: JavaScript API
menu_order: 3
taxonomy:
    doc_category: wordpress-plugins
---

Announcements created using Announcer plugin can be controlled manually using JavaScript. This is useful if you want to show/hide the announcement on click of a button or anything similar.

## Getting started

Before we can access the announcement we have to ensure that the announcement is inserted in the page. Announcements will be inserted in the page when it is active and it's "location rules" match. Announcements inserted on the page will be hidden first and will be shown based on the display type.

You can select display type as "custom" so that the announcement is inserted in the page but will not be shown.

Once it is confirmed that the announcement is inserted on the page you can access the `announcer` object attached to the announcement wrapper element.

```
var my_ancr = document.getElementById('ancr-123'); // Here 123 is the announcement ID

my_ancr.announcer.show(); // Shows the announcement
my_ancr.announcer.hide(); // Hides the announcement

```

In above example, we are accessing the announcement wrapper element by ID and calling the `show` and `hide` functions of `announcer` object to show and hide the announcement bar respectively.

## Supported properties

Below properties are available in the `announcer` object which can be used to understand and control the announcement.

- `is_shown` (bool) - `true` if announcement is shown, `false` otherwise.
- `show()` (function) - Shows the announcement.
- `hide()` (function) - Hides the announcement.

### Example

In below example the announcement is shown/hidden on click of a button.


#### HTML
```
<a href="#" class="button_show">Show announcement button</a>

<a href="#" class="button_hide">Hide announcement button</a>
```

#### JavaScript

```
var my_ancr = document.getElementById('ancr-123');

var show_btn = document.querySelector('.button_show');
show_btn.addEventListener('click', function(event){
    event.preventDefault();
    my_ancr.announcer.show();
});

var hide_btn = document.querySelector('.button_hide');
hide_btn.addEventListener('click', function(event){
    event.preventDefault();
    my_ancr.announcer.hide();
});
```