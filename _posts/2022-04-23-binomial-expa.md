---
layout: post
title:  "Polynomial expansion"
author: solida
categories: [ Jekyll, tutorial ]
image: assets/images/Binomial.png
---
<div id="observablehq-fc37ba2b">
  <div class="observablehq-viewof-numVars"></div>
  <div class="observablehq-numVars"></div>
  <div class="observablehq-binomial"></div>
  <div class="observablehq-rectData"></div>
  <div class="observablehq-formula"></div>
  <div class="observablehq-rs"></div>
  <div class="observablehq-ithLetter"></div>
  <div class="observablehq-color"></div>
  <div class="observablehq-d3"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/a-b-c-2.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof numVars") return Inspector.into("#observablehq-fc37ba2b .observablehq-viewof-numVars")();
    if (name === "numVars") return Inspector.into("#observablehq-fc37ba2b .observablehq-numVars")();
    if (name === "binomial") return Inspector.into("#observablehq-fc37ba2b .observablehq-binomial")();
    if (name === "rectData") return Inspector.into("#observablehq-fc37ba2b .observablehq-rectData")();
    if (name === "formula") return Inspector.into("#observablehq-fc37ba2b .observablehq-formula")();
    if (name === "rs") return Inspector.into("#observablehq-fc37ba2b .observablehq-rs")();
    if (name === "ithLetter") return Inspector.into("#observablehq-fc37ba2b .observablehq-ithLetter")();
    if (name === "color") return Inspector.into("#observablehq-fc37ba2b .observablehq-color")();
    if (name === "d3") return Inspector.into("#observablehq-fc37ba2b .observablehq-d3")();
  });
</script>