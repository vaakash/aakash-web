---
title: FAQ
menu_order: 5
taxonomy:
    doc_category: wordpress-plugins
---

### Q: How to show the popup in home/pages ?

In the widget box edit page, navigate to the "Location rules" tab. You can find two levels of configuration. Select "Basic" and select the options "hide in home page" and "pages". You can create complex rules more advanced than this using the "advanced" level of configuration which is available in the [PRO version](/wordpress-plugins/ultimate-floating-widgets-pro/).

### Q: Are widget boxes mobile responsive ?

Yes, widget boxes are responsive to small screens. Even if you provide a larger width/height for the widget box when the screen size is less than 600px then widget box will automatically switch to full screen mode.

### Q: Can I open the widget box via custom link ?

Yes, it is possible. Please check [this page](./custom-trigger.md) for more details

### Q: Can I show the widget box in the center of the page ?

No, that is not possible. Right now the widget boxes can be placed near the corners or to the sides of the window. You could use custom CSS (with flyout mode) to achieve the same but support for that would be beyond the scope of the plugin.

### Q: How to hide the widget on mobile devices ?

In Ultimate floating widgets settings page, go to the edit page of the widget box and switch to "Location rules" tab. Under this section select "On mobile devices alone".

### Q: Can I adjust the position of the button ?

Yes, using custom CSS you can adjust the position slightly as required. Note that in case of popup bubble type the popup bubble won't adjust the size dynamically as per the remaining height of the page. A minor adjustment is possible. You can use CSS like below,

    #ufw_<id>{
        bottom: 50px !important;
        right: 50px !important;
    }

### Q: Can I position the button anywhere in the page ?

With the popup bubble type, the buttons cannot be repositioned as needed. It can be positioned only near the corners of the page. However you can use CSS to adjust the position slightly like mentioned in above answer.

With flyout type, you can use custom CSS to position the button. You can use the class `#ufw_<ID> .ufw_btn` as the selector for the button.

### Q: How to add custom CSS to alter the design of the popup/widget box ?

In widget box edit page, scroll down to "Widget template settings" and click to expand the section. In that section under "Additional CSS" option you can provide your custom CSS.

### Q: How to hide the button and show it only after page scroll ?

In widget box edit page, make sure have selected "Trigger for widget box" as "From button" and scroll down to "Button customization" section. You can change when to reveal the button upon scroll under option "Reveal button when page is scrolled"

### Q: Can I add gradient background to button/widget box ?

Right now only solid colors can be set for the button and widget box. Support for gradients is in the plan. With custom CSS you can gradients right now.

### Q: Can I set an image as icon for the button ?

Yes. In the button settings tab, provide the URL of the image and the image will be used as icon.

### Q: How to open the widget box to the full screen ?

You can select the widget box type as "flyout" and set the width of the widget box as `100%`

### Q: Is it possible to have multiple columns of widgets in the widget box ?

Yes, with the [PRO version](/wordpress-plugins/ultimate-floating-widgets-pro/) of the plugin a maximum of 4 columns can be added to the widget. In the free version you can add widgets in 1 column.