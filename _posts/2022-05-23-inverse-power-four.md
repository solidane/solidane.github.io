---
layout: post
title:  "Sum of inverse powers of four"
author: solida
categories: Series
image: assets/images/Power4.png
---
In mathematics, a series is the sum of the several numbers, or elements of a
sequence. If we are dealing with a finite sequence, meaning we have a limited
number of elements in a sequence, the sum of that sequence would also be a finite
series. In the other hand a infinite series is the result of adding up a infinite
sequence of numbers. Through use of limit we can determine if a infinite series
converges or diverges. Exe. of series we also considered are [Gauss Summation](https://visualproofs.github.io/series/2022/04/12/gauss.html)
and [Fibonacci Sequence](https://visualproofs.github.io/series/2022/04/12/fibonacci.html).

<div id="observablehq-6c0f974d">
  <div class="observablehq-viewof-levels"></div>
  <div class="observablehq-dom"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/inverse-power-of-4.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof levels") return Inspector.into("#observablehq-6c0f974d .observablehq-viewof-levels")();
    if (name === "dom") return Inspector.into("#observablehq-6c0f974d .observablehq-dom")();
  });
</script>