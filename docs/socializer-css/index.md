---
title: Socializer.css - Doc
taxonomy:
    doc_category: misc
---

<h2>Getting started</h2>
<h3>1. Including the resources</h3>
<p>Include socializer.css and font-awesome font icon into the page.</p>
<p>Note: Any font-icon or images can be as icon, font-awesome font icon has the most number of social media icons and color schemes are defined as per its list.</p>

<pre>
&lt;link rel=&quot;stylesheet&quot; type=&quot;text/css&quot; href=&quot;https://cdn.rawgit.com/vaakash/socializer/master/socializer.css&quot;&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;https://maxcdn.bootstrapcdn.com/font-awesome/4.6.1/css/font-awesome.min.css&quot;&gt;
</pre>

<h3>2. The HTML</h3>
<p>Socializer.css depends on the following HTML structure. This HTML structure can be used directly or <code>socializer.js</code> can be used to generate it dynamically on the fly.</p>
<p>Note: Socializer.js generates HTML with font-awesome icon classes. So if it is the preferred way, make sure that font-awesome is included in the page.</p>

<h4>With socializer.js</h4>
<pre>
&lt;!-- Turns into social sharebar --&gt;
&lt;div class=&quot;socializer&quot; data-features=&quot;32px,circle,icon-white,pad&quot; data-sites=&quot;facebook,googleplus,print,email,rss&quot;&gt;&lt;/div&gt;

&lt;script src=&quot;https://cdn.rawgit.com/vaakash/socializer/master/js/socializer.js&quot;&gt;&lt;/script&gt;
&lt;script&gt;
(function(){
    socializer( '.socializer' );
}());
&lt;/script&gt;
</pre>

<h4>Without socializer.js</h4>
<pre>
&lt;ul class=&quot;socializer sr-32px sr-icon-white&quot;&gt;&lt;!-- Wrapper with &quot;socializer&quot; class followed by customization class names prefixed with sr- --&gt;
	&lt;li class=&quot;sr-twitter&quot;&gt;
		&lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-twitter&quot;&gt;&lt;/i&gt;&lt;/a&gt;
	&lt;/li&gt;
	&lt;li class=&quot;sr-facebook&quot;&gt;
		&lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-facebook&quot;&gt;&lt;/i&gt;&lt;/a&gt;
	&lt;/li&gt;
	&lt;li class=&quot;sr-{social_media_site_name}&quot;&gt;
		&lt;a href=&quot;#&quot;&gt;{social_media_icon}&lt;/a&gt;
	&lt;/li&gt;
&lt;/ul&gt;
</pre>
<p>Refer the below section for the list of social media button classes supported by socializer.css</p>

<h2 id="sharebar-css-classes">CSS classes</h2>
<p>Following CSS classes are supported by socializer.css. These names should be prefixed with <code>sr-</code> while using as CSS classes.</p>
<table>
<thead>
<tr>
<th>Sizes</th>
<th>Shapes</th>
<th>Hover effects</th>
<th>Layout types</th>
<th>Text styles</th>
<th>Border colors</th>
<th>Background colors</th>
<th>Icon colors</th>
<th>Border styles</th>
<th>Others</th>
</tr>
</thead>
<tbody>
<tr>
<td>16px</td>
<td>circle</td>
<td>opacity</td>
<td>fluid</td>
<td>text-in</td>
<td>bdr-white</td>
<td>bg-white</td>
<td>icon-white</td>
<td>bdr-sm</td>
<td>pad</td>
</tr>
<tr>
<td>32px</td>
<td>squircle</td>
<td>rotate</td>
<td>vertical</td>
<td>text-out</td>
<td>bdr-dark</td>
<td>bg-dark</td>
<td>icon-dark</td>
<td>bdr-md</td>
<td>multiline</td>
</tr>
<tr>
<td>48px</td>
<td>squircle-2</td>
<td>zoom</td>
<td></td>
<td>text-below</td>
<td>bdr-grey</td>
<td>bg-grey</td>
<td>icon-grey</td>
<td>bdr-lg</td>
<td></td>
</tr>
<tr>
<td>64px</td>
<td>diamond</td>
<td>shrink</td>
<td></td>
<td>text-hover</td>
<td></td>
<td>bg-none</td>
<td>icon-none</td>
<td>bdr-none</td>
<td></td>
</tr>
<tr>
<td></td>
<td>drop</td>
<td>float</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>ribbon</td>
<td>sink</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td>fade-white</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td>fade-black</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

<h3>Example</h3>
<p>To create a social media button with 48px icon size, circle shape, color icons, white background, small dark border and with shrink effect on hover, below is an example of how CSS classes are selected.</p>
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAG4AAAAgCAMAAADE173VAAABxVBMVEX///9Np97bSDsXFxdISEg+W5jn5+eFhYV6enohISHc3Nza2tqBgYElJSXz8/P29vb//+zQ0NC3t7e2trasrKypqamIiIh+fn54eHhzc3NWVlZTU1MvLy8dHR3s//////e2fpjhkpbT09TNzcw+fsHh4eHe3t6dnZ2Pj4+MjIyLi4t3d3dwcHBDQ0NBQUE9PT0zMzMsLCzw///z/v+Cv+r8///o9v/d8Pn///L/6sHbSY/lbjvu+//n6v////v39PL9+PDq3OxNp+KTrN5mqN5Sp97/9dLbcLWhoaGYmJh0XZjbSWPqkj33///W//+26v/l4v/09Pj26O9rwe9dtunfx+hzuOj79ufu0eTlxOGxt+BaqN+xrN709Nzhkr7+6LU+arXbXq/dgazbaqzlkpbqro3hkorbYX7bSn7xsXLcSnLcXl/fXkHbSEHeUz7fTTvB9P+S0P/S8fz/9Pbo8/Kw1vJzxfLfwPLM0O/dtOzHxerSzedNr+fYvd/Ht97O0Nv/6ti80NXhrtQ+eb723LXx0bW2p7FuibH/1qOAeZ5ib55Kap4+W57Ok5iweZiSb5jwwJb2wH7he2zrmGXvqV/gak3ohkHzh3A1AAAC0klEQVRIx7WXZ1fbMBSGHTnOjiGMJGQ2oYVCy0ozSgiEEChtU0rZq4xCoZTZvffeu/29lSUlSiI78MF+v1zLes59da8kn2OuSNZ6t57n9e56K8dIdczF2z3OGoOhxuix8zb0SjvM2mWroqMql88iRa0wpz1c+sJhbkVRE6zjBMeooQ0FDbCOs5yMmttRUB1z4tWwK2pBQWXMaucUZG5CQV2sK6wEOHw4qom5bJyiTHiOxV68+/j+LoMdJhtfpQyIPI7lWPd5QRCmK2L96fQIk43tdTDzIF7Ub4vclgS/CsLnT9EK2JsdAMDuai9FCFbvwY+nH6XQorI6nS4aPUUAbx2OBCOqPiKsXKRDBgv+BlibxI9ibidJkZ1MwPBUJ2n6FgGMJhwJRu2OBuiQwa4DcG1OnFnfukQRgulrSHWXYVWJ4DPJbeBGHqjV4wgx2kpx8ZvwOiGSDrDYmX0wHJFGMZJ6fSmSx3gDSTI7KDkNIbtCpww8jgij5wTpJh6y2E+QKymruicZIBgCSHUFPQkcwu7LqJLdBXAlAmu8GoJaSnE/NvZyoVcjCKNdml0o2E1wlZo5E278Lqy8fB6XbSayG4aNXgaStnrhEAq+QZjbSMjg1CBxGxiVOQNGpaPCYn9AMoCr+ws241z/Yk/yzlgMYfSE980NEbt7siectVPCPoDd+7iCf7CtZO8IRu9v3/g8cptMKd9f1o7FYHqQm4rhC/GwHCOfndvjj7OovImiAy76ma8Ta8diy/vw4oU29gBYi5RjNheuLTMP924hmij5qJIdoxi1q4R17wCktTibzefgFNTYSZ8pRu2UseDbX9vbq5mYTDaLWcnOfwxHBkuLY0rYwdlaG+TnTx4nDypjbc1y8+fyd1d1rL1BZjV0XnWsxewoOyV+2iINsCafSaQj0dRJt18bzMabvcZag6HW6DX76UXSDrPUmaRfJFOdhb5TGfsPrmBxJ7SseYAAAAAASUVORK5CYII=" />
<h4>Plain HTML</h4>
<pre>
&lt;ul class=&quot;socializer sr-48px sr-circle sr-bg-white sr-bdr-dark sr-bdr-sms sr-shrink&quot;&gt;
    &lt;li class=&quot;sr-twitter&quot;&gt;
        &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-twitter&quot;&gt;&lt;/i&gt;&lt;/a&gt;
    &lt;/li&gt;
    &lt;li class=&quot;sr-facebook&quot;&gt;
        &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-facebook&quot;&gt;&lt;/i&gt;&lt;/a&gt;
    &lt;/li&gt;
    &lt;li class=&quot;sr-googleplus&quot;&gt;
        &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-google-plus&quot;&gt;&lt;/i&gt;&lt;/a&gt;
    &lt;/li&gt;
&lt;/ul&gt;
</pre>
<h4>With socializer.js</h4>
<pre>
&lt;div class=&quot;socializer&quot; data-features=&quot;32px,circle,bdr-sm,bdr-dark,bg-white,pad&quot; data-sites=&quot;twitter,facebook,googleplus&quot;&gt;&lt;/div&gt;
&lt;!-- Include and initialize socializer.js once --&gt;
</pre>

<h4>Special classes</h4>
<dl>
	<dt><code>pad</code></dt>
	<dd>This class adds right padding to the buttons, separting them from each other.</dd>
	<dt><code>multiline</code></dt>
	<dd>This class adds bottom padding to the buttons. This class can be added if the buttons goes to multiple lines.</dd>
</dl>

<h3 id="text-styles">Texts</h3>
<p>When texts are included in the icon, the text CSS classes should be added to the parent of the icon instead of the main wrapper. Also the text should be wrapped with a tag with <code>text</code> class.</p>
<h4>Example</h4>
<p>Below example has text next to icon. Below example uses <code>text-in</code> for this case. Other text based classes can be referred in the above table.</p>
<pre>
&lt;ul class=&quot;socializer sr-48px sr-circle sr-bg-white sr-bdr-dark sr-bdr-sms sr-shrink&quot;&gt;
    &lt;li class=&quot;sr-twitter sr-text-in&quot;&gt;
        &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-twitter&quot;&gt;&lt;/i&gt; &lt;span class=&quot;text&quot;&gt;Twitter&lt;/span&gt;&lt;/a&gt;
    &lt;/li&gt;
    &lt;li class=&quot;sr-facebook sr-text-in&quot;&gt;
        &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-facebook&quot;&gt;&lt;/i&gt; &lt;span class=&quot;text&quot;&gt;Facebook&lt;/span&gt;&lt;/a&gt;
    &lt;/li&gt;
    &lt;li class=&quot;sr-googleplus&quot;&gt;
        &lt;a href=&quot;#&quot;&gt;&lt;i class=&quot;fa fa-google-plus&quot;&gt;&lt;/i&gt;&lt;/a&gt;
    &lt;/li&gt;
&lt;/ul&gt;
</pre>

<h2 id="color-schemes">Available social buttons with color schemes</h2>
<ul id="scrSitesList"></ul>

<script type="text/javascript">
<!--
window.addEventListener("load", function (){
	$.get( 'https://cdn.rawgit.com/vaakash/socializer/master/misc/api.json', function(data){
		$.each( data['sites'], function(name, prop){
			$( '#scrSitesList' ).append( '<li>' + name + '</li>' );
		});
	});
});
//--></script>

<h2>Floating sharebar</h2>
<p>Floating sharebar can be created by wrapping the main sharebar with floating bar related classes.</p>

<h3>Example</h3>
<pre>
&lt;div class=&quot;sr-sharebar sr-sb-hl sr-sb-top&quot;&gt;
    &lt;!-- Socializer sharebar HTML --&gt;
&lt;/div&gt;
</pre>
<h3>CSS Classes</h3>
<p>Below matrix lists all floating bar related CSS classes.</h3>
<table>
<thead>
<tr>
<th>Type</th>
<th>Position</th>
<th>Themes</th>
</tr>
</thead>
<tbody>
<tr>
<td>hl</td>
<td>top</td>
<td>white</td>
</tr>
<tr>
<td>vl</td>
<td>bottom</td>
<td>dark</td>
</tr>
<tr>
<td></td>
<td>left</td>
<td></td>
</tr>
<tr>
<td></td>
<td>right</td>
<td></td>
</tr>
</tbody>
</table>

<p>Note: If the orientation the sharebar is vertical, the layout type CSS class of the main sharebar should be <code>vertical</code></p>

[sc name="donateForm" title="Donation for Socializer CSS library"]