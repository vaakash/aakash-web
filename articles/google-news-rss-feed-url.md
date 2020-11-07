---
title: How to get Google news RSS feed URL ?
taxonomy:
    category: articles
---

Google news is a popular news aggregation service which is available in Google for a long time. It aggregates latest news across from multiple news sources and categorizes them based on trends, regions and topics.

You can read the same Google news in your own RSS reader, display it in your [WordPress website using Super RSS Reader plugin](/wordpress-plugins/super-rss-reader-pro/), use automation services like IFTTT or Zapier to automate whenever any article is aggregated by Google news.

You can get Google news RSS feed URL for top stories, by topic, geo location and even by language. Follow this article below to find the feed URL as needed.

## For top stories

The RSS feed for top stories is the simplest one. Just append `RSS` to the `https://news.google.com` and you get the RSS feed of the top stories of your location.

    https://news.google.com/rss

## By topic

![Google news rss feed by topic](/_images/google-news-rss-feed-1.png) {.wp-post-image}

To get the RSS feed by topic, simply visit the topic you want i.e Business, Sports, Technology like below and append `\rss` next to `news.google.com`. The resultant URL is the RSS feed of that topic.

You can apply the same to any topic you find on Google news. This will display the latest news in that topic.

Topic ID is something which look like this `CAAqJggKIiBDQkFTRWdvSUwyMHZNRGRqTVhZU0FtVnVHZ0pKVGlnQVAB` which can be seen in the URL.

    https://news.google.com/rss/topics/<TOPIC_ID>

__Example__

Here I have navigated to "technology" topic and adding `/rss` next to `news.google.com` is the RSS feed of that topic.

__RSS URL__

    https://news.google.com/rss/topics/CAAqJggKIiBDQkFTRWdvSUwyMHZNRGRqTVhZU0FtVnVHZ0pKVGlnQVAB

## By section under a topic

Similar to getting the RSS feed of a topic, the same technique can be applies to get the RSS feed URL of the particular section of a topic.

Simply navigate to the tab/section you want the RSS feed for and append `/rss` next to `news.google.com` and you get the RSS feed URL for that section.

    https://news.google.com/rss/topics/<TOPIC_ID>/sections/<SECTION_ID>

__Example__

    https://news.google.com/rss/topics/CAAqJggKIiBDQkFTRWdvSUwyMHZNRFp1ZEdvU0FtVnVHZ0pKVGlnQVAB/sections/CAQiSkNCQVNNUW9JTDIwdk1EWnVkR29TQldWdUxVZENHZ0pKVGlJT0NBUWFDZ29JTDIwdk1EZGljekFxQ2dvSUVnWlVaVzV1YVhNb0FBKi4IACoqCAoiJENCQVNGUW9JTDIwdk1EWnVkR29TQldWdUxVZENHZ0pKVGlnQVABUAE?hl=en-IN&gl=IN&ceid=IN%3Aen

## By custom search keyword

In case you want to read RSS feed which has particular keyword then you can use below format

    https://news.google.com/rss/search?q=<KEYWORD>

Here, replace `keyword` with the keyword you want the RSS feed for. For example if you want to RSS feed for Google news articles with the word `instagram` then the URL will be below.

    https://news.google.com/rss/search?q=instagram

## By country and language

You might have noticed that Google appends additional URL parameters like `hl`, `gl` and `ceid` to the google news URL. These are the parameters which decide the language, geo location the display the news for.

These parameters apply to any RSS feed above mentioned. The key is to change the language and country code as needed.

    https://news.google.com/rss?hl=<LANGUAGE_CODE>&gl=<COUNTRY_CODE>&ceid=<COUNTRY_CODE>:<LANGUAGE_CODE>

Here replace `LANGUAGE_CODE` and `COUNTRY_CODE` with the code of the language and country respectively you are looking for. You can find these code in [this page](https://www.fincher.org/Utilities/CountryLanguageList.shtml)

__Example__

    https://news.google.com/rss?hl=ta&gl=IN&ceid=IN:ta

In this example, country is India and language is Tamil. It is to note that Google news may not support all the available country and language codes.

## Displaying the RSS feed in WordPress

In case you want to display Google News in your self hosted WordPress website, then you can install a plugin called Super RSS Reader. This plugin allows you to display any RSS feed. With the above method you can get the RSS feed for Google news and use it with the plugin.

The [free version](https://wordpress.org/plugins/super-rss-reader/) allows to display any RSS feed in widget whereas the [PRO version](/wordpress-plugins/super-rss-reader-pro/) can display RSS feed in both widget and inside posts/pages using shortcodes.

Check out more about [Super RSS Reader](/wordpress-plugins/super-rss-reader/) to display RSS feed in your website.