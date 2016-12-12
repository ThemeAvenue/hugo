---
title: 'Behavior Flow: Speed Up Your WordPress Site'
author: Julien Liabeuf
layout: post
date: 2015-09-11T13:31:29+00:00
excerpt: Are you a performance nuts? Are you trying to implement every single trick in the book to speed up your WordPress site? Here is one more...
url: /behavior-flow-faster-wordpress/
prompt_recipient_ids:
  - 'a:0:{}'
categories:
  - Behavior Flow
  - Plugins
tags:
  - analytics
  - conversion
  - e-commerce
  - ux

---
Are you a performance nuts? Are you trying to implement every single trick in the book to speed up your WordPress site? Here is one more&#8230;

## Page Pre-rendering

There is a technique called <a href="https://www.chromium.org/developers/design-documents/prerender" target="_blank">page pre-rendering</a> that&#8217;s been introduced a couple of years ago now.

What page pre-rendering does is tell the browser (we&#8217;re talking Chrome and Firefox here) what page the visitor will load next. The browser will then pre-load this page in the background. The result is a super-fast loading of the next page when the visitor clicks a link to view it.

Here is an example of Google implementing page pre-rendering in its search engine (it&#8217;s called Instant Pages).



The same thing can be done within your site.

Of course, there is the good and the bad for such a technology.

<div class="row-fluid">
  <div class="span6 rhcol">
    <h3>
      <span style="color: #339966;">The Good</span>
    </h3>
    
    <ul>
      <li>
        <span style="color: #339966;">Super fast page load</span>
      </li>
      <li>
        <span style="color: #339966;">Better user experience</span>
      </li>
      <li>
        <span style="color: #339966;">Better conversion rate</span>
      </li>
      <li>
        <span style="color: #339966;">Etc</span>
      </li>
    </ul>
  </div>
  
  <div class="span6 rhcol">
    <h3>
      <span style="color: #993300;">The Bad</span>
    </h3>
    
    <ul>
      <li>
        <span style="color: #993300;">Increases server load</span>
      </li>
      <li>
        <span style="color: #993300;">Pre-loading a page that might not be the next one for some visitors</span>
      </li>
    </ul>
  </div>
</div>

This means that pre-rendering can be a very efficient technique but it can&#8217;t be applied blindly. It has to be done on a case-by-case basis and not in a global, inefficient way.

## Behavior Flow

The way to take fully advantage of page pre-rendering is to set it up page by page. It needs to be accurately defined. You don&#8217;t need to use this technique on every single page of your site. Some pages are just too general and aren&#8217;t made to lead to a specific action. This means the visitor could land anywhere on your site.

Page pre-rendering is tightly linked to behavior flow, and subsequently to conversion rate optimization. It all starts with a strategy: you want to take your visitor on page X, then convince him to view page Y to finally guide him to your final goal: a purchase, an opt-in e-mail, etc.

When your strategy is ready and the page flow is done, you&#8217;re ready to implement pre-rendering. Obviously, it will follow the above path: page X > page Y > Page Z (final goal).

What you want to do is set page X to tell the browser to pre-load page Y. Then set page Y to tell the browser to pre-load page Z.

This will result in an extremely fast conversion funnel. And we all know how important page load time is.

## The Behavior Flow WordPress Plugin

Because we wanted to implement page pre-rendering on our site <a href="https://getaweosmesupport.com" target="_blank">Awesome Support</a>, we checked existing possibilities.

Of course, the first option is to set the pre-rendering meta tags manually. However, if you want to create an optimized funnel, this is not the way to go.

The other option is a WordPress plugin. There are a couple of WP plugins for that but none of them are actually made for defining a real strategy. What they offer is a way to _globally_ pre-load pages on the site, without the ability to go page by page, which is a big strategic mistake from our point of view.

For that reason, we got started on developing a tiny plugin that does just that: add page pre-rendering on a page by page basis. The plugin is simply called <a href="https://github.com/ThemeAvenue/Behavior-Flow" target="_blank">Behavior Flow</a> and is maintained on GitHub.<figure id="attachment_816" style="width: 600px" class="wp-caption aligncenter">

<img class="wp-image-816 size-large" src="https://themeavenue.net/wp-content/uploads/2015/09/Behavior-Flow-GitHub-1024x671.png" alt="Behavior-Flow-GitHub" width="600" height="393" srcset="http://themeavenue.dev/wp-content/uploads/2015/09/Behavior-Flow-GitHub-1024x671.png 1024w, http://themeavenue.dev/wp-content/uploads/2015/09/Behavior-Flow-GitHub-300x197.png 300w, http://themeavenue.dev/wp-content/uploads/2015/09/Behavior-Flow-GitHub-768x503.png 768w, http://themeavenue.dev/wp-content/uploads/2015/09/Behavior-Flow-GitHub.png 1196w" sizes="(max-width: 600px) 100vw, 600px" /><figcaption class="wp-caption-text">Behavior Flow GitHub Repository</figcaption></figure> 

## Optimal Setup

In order to setup Behavior Flow in an optimal way you need two things:

  1. Have a conversion funnel strategy as explained above
  2. Backup this strategy with data

Point 1 is entirely up to you. Point 2 is not.

In order to get data to verify your strategy, Google Analytics is your best friend.

Log in your Analytics account and go to _Behavior > Behavior Flow_ ( sounds familiar? 😉 ). This screen will give you the data you need.<figure style="width: 1920px" class="wp-caption aligncenter">

[<img class="" src="https://cloud.githubusercontent.com/assets/1778633/9759982/611df35c-571b-11e5-889d-1f48e46f6b52.png" alt="Google Analytics Behavior Flow" width="1920" height="1075" />][1]<figcaption class="wp-caption-text">Google Analytics Behavior Flow</figcaption></figure> 

Once you have confirmed the efficiency of your funnel, install <a href="https://wordpress.org/plugins/behavior-flow/" target="_blank">Behavior Flow</a> on your WordPress site.

After you activated the plugin, a new metabox will appear in your pages, posts and custom post types edit screen. The metabox will allow you to select what the next page is from the page you&#8217;re editing.<figure style="width: 1372px" class="wp-caption aligncenter">

<img class="" src="https://cloud.githubusercontent.com/assets/1778633/9760084/24dd10d4-571c-11e5-83a4-25e230894620.png" alt="Behavior Flow Metabox" width="1372" height="802" /><figcaption class="wp-caption-text">Behavior Flow Metabox</figcaption></figure> 

For the scenario described above, you would do the following:

  * Edit page X and set page Y as the next page
  * Edit page Y and set page Z as the next page

That&#8217;s it. You now have a super optimized conversion funnel!

 [1]: https://cloud.githubusercontent.com/assets/1778633/9759982/611df35c-571b-11e5-889d-1f48e46f6b52.png