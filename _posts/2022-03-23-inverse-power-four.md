---
layout: post
title:  "Sum of inverse powers of four"
author: solida
categories: [Series, Fractals]
image: assets/images/powerofi4.png
---
In mathematics, a **series** is the sum of the several numbers, or elements of a
sequence. 

Based on the amount of objects in the sequence
- If we are dealing with a <span style="color: red;">*finite*</span> sequence, meaning we have a limited
number of elements in a sequence, the sum of that sequence would also be a <span style="color: red;">*finite*</span>
series.  **Example**: [The sum of n odd integers](https://visualproofs.github.io/series/algebra/2022/04/15/n-odd-numbers.html) and [Gauss Summation](https://visualproofs.github.io/series/2022/05/12/gauss.html)
- In the other hand a <span style="color: red;">*infinite*</span> series is the result of adding up a <span style="color: red;">*infinite*</span>
sequence of numbers. Through use of limit we can determine if a infinite series
converges or diverges. **Example**: look below

### Get your paints and brushes! We are painting in a canvas
Okay, so we are on a task. We have this empty, square Canvas,

![walking]({{ site.baseurl }}/assets/images/canvas.png)

and we want to paint $$\frac{1}{4}$$ of it blue

![walking]({{ site.baseurl }}/assets/images/canvas1.png)

we would end up with something like this. Now we want to paint another $$\frac{1}{16}$$ blue

![walking]({{ site.baseurl }}/assets/images/canvas2.png)

and this would be the resulting look. So we additionally painted $$\frac{1}{4}$$-th of $$\frac{1}{4}$$-th of the original canvas. We continue with $$\frac{1}{64}$$:

![walking]({{ site.baseurl }}/assets/images/canvas3.png)

We paint then $$\frac{1}{64} \times \frac{1}{4} = \frac{1}{256}$$.

![walking]({{ site.baseurl }}/assets/images/canvas4.png)

After that we paint blue another $$\frac{1}{1024}$$

![walking]({{ site.baseurl }}/assets/images/canvas5.png)

and we can go so on, painting blue the $$\left(\frac{1}{4}\right)^n$$ of the surface.

Now notice how we have 3 equally divided squares after each step. Notice also how from each of these squares only one
of them is painted blue, meaning we have 3 times identical pattern occurring and only one of them $$\frac{1}{3}$$ is blue coloured.
The blue pattern represents the sum of inverse power of four, and so we can conclude that the sum of inverse power of 4 converges to
$$\frac{1}{3}$$.


### Try it yourself
Use the slider below to see how the pattern converges to the above-mentioned value for different values of $$n$$.

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
    <mo form="prefix" stretchy="false">(</mo>
    <mfrac>
      <mn>1</mn>
      <mn>4</mn>
    </mfrac>
    <msup>
      <mo form="postfix" stretchy="false">)</mo>
      <mi>i</mi>
    </msup>
    <mo>=</mo>
    <mfrac>
      <mn>1</mn>
      <mn>3</mn>
    </mfrac>
  </mrow>
</math>