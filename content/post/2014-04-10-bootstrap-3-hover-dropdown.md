---
title: Bootstrap 3 Hover Dropdown
author: Julien Vernet
layout: post
date: 2014-04-10T07:39:49+00:00
url: /bootstrap-3-hover-dropdown/
prompt_recipient_ids:
  - 'a:0:{}'
subscribed_user_ids:
  - 'a:1:{i:0;i:3;}'
categories:
  - Bootstrap
  - Code Snippets
format: chat

---
As far I can remember, the Boostrap dropdown menu has always worked on click event. So unless you&#8217;re doing a web app, you&#8217;re most likely to want the Bootstrap dropdown menu to work on mouse-over.

Here are the two solutions I use, depending on the project:

## 1) CSS only technique (30 seconds)

This is in my opinion the easiest way to get the **Bootstrap 3 dropdown menu to work on hover** state. It&#8217;s lightweight and super easy to implement. Check out the JavaScript technique if you want more control of the hover state of Bootstrap dropdown menus.

<pre class="coolsyntax"><code class="lang-css">@media (min-width: 768px) {
	.dropdown:hover .dropdown-menu {
		display: block;
	}
}</code></pre>

## 2) JavaScript technique (5 min)

The main advantage of this solution over the first one is that you have a better control of the behavior. Using JavaScript allows you to add a delay before the dropdown closes automatically. This is a good thing in term of user experience / usability.

<span style="color: #ff0000;"><strong>Edit July 2015, from the comments:</strong></span>

> CWSpear’s plugin is using dirty hacks, and is not working on modern desktop browsers with touch support, so I made a proper plugin which is using only the Bootstrap javascript API, hence it works on all devices without braking any functionality: https://github.com/istvan-ujjmeszaros/bootstrap-dropdown-hover

[zilla\_button url=&#8221;https://github.com/istvan-ujjmeszaros/bootstrap-dropdown-hover/releases&#8221; style=&#8221;orange&#8221; size=&#8221;medium&#8221; type=&#8221;square&#8221; target=&#8221;\_self&#8221;] Download the plugin [/zilla_button]

### How to get started?

1. Include jQuery, Bootstrap and the plugin

<pre class="coolsyntax"><code class="lang-markup">&lt;link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css"&gt;
&lt;script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"&gt;&lt;/script&gt;
&lt;script src="//maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"&gt;&lt;/script&gt;

&lt;!-- The plugin --&gt;
&lt;script src="dist/jquery.bootstrap-dropdown-hover.min.js"&gt;&lt;/script&gt;</code></pre>

2. Initialize the plugin using the following:

<pre class="coolsyntax"><code class="lang-markup">$.fn.bootstrapDropdownHover();</code></pre>

* * *

Instead of re-inventing the wheel, I strongly advise you to use the plugin [bootstrap-hover-dropdown][1], which is well-maintained by **Cameron Spear**. It takes no longer than 5 min to implement, and you&#8217;ll have a perfect hover dropdown menu for Bootstrap 3.

It&#8217;s pretty easy to get it working:

[zilla\_button url=&#8221;https://github.com/CWSpear/bootstrap-hover-dropdown/archive/master.zip&#8221; style=&#8221;orange&#8221; size=&#8221;medium&#8221; type=&#8221;square&#8221; target=&#8221;\_self&#8221;] Download the plugin [/zilla_button]

  1. Extract `bootstrap-hover-dropdown.min.js` to your /javascript/ folder
  2. Call it after jQuery & Bootstrap

<pre class="coolsyntax"><code class="lang-markup">&lt;!-- script order matters! --&gt;
&lt;script src="/path/to/jquery.min.js"&gt;&lt;/script&gt;
&lt;script src="/path/to/bootstrap.min.js"&gt;&lt;/script&gt;
&lt;script src="/path/to/bootstrap-hover-dropdown.min.js"&gt;&lt;/script&gt;</code></pre>

  1. Initialize the plugin using the following:

<pre class="coolsyntax"><code class="lang-javascript">$('.dropdown-toggle').dropdownHover();</code></pre>

### What&#8217;s your favorite method to make Bootstrap navigation dropdown work on mouseover?

<span style="color: #ff6600;"><strong>Answer in the comments 😉</strong></span>

 [1]: https://github.com/CWSpear/bootstrap-hover-dropdown