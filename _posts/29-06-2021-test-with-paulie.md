---
layout: post
title: Paulie Test
subtitle: Introducing docs
author: Frankie
tags: 
comments: true
---


And you want to use these values in your html/hbs file.

you would only need to get the current object of the feed.

```js
const feed = window.dynamicContent["generator_richmedia_temple_framework_test_feed_main"][0];
```

and apply it to the html/hbs like this.

```js
// always import it
import dataBind from "@mediamonks/temple/util/dataBind";

// somewhere in your code
dataBind(feed, document.querySelector('body'));
```

and the html bindings would look like this

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>