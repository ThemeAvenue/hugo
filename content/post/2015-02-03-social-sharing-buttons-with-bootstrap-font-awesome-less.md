---
title: Social Sharing Buttons with Bootstrap, Font Awesome and LESS
author: Julien Vernet
layout: post
date: 2015-02-03T04:21:07+00:00
url: /social-sharing-buttons-with-bootstrap-font-awesome-less/
categories:
  - Bootstrap
  - Code Snippets

---
In a recent project, my client asked me to create some sort of a &#8220;Share to a friend feature&#8221;. She initially had in mind an email form but it wasn&#8217;t hard to convince her that Social Media is the way to go as of 2015. So I googled &#8220;**social buttons**&#8221; or &#8220;**social sharing buttons**&#8220;, and I stumble upon [AddThis][1], [AddToAny][2] and its siblings.

Some of these social media sharing services might have great features, but I felt like all these where overkill for what I was trying to achieve. And as a performance-concerned developer, I&#8217;m aware that most will most likely load their own CSS & Javascript; and I&#8217;m not happy with this. As a result, I decided to code my own **social sharing buttons using Boostrap, Font Awesome and LESS**.

[zilla\_button url=&#8221;http://themeavenue.github.io/Boostrap-Social-Buttons/&#8221; style=&#8221;orange&#8221; size=&#8221;medium&#8221; type=&#8221;square&#8221; target=&#8221;\_blank&#8221;] Demo [/zilla\_button] [zilla\_button url=&#8221;https://github.com/ThemeAvenue/Boostrap-Social-Buttons/archive/master.zip&#8221; style=&#8221;black&#8221; size=&#8221;medium&#8221; type=&#8221;square&#8221; target=&#8221;\_blank&#8221;] Download [/zilla\_button]

In this quick tutorial, we will be using:

  * The latest version of [Twitter Boostrap][3] (downloaded using Bower).
  * A custom [FontAwesome][4] package (only with the social icons I&#8217;m actually going to use). I used [fontello][5] to achieve this.
  * LESS, the pre-processing language that Boostrap uses

First thing&#8217;s first, let&#8217;s prepare our HTML markup. Each social media has a different sharing link.

<pre class="coolsyntax"><code class="lang-markup">&lt;div class="ssb"&gt;
	&lt;!-- Twitter --&gt;
	&lt;a href="http://twitter.com/home?status=http://example.com/" title="Share on Twitter" target="_blank" class="btn btn-twitter"&gt;&lt;i class="fa fa-twitter"&gt;&lt;/i&gt; Twitter&lt;/a&gt;
	&lt;!-- Facebook --&gt;
	&lt;a href="https://www.facebook.com/sharer/sharer.php?u=http://example.com/" title="Share on Facebook" target="_blank" class="btn btn-facebook"&gt;&lt;i class="fa fa-facebook"&gt;&lt;/i&gt; Facebook&lt;/a&gt;
	&lt;!-- Google+ --&gt;
	&lt;a href="https://plus.google.com/share?url=http://example.com/" title="Share on Google+" target="_blank" class="btn btn-googleplus"&gt;&lt;i class="fa fa-google-plus"&gt;&lt;/i&gt; Google+&lt;/a&gt;
	&lt;!-- StumbleUpon --&gt;
	&lt;a href="http://www.stumbleupon.com/submit?url=http://example.com/" title="Share on StumbleUpon" target="_blank" data-placement="top" class="btn btn-stumbleupon"&gt;&lt;i class="fa fa-stumbleupon"&gt;&lt;/i&gt; Stumbleupon&lt;/a&gt;
	&lt;!-- LinkedIn --&gt;
	&lt;a href="http://www.linkedin.com/shareArticle?mini=true&amp;url=&amp;title=&amp;summary=http://example.com/" title="Share on LinkedIn" target="_blank" class="btn btn-linkedin"&gt;&lt;i class="fa fa-linkedin"&gt;&lt;/i&gt; LinkedIn&lt;/a&gt;
&lt;/div&gt;</code></pre>

<p class=" pre-active">
  Once the markup is ready, we need to style it. And as you&#8217;re using Twitter Boostrap with LESS, you should be aware that there is a handful of LESS mixins that you can use. So I looked into <code class="">bootstrap/less/mixins/buttons.less</code> and I was glad to find a great mixin for creating button variants. <em>Actually, it wasn&#8217;t just a guess, I knew there was going to be one.</em>
</p>

<pre class="coolsyntax"><code class="lang-css">/* We define our variables (the social brand colors) */
@social-btn-color: white;
@social-brand-twitter: #00acee;
@social-brand-facebook: #3b5998;
@social-brand-googleplus: #e93f2e;
@social-brand-stumbleupon: #f74425;
@social-brand-linkedin: #0e76a8;

.ssb {
	font-size: 0px; /* Remove the additional margin due to inline-block */
	.btn {
		font-size: @font-size-base; /* Reset to default font-size */
		margin: 5px; /* Adjust spacing */
		transition: background-color .25s ease; /* Add some fading */
		border-radius: 0px; /* We want square buttons */
	}
}

/* To create buttons, we use the button mixin provided by Boostrap */
.btn-twitter {
	.button-variant(@social-btn-color; @social-brand-twitter; @social-brand-twitter;);
}
.btn-facebook {
	.button-variant(@social-btn-color; @social-brand-facebook; @social-brand-facebook;);
}
.btn-googleplus {
	.button-variant(@social-btn-color; @social-brand-googleplus; @social-brand-googleplus;);
}
.btn-stumbleupon {
	.button-variant(@social-btn-color; @social-brand-stumbleupon; @social-brand-stumbleupon;);
}
.btn-linkedin {
	.button-variant(@social-btn-color; @social-brand-linkedin; @social-brand-linkedin;);
}</code></pre>

That&#8217;s it. We&#8217;re done 🙂

[zilla\_button url=&#8221;http://themeavenue.github.io/Boostrap-Social-Buttons/&#8221; style=&#8221;orange&#8221; size=&#8221;medium&#8221; type=&#8221;square&#8221; target=&#8221;\_blank&#8221;] Demo [/zilla\_button] [zilla\_button url=&#8221;https://github.com/ThemeAvenue/Boostrap-Social-Buttons/archive/master.zip&#8221; style=&#8221;black&#8221; size=&#8221;medium&#8221; type=&#8221;square&#8221; target=&#8221;\_blank&#8221;] Download [/zilla\_button]

 [1]: http://www.addthis.com/
 [2]: https://www.addtoany.com/
 [3]: http://getbootstrap.com/
 [4]: http://fontawesome.io/
 [5]: http://fontello.com/