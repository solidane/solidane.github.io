---
layout: post
title:  "The sum of n consequent odd integers"
categories: [ Jekyll, tutorial ]
image: assets/images/1.jpg

---

<div id="observablehq-926a4ec7">
        <div class="observablehq-viewof-n"></div>
         <div class="observablehq-n"></div>
        <div class="container">
         <div class="observablehq-sumOfOdd"></div>
        </div>
            <div class="observablehq-sumToTex"></div>
            <div class="observablehq-firstNOddNumbers"></div>
             <div class="observablehq-sum"></div>
             <div class="observablehq-drawExample"></div>
             <div class="observablehq-drawDots"></div>
            <div class="observablehq-oddNums"></div>
    </div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/geometric-intuition-for-sum-of-first-n-odd-numbers.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof n") return Inspector.into("#observablehq-926a4ec7 .observablehq-viewof-n")();
    if (name === "n") return Inspector.into("#observablehq-926a4ec7 .observablehq-n")();
    if (name === "sumOfOdd") return Inspector.into("#observablehq-926a4ec7 .observablehq-sumOfOdd")();
    if (name === "sumToTex") return Inspector.into("#observablehq-926a4ec7 .observablehq-sumToTex")();
    if (name === "firstNOddNumbers") return Inspector.into("#observablehq-926a4ec7 .observablehq-firstNOddNumbers")();
    if (name === "sum") return Inspector.into("#observablehq-926a4ec7 .observablehq-sum")();
    if (name === "drawExample") return Inspector.into("#observablehq-926a4ec7 .observablehq-drawExample")();
    if (name === "drawDots") return Inspector.into("#observablehq-926a4ec7 .observablehq-drawDots")();
    if (name === "oddNums") return Inspector.into("#observablehq-926a4ec7 .observablehq-oddNums")();
  });
</script>

