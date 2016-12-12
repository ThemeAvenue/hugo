---
title: 'Create your portfolio using Behance API & Handlebars'
author: Julien Vernet
layout: post
date: 2014-07-17T05:30:45+00:00
url: /portfolio-behance-api-handlebars/
prompt_recipient_ids:
  - 'a:0:{}'
categories:
  - Lab
  - Web Development

---
Today I&#8217;ve decided to share with you my latest experiment: a portfolio page based on Behance API.

\[zilla\_button url=&#8221;https://siamkreative.github.io/Behance-API-Handlebars/&#8221; style=&#8221;orange&#8221; size=&#8221;medium&#8221; type=&#8221;square&#8221; target=&#8221;\_blank&#8221;] View demo [/zilla\_button\] \[zilla\_button url=&#8221;https://github.com/siamkreative/Behance-API-Handlebars&#8221; style=&#8221;black&#8221; size=&#8221;medium&#8221; type=&#8221;square&#8221; target=&#8221;\_blank&#8221;\] Code on Github [/zilla\_button]

### Technologies I used to create the portfolio

The great thing with front-end development is that there&#8217;s always new stuff to experiment with. Truth is, there are so many new technologies (frameworks, plugins and preprocessors) that I struggle to choose and stick with only a few. In this experiment, I wanted to learn how to use [Handlebars][1], which is an awesome templating engine used for instance by [Ghost][2]. Let&#8217;s sum up the different technologies we&#8217;re gonna use:

  * Behance API
  * HTML5 for a semantic markup
  * CSS3 & LESS preprocessor (along with [Preboot.less][3] from [@mdo][4])
  * jQuery & Handlebars for processing & populating AJAX data
  * sessionStorage for saving Behance data in the browser

### Pros & Cons:

Below is a list of advantages/drawbacks of doing it with front-end technologies only:

<div class="row-fluid">
  <div class="span6 rhcol">
    <h4>
      Pros
    </h4>
    
    <ul>
      <li>
        <span style="color: #339966;">Can be hosted for free on <a href="https://pages.github.com/">Github Pages</a>, <a href="https://confluence.atlassian.com/display/BITBUCKET/Publishing+a+Website+on+Bitbucket">Bitbucket</a> (or even on Dropbox) as it does not require PHP or any other server-side language. These hosting options are blazing fast!</span>
      </li>
      <li>
        <span style="color: #339966;">Page will be rendered even if getting data from Behance isn&#8217;t done (no time to first byte issue)</span>
      </li>
      <li>
        <span style="color: #339966;">Readability and ease-of-use of Handlebars templates</span>
      </li>
    </ul>
  </div>
  
  <div class="rhcol span6">
    <h4>
      Cons
    </h4>
    
    <ul>
      <li>
        <span style="color: #800000;">Your Behance <strong>API key is exposed</strong> (visible in the browser source)</span>
      </li>
      <li>
        <span style="color: #800000;">It requires an additional templating engine / library (in this experiment, Handlebars library is 44kb minified)</span>
      </li>
    </ul>
  </div>
</div>

### Todo-list:

Here&#8217;s the **list of things I&#8217;d like to do** (but I won&#8217;t probably&#8230;):

  1. Find a way to hide the API key (seems impossible to do this without server-side language)
  2. Add loading spinner while requesting data from Behance API
  3. Make sure it&#8217;s W3C compliant
  4. Make it fully responsive, and eventually serve retina-ready images (_if available from the Behance API_)
  5. Add click tracking to Google Analytics (for instance using [Boba.js][5])
  6. Figure out a way to cache images (seems impossible to do this without server-side language)
  7. Eventually switch to jQuery 2.x as it seems faster (but does not support Internet Explorer 6, 7, or 8)
  8. Fallback for old browsers 
      1. [Media Queries][6] are supported from IE9
      2. [sessionStorage][7] is supported from IE8

 [1]: http://handlebarsjs.com/
 [2]: https://ghost.org/
 [3]: http://getpreboot.com/
 [4]: http://twitter.com/mdo
 [5]: http://boba.space150.com/
 [6]: http://caniuse.com/#feat=css-mediaqueries
 [7]: http://caniuse.com/#feat=namevalue-storage