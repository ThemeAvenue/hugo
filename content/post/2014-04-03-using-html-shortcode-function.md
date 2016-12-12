---
title: Using HTML in a Shortcode
author: Julien Liabeuf
layout: post
date: 2014-04-03T02:33:58+00:00
url: /using-html-shortcode-function/
suevafree_template:
  - full
categories:
  - Code Snippets
  - WordPress
tags:
  - html
  - shortcode

---
Sometimes using HTML in a shortcode can make your life a lot easier. The problem is: you can&#8217;t. Or at least not without this simple trick.

## Shortcode Outputs Before the Content

That&#8217;s a very common issue. It sometimes happen with themes or plugins. You add a shortcode in your page, and the shortcode&#8217;s content appears at the top of your page, before everything else.

That is because the shortcode echoes some data. A shortcode should **never** echo data but return it instead.

So what if you really want to add HTML?

## Using the Output Buffering

PHP offers a very useful feature: <a href="http://www.php.net/manual/en/function.ob-start.php" target="_blank">output buffering</a>. Thanks to this, we can buffer any HTML content and then return it at the end of the function. Here is an example:

<pre><code class="lang-php">add_shortcode( 'shortcode', 'my_custom_shortcode' );
/**
 * Custom shortcode with HTML
 */
function my_custom_shortcode( $atts ) {

	/* Turn on buffering */
	ob_start(); ?&gt;

	&lt;div&gt;
		&lt;h1&gt;Test&lt;/h1&gt;
		&lt;p&gt;My content&lt;/p&gt;
	&lt;/div&gt;

	&lt;?php
	/* Get the buffered content into a var */
	$sc = ob_get_contents();

	/* Clean buffer */
	ob_end_clean();

	/* Return the content as usual */
	return $sc;

}</code></pre>

## Breaking Down the Function

**Start the Buffer**

First, we start the output buffer with `ob_start();`. This will prevent the following content to be output. Anything you will echo after the buffer is started will be buffered instead of being output.

**Write the HTML**

Then we add our HTML. Everything can be outside PHP at this stage. You can just close the PHP tag and write as much HTML as you want. Everything will be stored in the buffer, preventing the &#8220;content at the top of the page&#8221; issue.

**Get the Content**

The next step is to save all the buffered content into a PHP variable by using `ob_get_contents();`. In our example, we use the `$sc` variable to save the HTML we previously wrote.

**Cleaning the Buffer**

Before finishing, we clean the buffer by calling `ob_end_clean();`. This will result in emptying the current buffer and turning off the output buffer.

**Return the Content**

Finally, we can return the content saved in the `$sc` variable just like it&#8217;s supposed to be done.