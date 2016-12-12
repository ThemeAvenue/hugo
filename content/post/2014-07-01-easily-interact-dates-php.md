---
title: Easily Interact with Dates in PHP
author: Julien Liabeuf
layout: post
date: 2014-07-01T07:14:04+00:00
url: /easily-interact-dates-php/
categories:
  - Code Snippets
  - Web Development
tags:
  - date
  - strtotime
  - time
  - timestamp

---
A couple of weeks ago, a project I was working on involved handling dates. I had to get information from a database based on date ranges. This might sound scary at first, but as long as your date ranges aren&#8217;t too complex, it&#8217;s actually easy as pie!

## The Magic Function

Indeed, PHP has a magic function (since PHP 4) called <a href="http://www.php.net/manual/en/function.strtotime.php" target="_blank">strtotime()</a>. This function is darn simple and will save you an inestimable time. It can&#8217;t be simpler to use: tell the function what time you want and it gives you the timestamp. Now, maybe you know this function. Maybe you&#8217;ve even used it in the past. But did you know how far you can go? The function takes two parameters:

<pre><code class="lang-php">strtotime( string $time [, int $now = time() ] )</code></pre>

The `$time` parameter is your human readable date. The `$now` parameter is the relative date to which `$time` applies. In short, by default, the time you ask with `$time` is relative to the moment you ask it (when the function is executed). If you specify a `$now` (should be a timestamp), the date returned by `strtotime()` will be relative to your `$now` timestamp. Need an example? Let&#8217;s ask for the date of last Monday:

<pre><code class="lang-php">$last_monday = strtotime ( 'last Monday' );</code></pre>

As of today, Saturday 28th of June 2014, the result will be `$last_monday = 1403481600`; Pretty sweet huh? Now let&#8217;s see some more of the capabilities&#8230;

## Dates Examples

I won&#8217;t list all the possibilities here because:

  1. There are a LOT of possibilities,
  2. You can figure it out by yourself, possibly with the help of the <a href="http://www.php.net/manual/en/datetime.formats.relative.php" target="_blank">PHP documentation</a>

Also, you&#8217;ll notice I didn&#8217;t add a description for each line as I think the `$time` parameter pretty much speaks for itself.

First, here are the examples given by PHP.net:

<pre><code class="lang-php">echo strtotime("now"), "\n";
echo strtotime("10 September 2000"), "\n";
echo strtotime("+1 day"), "\n";
echo strtotime("+1 week"), "\n";
echo strtotime("+1 week 2 days 4 hours 2 seconds"), "\n";
echo strtotime("next Thursday"), "\n";
echo strtotime("last Monday"), "\n";</code></pre>

Now, here is a few more examples:

<pre><code class="lang-php">strtotime( 'now' );
strtotime( 'last monday', time() );
strtotime( 'next saturday', time() );
strtotime( 'last monday +7 days', time() );
strtotime( 'first day of this month', time() );
strtotime( 'last day of last month', time() );
strtotime( 'first day of january +2 months', time() );
strtotime( 'last day of december', time() );
strtotime( 'first day of march last year', time() );</code></pre>

I think you understand the pattern here. You can basically ask for anything to `strtotime()`. It understands days, months, years. It can add days, months, hours, minutes, seconds to a date. The possibilities are huge and if your operations are quite basic, you should be able to cover it with this function. A real time saver.