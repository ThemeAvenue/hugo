---
title: WordPress Plugin to Ease Mobile Development
author: Julien Liabeuf
layout: post
date: 2014-04-08T03:16:54+00:00
url: /help-mobile-development/
categories:
  - Plugins
  - WordPress
tags:
  - development
  - qr code
  - tool

---
I don&#8217;t know for you, but when I develop a WordPress theme or plugin that needs to be mobile compliant, I check the developmet site quite often from my mobile.

It really becomes annoying when I have to type long URLs like [http://development.dev/my-dev-site/my-test-url-is-so-long][1] on my small mobile&#8217;s keyboard. Yes it&#8217;s doeable, but the time I spend doing this is absolutely unproductive and is annoying as hell.

## Using QR Codes

At one point, I decided that it was too much and that I needed a simpler solution. I browsed the WordPress Extend looking for a plugin that would give me a QR code for my pages, but I couldn&#8217;t find anything that really helped. There are a lot of QR Code plugins on the Extend, but it&#8217;s for front-end use (shortcodes mostly). What I needed was a QR code in the page&#8217;s edit screen.

As nothing came up, I simply made it myself. What I did is nothing fancy and surely not hard to code, but it saves me a lot of tme now when I have to check pages on a mobile.

What the plugin actually does is:

  * Add a metabox in posts / pages edit screen with a QR code that links to this page (front-end),
  * Add a dashboard widget with a QR code that takes you to the site&#8217;s homepage

As I said, nothing fancy but it makes my life a lof easier! You can also add support for custom post types very easily by using the filter `wpaqr_post_types`.

If you want to give this plugin a try, download <a href="http://wordpress.org/plugins/wp-admin-qr-code-generator/" target="_blank">WP Admin QR Code Generator</a> on the WordPress Extend. Also, if you have any suggestion for improvements, I&#8217;ll be happy to hear it! Share it in the comments.

<p style="text-align: center;">
  [zilla_button url=&#8221;http://wordpress.org/plugins/wp-admin-qr-code-generator/&#8221; style=&#8221;orange&#8221; size=&#8221;medium&#8221; type=&#8221;square&#8221; target=&#8221;_blank&#8221;] Download [/zilla_button]
</p>

 [1]: #