---
layout: post
title:  "The sum of n consequent odd integers"
categories: 
image: assets/images/1.jpg

---
<math display="block" xmlns="http://www.w3.org/1998/Math/MathML">
  <mrow>
    <msub>
      <mi>S</mi>
      <mi>n</mi>
    </msub>
    <mo>=</mo>
    <munderover>
      <mo>∑</mo>
      <mrow>
        <mi>i</mi>
        <mo>=</mo>
        <mn>0</mn>
      </mrow>
      <mi>n</mi>
    </munderover>
    <mrow>
      <mo stretchy="true" form="prefix">(</mo>
      <mn>2</mn>
      <mi>i</mi>
      <mo>+</mo>
      <mn>1</mn>
      <mo stretchy="true" form="postfix">)</mo>
    </mrow>
    <mo>=</mo>
    <msup>
      <mi>n</mi>
      <mn>2</mn>
    </msup>
  </mrow>
</math>

<div id="observablehq-c1e9a462">
  <div class="observablehq-viewof-n"></div>
  <div class="observablehq-n"></div>
  <div class="observablehq-aba"></div>
  <div class="observablehq-sumOfOdd"></div>
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
    if (name === "viewof n") return Inspector.into("#observablehq-c1e9a462 .observablehq-viewof-n")();
    if (name === "n") return Inspector.into("#observablehq-c1e9a462 .observablehq-n")();
    if (name === "aba") return Inspector.into("#observablehq-c1e9a462 .observablehq-aba")();
    if (name === "sumOfOdd") return Inspector.into("#observablehq-c1e9a462 .observablehq-sumOfOdd")();
  });
</script>

