---
title: The problem of duplicate data-uris in CSS
author: Julien Vernet
layout: post
date: 2015-01-29T02:44:40+00:00
url: /problem-duplicate-data-uris-css/
categories:
  - Code Snippets
  - Web Performance
tags:
  - base64
  - css
  - data-uri
  - less
  - pagespeed
  - performance
  - stylesheet

---
In a recent project, I decided to use data-URIs for small images to save a few HTTP requests. I&#8217;d like to use the same base64 encoded image multiple times in my CSS. But as a performance-concerned developer, I know it will drastically increase my stylesheet&#8217;s weight. And I don&#8217;t like that idea.

### So what to do about duplicate data-URIs in CSS?

  1. Forget about it. Let GZIP do the work for you. [Read this great article][1]
  2. Group all selectors and use the data-URI only once. This is as easy as pie if you&#8217;re using LESS.
  3. Use a single class just for the background and adjust your markup accordingly. We don&#8217;t really want to be doing this, as this requires to add this additional class where you want to use the data-URI.

As the first solution is brilliantly covered by Martin Sutherland on his blog, I&#8217;m not going to explore it. Instead, I will detail the second solution.

So let&#8217;s we want to apply the same background image 3 times. So we write:

<pre class="coolsyntax"><code class="lang-css">/* This LESS code */
.header {background: data-uri('image/png;base64', 'images/background.png');}
.sidebar {background: data-uri('image/png;base64', 'images/background.png');}
.footer {background: data-uri('image/png;base64', 'images/background.png');}

/* Will compile into this CSS */
.header,
.sidebar,
.footer {background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAMAAAAyCAYAAACZDmG3AAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccl.../+pXgEGAH6HlYzJaNxNAAAAAElFTkSuQmCC) };</code></pre>

What are the advantages of using LESS you ask me? It&#8217;s more flexible and easier to maintain. You don&#8217;t have group all 3 selectors manually (LESS will do it for you), which helps you organize you stylesheet the way you want. And, you don&#8217;t have manually generate the data-URI using tools like [duri.me][2].

#### Useful links about using data-URIs with LESS

  * [LESS Misc functions: Data-URI][3]
  * [Embedding Images As Base64-Encoded Data URIs Using Less CSS][4]

 [1]: https://sunpig.com/martin/2011/02/21/some-notes-on-duplicate-data-uris-in-CSS/
 [2]: http://duri.me/
 [3]: http://lesscss.org/functions/#misc-functions-data-uri
 [4]: http://www.bennadel.com/blog/2649-embedding-images-as-base64-encoded-data-uris-using-less-css.htm