---
title: Socializer.js - Doc
taxonomy:
    doc_category: misc
---

<h2>Usage</h2>
<p>Socializer.js generates HTML for with respect to socializer.css features.</p>

<h3>Example</h3>
<pre>
&lt;script src=&quot;https://cdn.rawgit.com/vaakash/socializer/master/js/socializer.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
    socializer( '.my-element' );
&lt;/script&gt;
</pre>

<h3>Syntax</h3>
<pre>
&lt;script&gt;
    socializer( 'element to be selected', properties_object );
&lt;/script&gt;
</pre>

<h2>Options</h2>
<p>We can set options in two ways.</p>
<ul>
    <li>Inline using <code>data-*</code></li>
    <li>External options via JS object</li>
</ul>

<h3>Inline options</h3>
<p>Inline options should be set on the target element which gets converted into a sharebar.</p>
<p>Note: All examples below assumes <code>socializer.js</code> is included</p>

<h4>Example</h4>
<pre>
&lt;div class=&quot;my-buttons&quot;
data-features=&quot;32px,circle,vertical,icon-white,pad&quot;
data-sites=&quot;facebook,googleplus,instagram,print,email,rss,more&quot;
data-text=&quot;in&quot;
data-meta-link=&quot;http://www.aakashweb.com/&quot;
data-meta-title=&quot;Aakash Web&quot;

data-meta-instagram=&quot;https://instagram.com/vaakash8&quot;
data-more="pocket,digg,flickr" &gt;&lt;/div&gt;

&lt;script&gt;
    socializer( '.my-buttons' );
&lt;/script&gt;
</pre>

<dl>
    <dt><code>data-features</code></dt>
    <dd>This attribute holds all the CSS classes separated by comma and defines the appearance of the social buttons. List of all CSS classes can be referred in <a href="/docs/socializer-css-docs/#sharebar-css-classes">this page</a>.</dd>
    
    <dt><code>data-sites</code></dt>
    <dd>This attribute holds the list of social media buttons to be generated. List of all supported social media sites can be seen in <a href="/docs/socializer-css-docs/#color-schemes">this page</a>.</dd>
    
    <dt><code>data-text</code></dt>
    <dd>The attribute holds the text style for the buttons. If it is empty no texts will be shown. List of all CSS classes can be referred in <a href="/docs/socializer-css-docs/#sharebar-css-classes">this page</a> (optional)</dd>
    
    <dt><code>data-meta-link</code></dt>
    <dd>The URL to be shared is provided here (optional: When this is empty, the current page URL is used automatically)</dd>
    
    <dt><code>data-meta-title</code></dt>
    <dd>The title of the page to be shared is provided here (optional: When this is empty, the current page title is used automatically). Similarly there are other properties like <code>data-meta-twitterusername</code>, <code>data-meta-image</code>, <code>data-meta-rss</code> which can be used to change the respective properties.</dd>
    
    <dt><code>data-meta-{social_site_id}</code></dt>
    <dd>Attributes of this kind can be used to give custom URL to the specific social button. If placeholders like <code>{url}</code>, <code>{title}</code> are present in the URL, they will be replaced with the page's URL and title respectively. List of all supported social media site ID can be referred in <a href="/docs/socializer-css-docs/#color-schemes">this page</a>.(optional)</dd>
    
    <dt><code>data-meta-more</code></dt>
    <dd>Social media site IDs mentioned in this page are moved to a more menu. Make sure that the <code>data-sites</code> has a <code>more</code> ID present in the list. (optional: When this is empty, the current page title is used automatically)</dd>
    
</dl>

<h3>External options</h3>
<p>External options are the ones set via the properties while initializing. These properties are similar to the inline options and are self explanatory.</p>

<h4>Example</h4>
<pre>
&lt;div class=&quot;my-buttons&quot;&gt;&lt;/div&gt;

&lt;script&gt;
    socializer( '.my-buttons', {
        sites: [ 'facebook', 'twitter', 'googleplus', 'print', 'email', 'rss' ],
        features: '32px,circle,vertical,icon-white,pad',
        more: 'pocket,digg,flickr',
        meta: {
            link: 'https://www.aakashweb.com/',
            title: 'Aakash Web',
            description: '',
            image: '',
            rss: '',
            twitterusername: '',
            instagram: 'https://instagram.com/vaakash8'
        },
        text: 'in'
    });
&lt;/script&gt;
</pre>

[sc name="donateForm" title="Donation for Socializer JS"]