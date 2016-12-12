---
title: Using WordPress.org Plugin Reviews
author: Julien Liabeuf
layout: post
date: 2015-06-04T08:59:25+00:00
url: /wordpress-extend-plugin-reviews/
prompt_recipient_ids:
  - 'a:0:{}'
categories:
  - Plugin Reviews
  - Plugins
tags:
  - promotion
  - social proof
  - testimonial

---
So you&#8217;re a developer and you have a couple of plugins available on the WordPress Plugins Repository. You&#8217;re trying to promote those plugins and maybe you even have a dedicated site for some of them.

We all know that one of the strongest ways to promote a product or service is social proof. If a prospective customer / user sees 10, 20 or 100 people using your product and recommending it, it has a very powerful convincing effect. It&#8217;s worth much more than you saying _&#8220;it&#8217;s great! you should use it!&#8221;_.

WordPress Extend does provide a review system where users can rate your plugin on a scale from 1 to 5, and leave a comment explaining why your plugin is so awesome (or not&#8230;). What if you could re-use those testimonials as social proof on your own site? Guess what, you can.

## Get Reviews From WordPress.org

We pushed a brand new plugin today on the WordPress Extend that&#8217;s called <a href="https://wordpress.org/plugins/plugin-reviews/" target="_blank">Plugin Reviews</a>. What this plugin does is query WordPress&#8217; servers to retrieve the reviews of your plugin. It will then display those reviews in a grid layout or using a carousel.<figure id="attachment_786" style="width: 600px" class="wp-caption aligncenter">

<img class="size-large wp-image-786" src="https://themeavenue.net/wp-content/uploads/2015/06/plugin-reviews-1024x546.png" alt="Plugin Reviews on WordPress.org" width="600" height="320" srcset="http://themeavenue.dev/wp-content/uploads/2015/06/plugin-reviews-1024x546.png 1024w, http://themeavenue.dev/wp-content/uploads/2015/06/plugin-reviews-300x160.png 300w, http://themeavenue.dev/wp-content/uploads/2015/06/plugin-reviews-768x409.png 768w, http://themeavenue.dev/wp-content/uploads/2015/06/plugin-reviews.png 1366w" sizes="(max-width: 600px) 100vw, 600px" /><figcaption class="wp-caption-text">Plugin Reviews on WordPress.org</figcaption></figure> 

<p class=" pre-active">
  The plugin is really simple to use. There is no option page, no general settings whatsoever. The one and only thing you need is to use the shortcode <code class="">[wr_reviews]</code>.
</p>

<p class=" pre-active">
  This shortcode has 12 options, with only one mandatory: the slug of the plugin you want to get the reviews from. The rest is optional. The available parameters will allow you to choose the layout (grid or carousel), the number of reviews to show, the minimum rating and much more. The list of <a href="https://github.com/ThemeAvenue/Plugin-Reviews/wiki/Shortcode-Attributes" target="_blank">all parameters can be seen on the wiki page</a>.
</p>

## What It Looks Like {.pre-active}

<p class=" pre-active">
  The reason why we developed this plugin is for our own needs. We wanted to showcase user reviews for our <a href="http://getawesomesupport.com">WordPress support plugin</a> Awesome Support. After we completed the development we decided to submit it to the Extend and here is it now.
</p>

<p class=" pre-active">
  If you want to see what it looks like, you can check out our reviews page here: <a href="https://getawesomesupport.com/reviews/" target="_blank">https://getawesomesupport.com/reviews/</a>
</p><figure id="attachment_793" style="width: 600px" class="wp-caption aligncenter">

<img class="size-large wp-image-793" src="https://themeavenue.net/wp-content/uploads/2015/06/plugin-reviews-demo-1024x546.png" alt="Plugin Reviews for Awesome Support" width="600" height="320" srcset="http://themeavenue.dev/wp-content/uploads/2015/06/plugin-reviews-demo-1024x546.png 1024w, http://themeavenue.dev/wp-content/uploads/2015/06/plugin-reviews-demo-300x160.png 300w, http://themeavenue.dev/wp-content/uploads/2015/06/plugin-reviews-demo-768x409.png 768w, http://themeavenue.dev/wp-content/uploads/2015/06/plugin-reviews-demo.png 1366w" sizes="(max-width: 600px) 100vw, 600px" /><figcaption class="wp-caption-text">Plugin Reviews for Awesome Support</figcaption></figure> 

## What&#8217;s Next? {.pre-active}

<p class=" pre-active">
  This plugin is not at all a priority for us. It&#8217;s just a side project that we wanted to share. We will of course maintain it. It&#8217;s quite a small plugin and doesn&#8217;t require lots of work. If bugs arise we will fix them, we will probably add a couple of functions too, but we do not plan to work on it continuously. If you have ideas and want to contribute (pull requests are welcome), please head over to our <a href="https://github.com/ThemeAvenue/Plugin-Reviews" target="_blank">GitHub repo</a>.
</p>