---
title: "Customize the Favicon"
date: 2019-08-11 00:34:00 +0800
categories: [Blogging, Tutorial]
tags: [favicon]
comments: false
toc: false
---

In this project, the image file of Favicon[^favicon] is placed in `assets/img/favicons/`. You may need to replace the icon files with your own. So let's see how to customize these Favicons.

Whit a square image (PNG, JPG or GIF) in hand, open the site [*Favicon & App Icon Generator*](https://www.favicon-generator.org/), upload your original image.

![upload-image]({{ site.baseurl }}/assets/img/sample/upload-image.png)

Wait a moment, the website will automatically generate icons of various sizes.

![download-icons]({{ site.baseurl }}/assets/img/sample/download-icons.png)

Download the generated package, extract the contents and override:

- the PNG files in directory `_assets/img/favicons`
- the `favicon.ico` in the root directory

Rebuild the site so that the icon becomes your custom edition.


<br>

***

[^favicon]: [What are favicons?](https://www.favicon-generator.org/about/)