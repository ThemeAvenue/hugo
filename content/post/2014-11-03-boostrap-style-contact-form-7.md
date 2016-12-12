---
title: Boostrap Style for Contact Form 7
author: Julien Vernet
layout: post
date: 2014-11-03T08:19:22+00:00
url: /boostrap-style-contact-form-7/
categories:
  - Bootstrap
  - WordPress

---
If you also struggled to find a way to properly style Contact Form 7 to look like a Bootstrap form, look no longer. I spent quite some time researching but I never found a satisfactory answer.

Things to bare in mind before we get started:

  * You need to be familiar with the [LESS][1], the CSS pre-processor used by Bootstrap
<li class=" pre-active">
  The <code class="">:not()</code> CSS selector is supported by all latest browsers but not supported in IE8 (<a href="http://caniuse.com/#feat=css-sel3">read more</a>)
</li>
<li class=" pre-active">
  There&#8217;s no point in styling a form created with Contact Form 7 if your theme is not built with Boostrap&#8230;
</li>

## How does it work?

You have two options:

  * Use LESS. The main advantage is that you can style existing forms without editing the form markup
  * Edit the form markup to add Boostrap classes. The main advantage is that you&#8217;re able to change the form layout

### 1) Using LESS

What&#8217;s awesome with LESS and other CSS pre-processors is the flexibility it offers. Variables, mixins and functions are missing ingredients in CSS. Using LESS, I have the ability to &#8220;_apply_&#8221; Bootstrap styles to whatever element **without editing the markup**. I&#8217;m simply going to list all form elements and apply the relevant style:

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/SiamKreative/f6e1075a285b64ac143f">Gist</a>.
  </noscript>
</div>

Then you need to compile it. Performance-wise, it&#8217;s best to `@import` this in your theme&#8217;s main LESS stylesheet. But you can also compile it as a separate CSS file that would need to enqueue.

### 2) Changing the form markup

Compared to the previous, you have even more control on the style and layout. But it can be a pain in the ass if you have a large amount of forms to edit. Therefore, it&#8217;s not as easy to main as the LESS technique.

To create an horizontal form, we would do the following:

<img class="alignnone" src="https://i.imgur.com/UTRRPvU.png" alt="" width="730" height="351" />

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/SiamKreative/dff76d2d1e85fb9d3c9a">Gist</a>.
  </noscript>
</div>

To create a form without label, you can do:

<img class="alignnone" src="https://i.imgur.com/NiEgRDc.png" alt="" width="730" height="281" />

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/SiamKreative/a49611860bc1713a32c6">Gist</a>.
  </noscript>
</div>

### How about a WordPress plugin?

A tiny WordPress plugin could be useful for users who don&#8217;t have knowledge of LESS and simply want to style their Contact forms 7. But hey, we&#8217;re pretty busy at the time, so probably not for now. The plugin should do the following:

  1. Define the color variables using constants
  2. [Compile and cache the LESS stylesheet][2]
  3. Enqueue the compiled stylesheet

 [1]: http://lesscss.org/
 [2]: http://www.tailored4wp.com/how-to-use-less-auto-compiler-in-your-next-wordpress-project-quick-tip-361/