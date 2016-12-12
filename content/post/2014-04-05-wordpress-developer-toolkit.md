---
title: WordPress Developer Toolkit
author: Julien Liabeuf
layout: post
date: 2014-04-05T02:48:54+00:00
url: /wordpress-developer-toolkit/
suevafree_template:
  - full
categories:
  - WordPress
tags:
  - development
  - test
  - tools
  - workfow

---
How many _&#8220;10 Best WordPress Plugins&#8221;_ or _&#8220;Must Have WordPress Plugins&#8221;_ articles have you seen? A lot right? It&#8217;s everything for the users. What about developers?

There is a number of plugins I always use while developing a theme or plugin. Some of them saved me a lot of time and I can&#8217;t develop without it anymore. I thought it could be a good idea to share my list&#8230;

### WordPress Beta Tester

I always test my themes and plugins on the latest versions of WordPress. I use this plugin with the &#8220;Bleeding edge&#8221; option to be able to identify and fix blocking points with future WordPress version at an early stage of the development.

<a href="http://wordpress.org/plugins/wordpress-beta-tester/" target="_blank">http://wordpress.org/plugins/wordpress-beta-tester/</a>

### WP Optimize

Especially when testing, the database can get very messy. It&#8217;s been a while I&#8217;ve been using this plugin and I saw their number of Facebook fans grow like crazy. They keep updating it and adding new features.

<a href="http://wordpress.org/plugins/wp-optimize/" target="_blank">http://wordpress.org/plugins/wp-optimize/</a>

### Query Monitor

This is the holy grail of WordPress debugging plugins. The amout of useful info it provide is gigantic, the integration is very well done. They even offer you to setup a cookie that will allow you to see the debug info when logged-out. Very useful when testing views as a regular visitor.

<a href="https://github.com/johnbillion/query-monitor" target="_blank">https://github.com/johnbillion/query-monitor</a>

### WordPress Database Reset

This plugin is probably the one which saved me the most time. I do love it! While testing an install process, it makes your life beautifully simple! I used to drop my database tables and quickly re-install WP, but it&#8217;s a real pain with time. With this plugin, one click will reset your database to &#8220;factory state&#8221;, but still re-creates your admin user. Basically, one click and you&#8217;re in a &#8220;freshly installed&#8221; WordPress site.

<a href="http://wordpress.org/plugins/wordpress-database-reset/" target="_blank">http://wordpress.org/plugins/wordpress-database-reset/</a>

### WP Crontrol

I used to install other WP cron debugging plugins, but this one really brings value to developers. The timestamps are accurate, which is not the case in all similar plugins, you can run / delete registered tasks, and it tells you when something prevents WP cron from working. This can potentially save you a lot of time.

<a href="http://wordpress.org/plugins/wp-crontrol/" target="_blank">http://wordpress.org/plugins/wp-crontrol/</a>

### WP Test

Finally, even if it&#8217;s not strictly a WordPress plugin, I wanted to add WP Test. I used to import the <a href="http://codex.wordpress.org/Theme_Unit_Test" target="_blank">WordPress Unit Test</a> data for theme testing, but then I switched to WP Test.io It is based on the WordPress Unit Test with some extra scenarios based on _&#8220;three years of leading quality, support, and testing for 8BIT, which has uncovered some corner cases in the way people use WordPress&#8221;_, Michael Novotny says.

<a href="http://wptest.io/" target="_blank">http://wptest.io/</a>

### WP Admin QR Code Generator

This plugin is a bit special as I am the developer.

What it does is very simple: it adds a metabox in the post edit screen with a QR code linking to the front-end view. Why? Because I was tired of manually typing the long URLs of my development install on the small keyboard of my mobile. When you have to test pages on mobiles during development, this can save you a lot of time.

<a href="http://wordpress.org/plugins/wp-admin-qr-code-generator/" target="_blank">http://wordpress.org/plugins/wp-admin-qr-code-generator/</a>

That&#8217;s it for me. Of course I&#8217;m always looking for new, better tools and processes. If you have tips you wanna share that make you life as a WP developer easies, please share it in the comments.