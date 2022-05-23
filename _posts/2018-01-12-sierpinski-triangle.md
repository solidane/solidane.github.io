---
layout: post
title:  "Sierpinski Triangle"
author: solida
categories: [ Jekyll, tutorial ]
image: assets/images/2.jpg
---
<div id="observablehq-f40c7c08">
  <div class="observablehq-viewof-sierp_steps"></div>
  <div class="observablehq-sierp_steps"></div>
  <div class="observablehq-sierp_approx"></div>
  <div class="observablehq-sierpIFS"></div>
  <div class="observablehq-viewof-sierp_steps2"></div>
  <div class="observablehq-sierp_steps2"></div>
  <div class="observablehq-viewof-seed"></div>
  <div class="observablehq-seed"></div>
  <div class="observablehq-sierp_approx2"></div>
  <div class="observablehq-viewof-start"></div>
  <div class="observablehq-start"></div>
  <div class="observablehq-viewof-clear"></div>
  <div class="observablehq-clear"></div>
  <div class="observablehq-canvas"></div>
  <div class="observablehq-polygon"></div>
  <div class="observablehq-MathJax"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/construction-of-the-serpinski-triangle.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof sierp_steps") return Inspector.into("#observablehq-f40c7c08 .observablehq-viewof-sierp_steps")();
    if (name === "sierp_steps") return Inspector.into("#observablehq-f40c7c08 .observablehq-sierp_steps")();
    if (name === "sierp_approx") return Inspector.into("#observablehq-f40c7c08 .observablehq-sierp_approx")();
    if (name === "sierpIFS") return Inspector.into("#observablehq-f40c7c08 .observablehq-sierpIFS")();
    if (name === "viewof sierp_steps2") return Inspector.into("#observablehq-f40c7c08 .observablehq-viewof-sierp_steps2")();
    if (name === "sierp_steps2") return Inspector.into("#observablehq-f40c7c08 .observablehq-sierp_steps2")();
    if (name === "viewof seed") return Inspector.into("#observablehq-f40c7c08 .observablehq-viewof-seed")();
    if (name === "seed") return Inspector.into("#observablehq-f40c7c08 .observablehq-seed")();
    if (name === "sierp_approx2") return Inspector.into("#observablehq-f40c7c08 .observablehq-sierp_approx2")();
    if (name === "viewof start") return Inspector.into("#observablehq-f40c7c08 .observablehq-viewof-start")();
    if (name === "start") return Inspector.into("#observablehq-f40c7c08 .observablehq-start")();
    if (name === "viewof clear") return Inspector.into("#observablehq-f40c7c08 .observablehq-viewof-clear")();
    if (name === "clear") return Inspector.into("#observablehq-f40c7c08 .observablehq-clear")();
    if (name === "canvas") return Inspector.into("#observablehq-f40c7c08 .observablehq-canvas")();
    if (name === "polygon") return Inspector.into("#observablehq-f40c7c08 .observablehq-polygon")();
    if (name === "MathJax") return Inspector.into("#observablehq-f40c7c08 .observablehq-MathJax")();
  });
</script>
