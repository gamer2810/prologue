---
title: Improving Webpage Performance
layout: post
date: 2020-10-06T04:43:48.263Z
tags:
  - devlog
  - web
  - webdev
  - performance
author: K3K
---
After playing around with Google Lighthouse, I found various places in the code where I can easily improve to enhance this site's performance. This note serves both as a to-do list for this site and a note of things to check for when developing any web page.

1. Pay extra attention to included CSS and JS files

   Clarify which files need to be load for a specific page. Excessive CSS and JS scripts could lead to unwanted errors, waste browser's resources and downgrade the site's performance.

   Do not include scripts for a specific page (Ex: Homepage) in a page-wise component (Ex: Sidebar Navigation).
2. Preload resources using HTML <link> tags

   HTML offers a wide range of options for you to preload resources:

   * `<link rel="preload" as="{TYPE}">`: preload a specific resource (document, image, style...).

     Read more: <https://developer.mozilla.org/en-US/docs/Web/HTML/Preloading_content#The_basics>
   * `<link rel="preconnect">`: establish early connections so that subsequent fetch will not have to, hence the increase in performance.

     Read more: <https://web.dev/uses-rel-preconnect/>
   * `<link rel="dns-fetch">`: same as preconnect.
3. All list members should be encapsulated in a `<li>` tag.

   ``