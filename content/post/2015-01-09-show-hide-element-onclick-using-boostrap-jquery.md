---
title: 'Show and hide element onclick using Boostrap & jQuery'
author: Julien Vernet
layout: post
date: 2015-01-09T10:57:13+00:00
url: /show-hide-element-onclick-using-boostrap-jquery/
prompt_recipient_ids:
  - 'a:0:{}'
categories:
  - Bootstrap
  - Code Snippets
  - jQuery

---
<p class=" pre-active">
  <em>Boostrap is the most widely used front-end framework. It comes with jQuery, the most famous javascript library. Let&#8217;s achieve something super simple using both.</em>
</p>

<p class=" pre-active">
  If you&#8217;re using <strong>Boostrap 3 and jQuery</strong>, toggling the visibility of an element on click event is dead simple. We rely on two Boostrap classes: <code class="">.show</code> and <code class="">.hide</code> (<a href="http://getbootstrap.com/css/#helper-classes-show-hide">read more</a>).
</p>

Copy and paste the following in your javascript file:

<pre class="coolsyntax"><code class="lang-javascript">$('.toggle').click(function (event) {
	event.preventDefault();
	var target = $(this).attr('href');
	$(target).toggleClass('hidden show');
});</code></pre>

Example markup:

<pre class="coolsyntax pre-active"><code class="lang-markup">&lt;a href="#credits" class="toggle btn btn-primary"&gt;Click on me to reveal the hidden treasure&lt;/a&gt;

&lt;div id="credits" class="well hidden"&gt;
	&lt;h1&gt;I'm the hidden treasure :)&lt;/h1&gt;
	&lt;p&gt;Whilst most Japanese people are aware of English swear words and want to know more, they're not quite sure on how they're used and the role they play.&lt;/p&gt;
	&lt;div class="embed-responsive embed-responsive-16by9"&gt;
		&lt;iframe width="853" height="480" src="//www.youtube.com/embed/T9-OWfS2Vy4" frameborder="0" allowfullscreen&gt;&lt;/iframe&gt;
	&lt;/div&gt;
&lt;/div&gt;</code></pre>

The code is pretty self explanatory, don&#8217;t you think? Anyway, feel free to leave a comment if you&#8217;re struggling with this or if you have suggestions.

### Demo

<http://jsfiddle.net/SiamKreative/7uxyrrkv/>