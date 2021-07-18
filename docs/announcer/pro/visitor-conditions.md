---
title: Visitor conditions
menu_order: 4
taxonomy:
    doc_category: wordpress-plugins
---

With "Visitor conditions" feature in Announcer WordPress plugin, you can target specific users and display announcement only to them.

You can build your own rules easily within the settings page and make sure only certain users see the announcement.

**Note:** Rules "Number of times an user has logged in" and "Number of times an user has visited the site" set cookies in the user's browser to track the information. You can consider this information to be included in your cookie policy if needed. These cookies are used only by announcer plugin to evaluate the rule and not used for any other purposes.

![Visitor conditions settings in Announcer PRO WordPress plugin](/_images/ancrp-visitor-conditions.png) {.wp-post-image}

## List of supported visitor conditions

### 1) Referrer

Target users who are coming to your page from a specific website.

**Example:** If you want to target users who are coming from Google search result then you can create a rule like `Referer` - `contains` - `google.com`

### 2) Cookie

Target users who have certain cookie set or a cookie set with a specific value.

**Example:** To target user who has the cookie `mycookie` then you can create a rule like `Cookie` - `exists` - `mycookiename`. If you want to check the value of the cookie then you can set the value as `mycookiename=my desired value`

### 3) Query parameters

Target users when they reach your page with certain query parameters set to the page URL. i.e `param1` is the query parameter in the URL `http://mywebsite.com/?param1=value1`

**Example:** This is helpful to show announcement to users who are coming to your website by clicking a facebook ad. You can use the `utm_*` query parameter for example. You can set a rule like `Query parameters` - `exists` - `utm_source=facebook`. If you want to just check for the presence of query parameter then simply set value as `utm_source`

### 4) Browser

Target users by the type of browser used.

**Example:** `Browser` - `is` - `Chrome` will target user who use the Chrome browser. Please note that the browser name is searched in the [User agent](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/User-Agent) string. You can enter any browser name and target users as long as the user agent string has the name of the browser.

To select multiple browsers, add multiple `or` rules with the `browser` condition.

### 5) Operating system

Target users by the type of operating system used.

**Example:** `Operating system` - `is` - `Windows` will target user who are using the Windows OS. Same like "browser" condition mentioned above the name of the operating system is searched in user agent string. You can only enter name which are sent in the user agent.

### 6) Device type

Target users by the type of device used. i.e mobile (or) desktop

### 7) User logged in status

Target users by whether they are logged in or logged out. If you want to show/hide the announcement based on used logged in status then you can add this rule.

**Example:** `User logged in status` - `is` - `logged in` will target users who are logged in.

### 8) User role

Target users on the user role assigned to them. This works only when the user is logged in. You can use this to show/hide announcements based on their role.

**Example:** `User role` - `is` - `subscriber` will target users with the role subscriber. If you want to target multiple roles then please add a new rule group for each.

### 9) Custom function

Target users who meet your own custom JavaScript function. The custom JavaScript function should return `true` or `false` after evaluating your own custom logic.

Use this to write your own rules in case above rules are not satisfied or if you want to your website backend or so. It is an open end which you can use to check anything.

**Example:** You can write a function to show the announcement to users where the screen size is smaller than 800 pixels like below.

    function announcer_small_screen(){
        if(screen.width < 800){
            return true;
        }else{
            return false;
        }
    }

You can then set the function name as value to the rule like `Custom function` - `is` - `announcer_small_screen`

### 10) URL

Target users based on the text in the URL. Multiple operators like `contains`, `regex` and more are supported by this rule.

**Example:** `URL` - `contains` - `hello` will target users when the page URL has the word `hello`

### 11) Number of times an user has logged in

Target users based on the number of times they have logged in. This is tracked by placing a cookie in the user's browser and increasing it whenever they login. When there is no cookie, the user is considered to have no logins. This cookie expires in 1 year.

Multiple operators like `greater_than`, `lesser_than` and `equal_to` are supported by this rule.

**Example:** `No. of times an user logged in is` - `greater_than` - `10` will target users who has logged in to the website more than 10 times.

### 12) Number of times an user has visited the site

Target users based on the number of time they have viewed the site. This is tracked by placing a cookie in the user's browser and increasing it every 1 hour whenever they visit the site. This information is recorded for the entire site and not for an individual page. When there is no cookie, the user is considered to have no visits. This cookie expires in 1 year.

Multiple operators like `greater_than`, `lesser_than` and `equal_to` are supported by this rule.

**Example:** `No. of times an user viewed site is` - `lesser_than` - `5` will target users who has visited the site less than 5 times.

## Building multiple rules

By default with no rules set, the announcement will be displayed to all users.

You can check for multiple conditions which is called "Rules group". If the user meets **any** of the rules group then the announcement is shown.

A rules group evaluates to pass only when all the rules in the rules group meet. i.e they are `and` conditions.

Since announcement is shown when any of the rules group is met they are `or` conditions.

So you can create multiple rules group if needed if you want the user to meet any of the rules group condition.

In the image below, the announcement will be shown when either of these meet

1. when the user uses Chrome browser and comes from `google.com`
2. when the user's operating system is Windows.

![Visitor conditions settings in Announcer PRO WordPress plugin](/_images/ancrp-visitor-conditions.png) {.wp-post-image}

## How "location rules" differ from "visitor conditions"

With location rules you define the rules on which posts and pages you need to insert the announcement.

Visitor conditions is an additional check which further checks various user properties like referrer, browser etc. as mentioned above.

### Haven't got the plugin yet ?

If you haven't downloaded the plugin yet, please visit the plugin homepage to purchase and download the plugin using the link below.

[Get PRO version](https://www.aakashweb.com/wordpress-plugins/announcer-pro/?utm_source=doc&utm_medium=visitor-conditions&utm_campaign=ancr-pro#purchase) {.button}