---
layout: post
title:  "Sum of inverse powers of four"
author: solida
categories: [ Jekyll, tutorial ]
image: assets/images/Power4.png
---
<div id="observablehq-6c0f974d">
  <div class="observablehq-dom"></div>
  <div class="observablehq-viewof-levels"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/inverse-power-of-4.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "dom") return Inspector.into("#observablehq-6c0f974d .observablehq-dom")();
    if (name === "viewof levels") return Inspector.into("#observablehq-6c0f974d .observablehq-viewof-levels")();
  });
</script>