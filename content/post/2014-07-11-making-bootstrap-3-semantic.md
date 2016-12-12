---
title: Making Bootstrap 3 More Semantic
author: Julien Vernet
layout: post
date: 2014-07-11T03:08:18+00:00
url: /making-bootstrap-3-semantic/
categories:
  - Bootstrap

---
If you&#8217;re here, you know that Boostrap 3 is a powerful and flexible front-end framework. But you also know that embedding Bootstrap classes in your HTML is wrong. Sure, Bootstrap <span style="color: #3f4549;">representational</span> classes are easy to use, but what if you want to keep your markup clean?

## 1) Clean your markup

Before:

<pre class="coolsyntax"><code class="lang-markup">&lt;div class="container"&gt;
    &lt;div class="row"&gt;
        &lt;div class="col-lg-8 col-md-8 col-sm-6 col-xs-12"&gt;
            Main content
        &lt;/div&gt;
        &lt;div class="col-lg-4 col-md-4 col-sm-6 col-xs-12"&gt;
            Sidebar
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/div&gt;</code></pre>

After:

<pre class="coolsyntax"><code class="lang-markup">&lt;div class="container"&gt;	
	&lt;div class="introduction"&gt;
		&lt;section role="main"&gt;
			Main content
		&lt;/section&gt;
		&lt;aside role="complementary"&gt;
			Sidebar
		&lt;/aside&gt;
	&lt;/div&gt;
&lt;/div&gt;</code></pre>

## 2) Using LESS to import Bootstrap core

Bootstrap 3 is built with LESS, a CSS preprocessor written in javascript. To unlock super powers, simply do:

  1. Create your own LESS stylesheet, let&#8217;s say **style.less**
  2. Import Bootstrap LESS files (all of them or individually if you don&#8217;t want to use all components)

<pre class="coolsyntax"><code class="lang-css">// Import all Boostrap
@import "assets/bower_components/bootstrap/less/bootstrap.less";

// Or import components individually (for instance only grid and buttons):
@import "assets/bower_components/bootstrap/less/variables.less";
@import "assets/bower_components/bootstrap/less/mixins.less";
@import "assets/bower_components/bootstrap/less/grid.less";
@import "assets/bower_components/bootstrap/less/buttons.less";
</code></pre>

Importing components individually gives you the opportunity to **use only what you need**. This means the resulting CSS file could be drastically smaller.

I recommend using [Prepros][1] to compile LESS stylesheets into CSS. The built-in live-reload is particularly handy.

## 3) Structure the code using Bootstrap Mixins

If you now take a look at your page, you&#8217;ll see that it has no style&#8230; the grid isn&#8217;t a grid anymore. So how to &#8220;restore&#8221; the way it looked? Mixins to the rescue!

First let&#8217;s create a handy mixin that helps playing with columns:

<pre class="coolsyntax"><code class="lang-markup">make-column(@large, @medium, @small, @tiny: 16) {
	.make-xs-column(@tiny);
	.make-sm-column(@small);
	.make-md-column(@medium);
	.make-lg-column(@large);
}</code></pre>

Then you would do the following:

<pre class="coolsyntax"><code class="lang-css">.introduction {
	.make-row();
}
[role="main"] {
	.make-column(8,8,6,12);
}
[role="complementary"] {
	.make-column(4,4,6,12);
}</code></pre>

### Why should I care about semantic?

Making your Bootstrap code more readable for Search Engine bots (Google Bot for instance) will definitely help your SEO. But as this technique uses LESS, it also gives you more flexibility for styling elements. For instance, using variables or using anything Bootstrap mixins.

### When should I use this technique?

Wondering when it&#8217;s worth spending time on this? In my opinion, this concept only applies to small sites.

For larger sites or web apps, I do not recommend using it as it&#8217;ll be a headache to maintain and the resulting CSS files will be bigger. I think it makes sense to use Bootstrap components if your project is big enough to raise concerns about maintainability.

##### Sources and inspiration:

  * [Bootstrap without all the debt][2]
  * [Using Bootstrap the Right (Semantic) Way][3]
  * [Please stop embedding Bootstrap classes in your HTML!][4]
  * [Semantic UI][5]

 [1]: http://alphapixels.com/prepros/
 [2]: https://coderwall.com/p/wixovg
 [3]: http://www.ostraining.com/blog/coding/bootstrap-right-way/
 [4]: http://ruby.bvision.com/blog/please-stop-embedding-bootstrap-classes-in-your-html
 [5]: http://semantic-ui.com/