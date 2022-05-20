---
layout: post
title:  "Sierpinski Triangle"
author: solida
categories: [ Jekyll, tutorial ]
image: assets/images/2.jpg
---
<div id="observablehq-099c322a">
  <div class="observablehq-d3"></div>
  <div class="observablehq-width"></div>
  <div class="observablehq-height"></div>
  <div class="observablehq-offset"></div>
  <div class="observablehq-B"></div>
  <div class="observablehq-C"></div>
  <div class="observablehq-A"></div>
  <div class="observablehq-viewof-recursion_depth"></div>
  <div class="observablehq-recursion_depth"></div>
  <div class="observablehq-remove_triangles"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/sierpinski-triangle.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "d3") return Inspector.into("#observablehq-099c322a .observablehq-d3")();
    if (name === "width") return Inspector.into("#observablehq-099c322a .observablehq-width")();
    if (name === "height") return Inspector.into("#observablehq-099c322a .observablehq-height")();
    if (name === "offset") return Inspector.into("#observablehq-099c322a .observablehq-offset")();
    if (name === "B") return Inspector.into("#observablehq-099c322a .observablehq-B")();
    if (name === "C") return Inspector.into("#observablehq-099c322a .observablehq-C")();
    if (name === "A") return Inspector.into("#observablehq-099c322a .observablehq-A")();
    if (name === "viewof recursion_depth") return Inspector.into("#observablehq-099c322a .observablehq-viewof-recursion_depth")();
    if (name === "recursion_depth") return Inspector.into("#observablehq-099c322a .observablehq-recursion_depth")();
    if (name === "remove_triangles") return Inspector.into("#observablehq-099c322a .observablehq-remove_triangles")();
  });
</script>

