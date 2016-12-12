---
title: Why you should be using Schema.org with WordPress
author: Julien Vernet
layout: post
date: 2014-04-15T06:06:15+00:00
excerpt: 'Microdatas consist of particular HTML statements used to provide additional information to the search engines. It can result, among other things, in having rich snippets.  Here is how you can implement it in your site and increase your click through rate.'
url: /wordpress-microdata-schema-org/
suevafree_template:
  - full
inspiration:
  - http://wp-buddy.com/products/themes/schema-org-wordpress-theme/
categories:
  - Web Development
  - WordPress
format: quote

---
### 1) What is Schema.org?

[Schema.org][1] is one type of <a href="http://en.wikipedia.org/wiki/Microdata_(HTML)" target="_blank">Microdata</a>. Microdata is a synonym for particular HTML statements. It can be embedded into HTML to provide additional information to the search engines. It can result, among other things, in having rich snippets.

### 2) What are rich snippets?

Rich snippets are the result of the microdata implementation.

[<img class="alignnone size-full wp-image-368" alt="rich-snippets" src="https://themeavenue.net/wp-content/uploads/2014/04/rich-snippets.jpg" width="680" height="394" srcset="http://themeavenue.dev/wp-content/uploads/2014/04/rich-snippets.jpg 680w, http://themeavenue.dev/wp-content/uploads/2014/04/rich-snippets-300x174.jpg 300w" sizes="(max-width: 680px) 100vw, 680px" />][2]

## When to use Schema.org in a WordPress theme?

Implementing microdatas on a WordPress site can take some time, so if your site is getting only a few hits a month, it&#8217;s probably not worth it. Build your traffic first, and then your pages are well indexed on Google, it&#8217;s time to stand out from the crowd.

Having rich snippets is especially useful when your WordPress site has several custom fields. For instance, on a real estate site, you might want to highlight the price and number of rooms. On an e-commerce site, you might want to show ratings and if the product is in stock.

### I want to use schema.org, how to get started?

There is pretty much two options:

  1. Use a plugin such as [Schema Creator by Raven][3] or [All In One Schema.org Rich Snippets][4]
  2. The DIY method: code it directly in your theme

The first option is most-likely suitable if you&#8217;re using a paid/free WordPress theme. If you&#8217;re a developer, you could of course implement microdatas using a child-theme; but in my opinion it can get messy. Follow [this tutorial][5] if you want to use **Schema Creator by Raven**.

The second option is designed for theme developers. The main advantage over the first one is that you have a better control of the markup, and it saves you from installing yet-another-plugin. Promoting microdatas to your clients is also good way to impress them and close deals. Not mentioning it to a potential e-commerce client would be such a shame, especially knowing that [basic implementation with WooCommerce take less than a minute][6].

**Preview and test micro-datas**

But hey, what if I want to check how the search result page will look like with rich snippets? Google offers a [Rich Snippet Testing tool][7] to review and test the micro data in your pages and posts. Simply past the URL of the post in which you inserted schematic data and click _Preview._

### How can I be sure that the rich snippets will show up?

Unfortunately, you can&#8217;t. Google is the one making the decision whether to show rich snippets or not on your search results. However, if correctly implemented, there is no reason for Google not to show it in the SERP. You&#8217;d really miss something if you passed your way on this.

 [1]: http://schema.org/
 [2]: https://themeavenue.net/wp-content/uploads/2014/04/rich-snippets.jpg
 [3]: https://wordpress.org/plugins/schema-creator/
 [4]: http://wordpress.org/plugins/all-in-one-schemaorg-rich-snippets/
 [5]: http://wpsites.net/seo/schema-microdata-wordpress-plugin/
 [6]: http://www.primathemes.com/documentation/woocommerce-fix-google-rich-snippet-for-on-sale-product/
 [7]: http://www.google.com/webmasters/tools/richsnippets/