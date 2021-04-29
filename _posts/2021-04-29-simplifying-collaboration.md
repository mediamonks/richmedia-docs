---
layout: post
title: Introducing modular animation frames
subtitle: better cross collaboration
author: Frankie Bukenya
tags: [animation, collaboration]
comments: true
---

A new approach implemented on a really, big project allowed for multiple developers to work on a project without the risk of
breaking each code, and less duplication of animation code that remained the same. In the below example, a single frame could
be changed and added to the timeline leaving the rest the same and untouched.

```
+-- ..
|-- (shared)
|
|-- scripts (shared scripts)
|   |-- animations (main animations)
|   |   |   |-- animations (parts)
|   |   |   |   |-- copyAnimations.js
|   |   |   |   |-- ctaAnimation.js
|   |   |   |-- Animation.js  (main timeline)
|   |   |   |-- Animation2.js
|   |   |   |-- Animation3.js
|   |   |   |-- Animation4.js
|   |   |   |-- Animation5.js
|   |-- Banner.js
|   |-- Main.js     
|   |-- OtherAnimation.js
|   |-- Variant1.js
|   |-- Variant2.js
|   |
|   +-- ..
|
|-- (rootfiles)
+-- ..
```

This is an example of a very modular structure for shared animations that allows for multiple developers to work
the same project with ease. 
