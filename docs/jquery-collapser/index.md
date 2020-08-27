---
title: jQuery Collapser
taxonomy:
    doc_category: jquery-plugins
---

## Usage

Include jQuery and jQuery collapser in the page. Attach the `collapser` method to the elements after the DOM is ready to be manipulated.

[Demo page](/demos/jquery-collapser/)

    <script src="jquery.js"></script>
    <script src="jquery.collapser.js"></script>

    <p class="myElement">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>

    <script>
    $(document).ready(function(){
        $('.myElement').collapser({
            mode: 'words',
            truncate: 20
        });
    });
    </script>

## Supported options

Below are the complete list of options supported by collapser. The values given below are the defaults.

    $('.myElement').collapser({
        mode: 'words',
        speed: 'slow',
        truncate: 10,
        ellipsis: ' ... ',
        controlBtn: '',
        
        showText: 'Show more',
        hideText: 'Hide text',
        showClass: 'show-class',
        hideClass: 'hide-class',

        atStart: 'hide',
        blockTarget: 'next',
        blockEffect: 'fade',

        lockHide: false,
        changeText: false,

        beforeShow: null,
        afterShow: null,
        beforeHide: null,
        afterHide: null
    });

`mode` - string

The mode of operation of the plugin. Accepted values are,

- **chars**: To truncate characters
- **words**: To truncate words
- **lines**: To truncate lines
- **block**: To toggle a selected elements

`target` - string or function

This element to be selected for toggling in "block" mode is specified here. Other modes don't use this value. If the value is a string, then accepted values are `next/prev/siblings`. This selects the element which is next/prev/sibling to the current one. If the value is a function then it should return the selected element.

`speed` - string or number

The speed of transition of the height transition during the element collapse. Accepted values are time in milliseonds and strings: slow/medium/fast

`ellipsis` - string

The text displayed next to the hidden element to indicate the presence of more content. Accepts both text and HTML string.

`controlBtn` - string or function

The expand/collapse button selector. When the value is a,

- _string_: the control button is automatically created and the value is used as "class name"
- _function_: the control button is not created and hence the function should return a jQuery element

`showText` and `hideText` - string

The text/HTML to be present in the control button when the element is in collapsed and expanded state respectively.

`showClass` and `hideClass` - string

The class name of the element when it is in expanded and collapsed state respectively.

`atStart` - string or function

The default state of the element when the page is loaded. Accepted strings are "show" and "hide". The value "show" makes the element to be expanded by default and "hide" does the opposite. If a function is used, then it should return either "show" or hide". This value is overridden when the element has a `data-start` attribute. The accepted values remains the same. [Check out the demo](/demos/jquery-collapser/).

`blockTarget` - string

In block mode, this option is used to select the target element to collapse relative to the element collapser is initialized. Some values are `next`, `prev`.

`blockEffect` - string

The type of effect when toggling elements in "block" mode of operation. Accepted values are "fade" for fadeIn/fadeOut transitions and "slide" for slideUp/slideDown transitions

`lockHide` - boolean

This property removes the "hide" button once the content is expanded. Accepts boolean value.

`changeText` - boolean

This property changes the text of the element during the collapse and expand state. It is used only in "block" mode of operation and is not used by other modes.

Callbacks - function

- `beforeShow`: This function is triggered before the expand event
- `afterShow`: This function is triggered after the expand event
- `beforeHide`: This function is triggered before the collapse/hide event
- `afterHide`: This function is triggered after the collapse/hide event

## Using function as values

Some of the properties listed above accept functions as value. These functions accept only one formal parameter. This parameter is an object which holds all the public methods used in the plugin.

    $('.myElement').collapser({
        mode: 'chars',
        afterShow: function( myParam ){
            // use myParam to access the methods defined in the plugin.
        }
    });

## `this` keyword within the function

The "this" keyword used within the function points to the current element with which collapser is initializer. This is useful to manipulate the element and target other DOM elements relative to the current element. This is demonstrated in the demo page, [check it out](/demos/jquery-collapser/).

    // HTML
    <h2>Heading <a href="#" class="myControlBtn">Dummy</a> </h2>
    <p class="myElement">Some text to truncate b characters ...</p>

    // jQuery
    $('.myElement').collapser({
        mode: 'chars',
        controlBtn: function( element ){
            return $(this).parent().find( '.myControlBtn' );
        }
    });

## Methods available

Collapser has some methods which can be used externally to control the element. They are,

- `show`: accepts two parameters, one the element with collapser attached to expand and the other to specify the transition speed.
- `hide`: accepts two parameters, one the element with collapser attached to collapse and the other to specify the transition speed.
- `reInit`: accepts one parameter, the element with collapser attached to reInit

## Setting remaining text count

The remaining words/lines count is calculated by the plugin and stored in `remaining` property. Since `afterHide` function allows function, a dynamic string can be returned with the remaining count of words/lines. The function receives the element itself as a parameter and from where, the collapser option can be modified and remaining count can be accessed. This is demonstrated as demo 6 in the [demo page](/demos/jquery-collapser/).

    <p class="wordCount">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>

    $('.wordCount').collapser({
        mode: 'words',
        truncate: 10,
        showText: 'There are still <b>%s</b>, click to show',
        hideText: 'Hide ^^^',
        afterHide: function(element){
            element.o.showText = element.o.showText.replace( '%s', element.remaining + ' words' );
        }
    });