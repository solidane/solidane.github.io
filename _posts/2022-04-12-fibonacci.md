---
layout: post
title:  "Fibonacci Sequence"
author: solida
categories: [ Jekyll, tutorial ]
image: assets/images/Fibo.png
---
The Fibonacci sequence is in mathematics a sequence of numbers, where each number is the result of the sum of the two preceding ones. 
This sequence typically starts from 0 and 1 (the examples in the following are also based on this), although there are other alterations.  
A sequence given the above mentioned starting would be 0,1,1,2,3,5,8,13... and so on forever. 
This famous sequence has appliance in many departments from computer science to photography, where it's known as the golden ratio. 
The formula used to generate such a sequence would be:

<math display="block">
  <mrow>
    <msub>
      <mi>F</mi>
      <mn>0</mn>
    </msub>
    <mo>=</mo>
    <mn>0</mn>
    <mo separator="true">,</mo>
    <msub>
      <mi>F</mi>
      <mn>1</mn>
    </msub>
    <mo>=</mo>
    <mn>1</mn>
  </mrow>
</math>

and

<math display="block">
  <mrow>
    <msub>
      <mi>F</mi>
      <mi>n</mi>
    </msub>
    <mo>=</mo>
    <msub>
      <mi>F</mi>
      <mrow>
        <mi>n</mi>
        <mo>−</mo>
        <mn>1</mn>
      </mrow>
    </msub>
    <mo>+</mo>
    <msub>
      <mi>F</mi>
      <mrow>
        <mi>n</mi>
        <mo>−</mo>
        <mn>2</mn>
      </mrow>
    </msub>
  </mrow>
</math>

for n>1

Use the slider below to test it for different n-values.


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