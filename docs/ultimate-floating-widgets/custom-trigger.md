---
title: Custom trigger
menu_order: 3
taxonomy:
    doc_category: wordpress-plugins
---

Ultimate floating widgets plugin provides many trigger options like "from button", "Automatic on page scroll". If you want to open the widget box using a custom link then you can follow the instructions below.

**Note:** 

* Using this method, the widget box will not open below/above the link. It will still open near the corner/sides of the page as it is configured. Here just that the button is not used as a trigger.

* If you want to hide the button then select Trigger -> Automatic on page scroll and enter `200` as the value for "Open widget box when page is scrolled". This ensures that the button is not shown and not displayed automatically on scroll.

## The JavaScript call

The plugin has a simple JavaScript API with which you can open/close/toggle the widget box.

    // To open the widget box
    UFW.open('<WIDGET_BOX_ID>');

    // To close the widget box
    UFW.close('<WIDGET_BOX_ID>');

    // To toggle the widget box
    UFW.toggle('<WIDGET_BOX_ID>');

Here `WIDGET_BOX_ID` is the ID of the widget box. This can be found in the edit page in the browser address bar.

You can call these JavaScript functions in your script or using a simple link like below

    <a href="#" onclick="event.preventDefault(); UFW.open('5');">Open the widget box</a>

Here the onclick attribute has the JS call to open the widget box. You can follow the above example to make anything open/close the widget box.

### Example with jQuery

If you are using jQuery and want to open a link with a specific class to open/close the widget box then you can add the click even like below.

    // HTML
    <a href="#" class="my_link">Open close widget</a>
    
    // JavaScript
    jQuery(document).on('click', '.my_link', function(e){
        e.preventDefault();
        UFW.open('<WIDGET_BOX_ID>');
    });