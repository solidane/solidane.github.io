---
layout: post
title:  "Sierpinski Triangle"
author: solida
categories: Fractals
image: assets/images/sptriangle.jpg
---
A fractal is a pattern, where as you zoom in, similar patterns appear at all smaller scales. Fractals can be thought of as never-ending patterns.



## What is the Sierpinski's fractal?
One of the most well known examples of fractals is
Sierpinski triangle. Wacław Sierpiński was the first mathematician to think about the properties of this triangle, but this pattern is to be found in artwork, patterns, and mosaics many centuries earlier like to be seen in the pictures below:

![walking]({{ site.baseurl }}/assets/images/collage.jpg)

### Removing triangles method

The Sierpinski triangle may be constructed from an equilateral triangle by repeated removal of triangular subsets:
1. Start with an equilateral triangle.
2. Subdivide it into four smaller congruent equilateral triangles and remove the central triangle.
3. Repeat step 2 with the smaller triangles until the end of time

We can easily write a recursive function that performs the above process to a given depth, such that we get a satisfactory approximation of the Sierpinski triangle.

We can visualize this process using the slider to control the stage in the construction below:
<div id="observablehq-f40c7c08">
  <div class="observablehq-viewof-sierp_steps"></div>
  <div class="observablehq-sierp_steps"></div>
  <div class="observablehq-sierp_approx"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/construction-of-the-serpinski-triangle.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof sierp_steps") return Inspector.into("#observablehq-f40c7c08 .observablehq-viewof-sierp_steps")();
    if (name === "sierp_steps") return Inspector.into("#observablehq-f40c7c08 .observablehq-sierp_steps")();
    if (name === "sierp_approx") return Inspector.into("#observablehq-f40c7c08 .observablehq-sierp_approx")();
  });
</script>

## The Chaos Game

<div id="observablehq-a077419d">
  <div class="observablehq-viewof-start"></div>
  <div class="observablehq-start"></div>
  <div class="observablehq-viewof-clear"></div>
  <div class="observablehq-clear"></div>
  <div class="observablehq-canvas"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/construction-of-the-serpinski-triangle.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof start") return Inspector.into("#observablehq-a077419d .observablehq-viewof-start")();
    if (name === "start") return Inspector.into("#observablehq-a077419d .observablehq-start")();
    if (name === "viewof clear") return Inspector.into("#observablehq-a077419d .observablehq-viewof-clear")();
    if (name === "clear") return Inspector.into("#observablehq-a077419d .observablehq-clear")();
    if (name === "canvas") return Inspector.into("#observablehq-a077419d .observablehq-canvas")();
  });
</script>
