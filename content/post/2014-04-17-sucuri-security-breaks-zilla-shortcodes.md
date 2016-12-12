---
title: Sucuri Security breaks Zilla Shortcodes
author: Julien Liabeuf
layout: post
date: 2014-04-17T02:00:49+00:00
url: /sucuri-security-breaks-zilla-shortcodes/
categories:
  - Plugins
  - WordPress
tags:
  - fix
  - issue
  - shortcodes

---
Sucuri Security and Zilla Shortcodes are two plugins we use quite often at ThemeAvenue. We actually use them both on several WordPress sites. But here is the problem: if you use the 1-click hardening, chances are you&#8217;ll break Zilla Shortcodes.

## Why is Zilla Shortcodes Broken?

It is actually quite stupid, and happily very easy to fix.

The problem arises when you harden the `wp-content` folder.

What Sucuri does is add a new `.htaccess` file in your wp-content directory and uses this `.htaccess` to prevent access to all `.php` files. However, Zilla Shortcodes does a direct call to one `.php` file in order to add the shortcodes button in the WordPress editor toolbar.

## How to Fix It

As I said earlier, the fix is very simple.

First, start your FTP client and navigate to `/wp-content/`

Once you&#8217;re there, edit the `.htaccess` file. At the end of this file, add the following 3 lines:

<pre><code class="lang-markup">&lt;Files "popup.php"&gt;
Allow from all
&lt;/Files&gt;</code></pre>

That&#8217;s it! Upload the edited file and the shortcodes button will work again!