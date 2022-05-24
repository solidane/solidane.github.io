---
layout: post
title:  "Fibonacci Sequence"
author: solida
categories: [ Jekyll, tutorial ]
image: assets/images/4.jpg
---

<div id="observablehq-412999a1">
  <div class="observablehq-viewof-series"></div>
  <div class="observablehq-canvas"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/fibonacci-series-visualised.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof series") return Inspector.into("#observablehq-412999a1 .observablehq-viewof-series")();
    if (name === "canvas") return Inspector.into("#observablehq-412999a1 .observablehq-canvas")();
  });
</script>