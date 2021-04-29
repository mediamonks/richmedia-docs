---
layout: post
title: Introducing Handlebars to the .richmediarc
subtitle: building an even more powerful framework
author: frankie_bukenya
tags: [handlebars]
comments: true
---

This is what the index file looks like with handlebars:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>{{settings.size.width}}x{{settings.size.height}}</title>
  <link rel="stylesheet" href="{{content.localization}}" type="text/css">
  <link rel="stylesheet" href="{{content.versionStyle}}" type="text/css">
  <script type="text/javascript">
    var clickTag = "{{content.clickTag}}";
  </script>
</head>

<body>
<div class="banner border">
  <div class="content fullscreen" style="opacity: 0">

    <div class="frame frame0">
      {{#if content.illType}}
        <img class="element" svg src="{{content.imageElement}}">
      {{else}}
        <img class="gradient" src="{{content.gradient}}">
        <img class="element" src="{{content.imageElement}}">
      {{/if}}
      <div class="copy0 copy thin">{{{content.copy0}}}</div>
    </div>

    <div class="frame frame1">
      <div class="copy1 copy thin">{{{content.copy1}}}</div>
      <div class="cta_back">
        <img class="logo_color" svg src="{{content.imageLogoColor}}">
      </div>
      <img class="cursor" svg src="{{content.imageCursor}}">
    </div>

    <div class="frame frame2">
      <div class="copy2 copy thin">{{{content.copy2}}}</div>
      <div class="cta">
        <div class="copy_cta medium">{{{content.copyCta}}}</div>
      </div>
      <img class="logo" svg src="{{content.imageLogo}}">
      <div class="disclaimer light">{{{content.copyDisclaimer}}}</div>
    </div>
    <img class="replay" src="{{content.imageReplay}}">
  </div>
  <div class="mainExit fullscreen"></div>
</div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.6.0/gsap.min.js"></script>

</body>
</html>

```

This is an example of a single index.hbs file that was used to create *ALL* the units in a single project. 
