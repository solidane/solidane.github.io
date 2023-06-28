---
layout: post
title:  "Sum of inverse powers of four"
author: solida
categories: [Series, Fractals]
image: assets/images/powerofi4.png
lang: en
---
In mathematics, a **series** is the sum of several numbers, of which there may be finitely or even infinitely many. All the numbers, which we sum over, form a so-called **sequence**.

How many elements are in the sequence?
- If we are dealing with a <span style="color: red;">*finite*</span> sequence, meaning we have a limited
number of elements we sum over, the sum of that sequence is a <span style="color: red;">*finite*</span>
series.  **Example**: [The sum of <math display="inline"><mi>n</mi></math> odd integers](https://visualproofs.github.io/series/algebra/2022/04/15/n-odd-numbers.html) and [Gauss Summation](https://visualproofs.github.io/series/2022/05/12/gauss.html)
- Alternatively, an <span style="color: red;">*infinite*</span> series is the result of adding up an <span style="color: red;">*infinite*</span>
sequence of numbers. Through the use of limit we can determine if an infinite series
converges or diverges. Let's look at an example!

### Get your paint and brushes! We are painting a canvas
We start with an empty, square Canvas,

![walking]({{ site.baseurl }}/assets/images/canvas.png)

and we want to paint <math display="inline"><mfrac><mn>1</mn><mn>4</mn></mfrac></math> of it blue:

![walking]({{ site.baseurl }}/assets/images/canvas1.png)

So we end up with something like this. Now, we want to paint another <math display="inline"><mfrac><mn>1</mn><mn>16</mn></mfrac></math> blue:

![walking]({{ site.baseurl }}/assets/images/canvas2.png)

This would be the resulting look. So we additionally painted <math display="inline"><mfrac><mn>1</mn><mn>4</mn></mfrac></math>-th of <math display="inline"><mfrac><mn>1</mn><mn>4</mn></mfrac></math>-th of the original canvas. We continue with <math display="inline"><mfrac><mn>1</mn><mn>64</mn></mfrac></math>:

![walking]({{ site.baseurl }}/assets/images/canvas3.png)

We then paint <math display="inline"><mfrac><mn>1</mn><mn>4</mn></mfrac><mo>&times;</mo><mfrac><mn>1</mn><mn>64</mn></mfrac><mo>=</mo><mfrac><mn>1</mn><mn>256</mn></mfrac></math>.

![walking]({{ site.baseurl }}/assets/images/canvas4.png)

After that we paint blue another <math display="inline"><mfrac><mn>1</mn><mn>1024</mn></mfrac></math>:

![walking]({{ site.baseurl }}/assets/images/canvas5.png)

We can go on like this, painting blue <math display="inline"><msup><mrow><mfrac><mn>1</mn><mn>4</mn></mfrac></mrow><mi>n</mi></msup></math> of the surface in every step.

After every step, we have three identical squares, one of which is painted completely blue and the other two are left blank. In the fourth step, the pattern repeats on a smaller scale, we again have one blue and two white squares. This pattern continues infinitely, so that for every scale there is one blue and two white squares. So overall we have painted <math display="inline"><mfrac><mn>1</mn><mn>3</mn></mfrac></math> of the canvas blue.
The blue pattern represents the sum of inverse power of four, and so we can conclude that the sum of inverse powers of 4 converges to <math display="inline"><mfrac><mn>1</mn><mn>3</mn></mfrac></math>.


### Try it yourself
Use the slider below to see how the painting converges to the above-mentioned pattern for different values of <math display="inline"><mi>n</mi></math>.

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

### The math behind it

<math display="block">
  <mrow>
    <mfrac>
      <mn>1</mn>
      <mn>4</mn>
    </mfrac>
    <mo>+</mo>
    <mfrac>
      <mn>1</mn>
      <mn>16</mn>
    </mfrac>
    <mo>+</mo>
    <mfrac>
      <mn>1</mn>
      <mn>64</mn>
    </mfrac>
    <mo>+</mo>
    <mi>.</mi>
    <mi>.</mi>
    <mi>.</mi>
    <mo>=</mo>
    <mrow>
      <munderover>
        <mo movablelimits="false">∑</mo>
        <mrow>
          <mi>i</mi>
          <mo>=</mo>
          <mn>1</mn>
        </mrow>
        <mi>∞</mi>
      </munderover>
    </mrow>
    <mrow>
    <mo stretchy="false" form="prefix">(</mo>
    <mfrac>
      <mn>1</mn>
      <mn>4</mn>
    </mfrac>
    <msup>
    <mo stretchy="false" form="prefix">)</mo>  
    <mi>i</mi>
    </msup>
    </mrow>
    <mo>=</mo>
    <mfrac>
      <mn>1</mn>
      <mn>3</mn>
    </mfrac>
  </mrow>
</math>