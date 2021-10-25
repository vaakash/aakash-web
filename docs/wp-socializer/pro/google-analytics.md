---
title: Google Analytics
menu_order: 5
taxonomy:
    doc_category: wordpress-plugins
---

_With Google Analytics integration feature, WP Socializer will send tracking event to Google Analytics whenever a link a share/follow link is clicked._

**Note:**

- Google Analytics script should be already present and configured on your website.
- Clicks/Shares can be tracked on Google Analytics website directly.
- Clicks/Shares events are sent for both Google Analytics and Google tag manager.
- Both Google Analytics Universal property and the new Google Analytics 4 are supported.

## Enabling Google Analytics integration

Google Analytics integration feature with WP Socializer does not require any special configuration. You can enable the feature like below,

- Go to _WP Socializer_ → _Google Analytics integration_
- Under _Enable/disable Google Analytics integration_ click the toggle to enable the feature.

### How does it work ?

Google Analytics supports tracking events happening on a site. WP Socializer makes use of this and send "events" to Google Analytics whenever a share/follow link is clicked on your website. **Note** WP Socializer expects Google analytics to be already configured with the script present in your posts/pages.

These custom events can be viewed in your Google Analytics dashboard. Below are the event information sent by WP Socializer.

- _Event Action_ - Share or Follow
- _Event Category_ - The name of the social network
- _Event label_ - The URL of the page which is shared/followed.
- _Origin_ - The feature from which the click happened i.e floating sharebar, follow bar etc. **Note:** This event information can be viewed only in Google Analytics 4

Google Analytics by default collects more information along with the ones sent by WP Socializer like user information, page location, browser details, date/time etc. Using these details you can track share/follow activities happening on your website.

**Note**
- The action `Share` indicates that a WP Socializer share related icon is clicked i.e from [Share icons](../share-icons.md), [Floating sharebar](../floating-sharebar.md), [Text sharebar](../text-sharebar.md) or from [Share icons shortcode](../shortcodes.md)
- The action `follow` indicates that a WP Socializer follow related icon is clicked i.e from [Follow icons](../follow-icons.md), [follow icons widget](../widgets.md), [follow icons shortcode](../shortcodes.md)

## Tracking clicks/shares in Universal Google Analytics property

If you are using Google Analytics universal analytics property then you can see WP Socializer events like below.

- Login to your [Google Analytics dashboard](https://analytics.google.com/analytics/web/)
- Select your _Google Analytics account_ → _&lt;your universal analytics property&gt;_ → _&lt;your view&gt;_

### Realtime

Under _Reports_ → _Real-time_ → _Events_ you can see all the realtime WP Socializer events happening on your website.

Please find some example screenshots below.

### History

- Go to _Reports_ → _Behavior_ → _Events_ → _Top events_
- Select _Primary dimension_ as _Event action/category/label_
- Search for the type of action/social networking site/page URL as needed above the table to see history

Please find some example screenshots below.

## Tracking clicks/shares in Google Analytics 4

If you are using Google Analytics 4 property then you can see WP Socializer events like below.

- Login to your [Google Analytics dashboard](https://analytics.google.com/analytics/web/)
- Select your _Google Analytics account_ → _&lt;your google analytics 4 property&gt;_

### Realtime

- Under _Real-time_ → _Events_ section, you can see all the realtime WP Socializer events happening on your website.

### History

- Go to _Engagement_ → _Events_
- Search for the event name share or follow
- Click the event to see more details.

Please find some example screenshots below.

## Tracking clicks/shares using Google Tag manager

If you are using Google Tag manager then you can configure Google Tag manager to receive the events and pass it on to Google Analytics of your choice.

- Log in to your Google Tag Manager dashboard.

### Creating variables

- Variables → User-defined variables → New
    - Variable 1
        - Variable name = Social Network
        - Variable type = Data layer variable
        - Data layer variable name = socialNetwork
    - Variable 2
        - Variable name = Social Action
        - Variable type = data layer variable
        - Data layer variable name = socialAction
    - Variable 3
        - Variable name = Social Target
        - Variable type = data layer variable
        - Data layer variable name = socialTarget
    - Variable 4
        - Variable name = UA tracking ID
        - Variable type = Google Analytics settings
        - Tracking ID = 

### Creating trigger

- Trigger → New
    - Name = WP Socializer trigger
    - Trigger type = Custom event
    - Event name = `wp_socializer`
    - Event = equals = `wp_socializer`

### Create Google analytics tag

- Tags → New
    - Name = Google Analytics tag (UA) (For Universal analytics property)
    - Tag configuration:
        - Tag type = Google analytics: Universal analytics
        - Track type = Event
        - Category = `{{Social Network}}`
        - Action = `{{Social Action}}`
        - Label = `{{Social Target}}`
        - Google Analytics settings = `{{UA tracking ID}}`

    - Triggering:
        - Firing triggers = WP Socializer trigger
        - Submit → Publish changes

    - Name = Google analytics tag (GA) (For Google Analytics 4 property)
    - Tag configuration:
        - Configuration Tag = None - Manually set
        - Measurement ID = &lt;your GA4 measurement ID&gt;
        - Event name = `{{Social Action}}`
        - Event parameters = Add row
            - Parameter Name = `event_category`, Value = `{{Social Network}}`
            - Parameter Name = `event_label`, Value = `{{Social Target}}`
