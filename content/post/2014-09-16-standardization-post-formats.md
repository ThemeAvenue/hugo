---
title: For Standardization of Post Formats
author: Julien Liabeuf
layout: post
date: 2014-09-16T09:10:03+00:00
url: /standardization-post-formats/
categories:
  - Thoughts
  - WordPress
tags:
  - post formats
  - standardization
  - user experience

---
One of the projects we are working on lately at ThemeAvenue involves post formats.

I have been thinking a lot about those lately. I have also discussed it with a few fellow WordPress developers. I know there is a &#8220;heavy&#8221; history behind post formats. Lots of talks about how it should work, sudden withdrawal from WordPress 3.6&#8230;

Yet, the post formats are still present in the latest version of WP, and it is not easy to use them.

## No Standard, No Portability

Actually, it is quite easy to use post formats. What is not easy, or even impossible for the end-user, is to keep its content from theme to theme. Most of the themes using them are creating different techniques to work with post formats data.

This leads to two huge problems:

  1. Impossible to keep the content when changing the theme,
  2. Users _never_ know how those damn post formats work

In the end, this complexity and loss of data is imputed to WordPress, which nobody in the community wants. But why does it have to be this way?

Post formats are great. It allows for a wide variety of content to be displayed in the best possible way. It also make reading a blog more pleasant as the archive page is a lot less boring. How difficult would it be to try and define a standard way of using post formats? There is no technical challenge, it&#8217;s just a matter of decision.

## Content vs Custom Fields

There are two fundamental ways of handling post formats data:

  1. The post content,
  2. Post metas

Both solutions have their pros and cons.

At the beginning of my reflection, I was more into the first solution. The main reason why solution 1 is good is because if all the data is saved in the content, then nothing is lost if the theme is changed.

However, the main drawback of this solution is that is requires a lot more data processing as the content and the format-specific data are mixed all together.

Solution 2 seemed less appealing to me at first. It would obviously make the data processing a lot easier, but keeping all data in the content seemed so much more interesting.

Then, I started to think more about _standardization_. If we could reach a community-driven standard, then using post metas would no more be a problem.

However, the real reason that made me change my mind is what my partner [Julien][1] brought to my attention: **user experience**.

Let&#8217;s imagine everything is saved in the content. How on earth is the user supposed to know how to structure his data to make the format of his choice work correctly?<figure id="attachment_650" style="width: 600px" class="wp-caption aligncenter">

<img class="size-large wp-image-650" src="https://themeavenue.net/wp-content/uploads/2014/09/link-post-format-messy-1024x596.png" alt="What the hell do I have to do?" width="600" height="349" srcset="http://themeavenue.dev/wp-content/uploads/2014/09/link-post-format-messy-1024x596.png 1024w, http://themeavenue.dev/wp-content/uploads/2014/09/link-post-format-messy-300x175.png 300w, http://themeavenue.dev/wp-content/uploads/2014/09/link-post-format-messy-768x447.png 768w, http://themeavenue.dev/wp-content/uploads/2014/09/link-post-format-messy.png 1355w" sizes="(max-width: 600px) 100vw, 600px" /><figcaption class="wp-caption-text">What the hell do I have to do?</figcaption></figure> 

Video, audio, chat, quote, link, gallery&#8230; Those are very different data types, and it is far from easy to guess how it&#8217;s supposed to be handled.

Now, by using post metas and metaboxes, we can greatly improve the user experience by explicitly prompting the user to enter his data in specific (and well labeled) fields. Instead of guessing _&#8220;where should the link URL be pasted&#8221;_, the user is _asked_ to paste the URL in a specific box. Can you see the difference?<figure id="attachment_651" style="width: 600px" class="wp-caption aligncenter">

<img class="size-large wp-image-651" src="https://themeavenue.net/wp-content/uploads/2014/09/link-post-format-1024x596.png" alt="Easy as pie to add a link." width="600" height="349" srcset="http://themeavenue.dev/wp-content/uploads/2014/09/link-post-format-1024x596.png 1024w, http://themeavenue.dev/wp-content/uploads/2014/09/link-post-format-300x175.png 300w, http://themeavenue.dev/wp-content/uploads/2014/09/link-post-format-768x447.png 768w, http://themeavenue.dev/wp-content/uploads/2014/09/link-post-format.png 1355w" sizes="(max-width: 600px) 100vw, 600px" /><figcaption class="wp-caption-text">Easy as pie to add a link.</figcaption></figure> 

## The Necessity of Standardizing

Post format are a great, but also greatly under exploited. It was designed as a standard for content types, but it went only half way by standardizing the front-end part and completely neglecting the data handling.

If no standard is set, post formats will never be able to take off to their full potential. Firstly because the users don&#8217;t want to use them, secondly because developers and designers don&#8217;t express their creativity fully on this feature.

So, how about a standardization for post formats data? Do you think it&#8217;s a necessary step? Are you willing to step-in?

 [1]: https://themeavenue.net/author/julienv/