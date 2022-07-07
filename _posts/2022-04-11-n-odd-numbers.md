---
layout: post
title:  "The sum of n consequent odd integers"
categories: [Series, Algebra]
image: assets/images/1.jpg

---

The scope of odd numbers includes all of the integers, who have a remainder of one when divided by two.
With n being an integer, the general form of an odd number would be \(2*n - 1\), and such numbers would be: 1, 3, 5, 7, 9, 11, 13...

   The sum of n odd integers is nothing else but the summation (adding up) of a series of odd numbers starting 
from 1 up to a certain n or even infinity. 

## Discovering patterns

Let's start small and sum up:
- the first 2 odd numbers. 1 + 3 = 4   
- the first 3 odd numbers: 1 + 3 + 5 = 9 
- the first 4 odd numbers: 1 + 3 + 5 + 7 = 16

#### Do you see a pattern emerging? 
If you haven't noticed so far, that pattern says that if we add the first n odd numbers then the result is <math display="inline"> <msup> <mi>n</mi> <mn>2</mn> </msup> </math>. 
We might be up to something, if this pattern holds?

#### Are the sums of odd numbers related to square numbers?
Up to this point the pattern holds and seems to be promising, but we still have to reassure that this is not some kind of unorthodox coincidence.

Let's think on ways on how one can represent square numbers. A trivial and very logical candidate would be a square cause of equivalent lengths of width and height.

Now let's take for instance the first 2 odd numbers 1 and 3, and let's represent them as sets of squares:

![walking]({{ site.baseurl }}/assets/images/4cube.png)

Since we are looking for a visual representation of <math display="inline"> <msup> <mi>2</mi> <mn>2</mn> </msup> </math> , in this case the most useful representation of 4 blocks would be this:

![walking]({{ site.baseurl }}/assets/images/4cube2.png)

Which can clearly be derived from the surface area of the square.

Let's add for instance the next odd number 5 to the existing blocks.
![walking]({{ site.baseurl }}/assets/images/45Cubes.png)

If it would be to fit in one square, it would look something like this:
![walking]({{ site.baseurl }}/assets/images/9cube.png)

To get to the next odd number we just have to add 2 to the previous odd number. Similar in this case every layers differs two blocks more or less from the neighbouring ones. Although we only illustrated for n = 3, one can see that this pattern holds!

### Try it yourself

Use the slider below to test it for different n-values.
<div id="observablehq-c1e9a462">
  <div class="observablehq-viewof-n"></div>
  <div class="observablehq-sumOfOdd"></div>
  <div class="observablehq-sumToTex"></div>
  <div class="observablehq-firstNOddNumbers"></div>
  <div class="observablehq-sum"></div>
  <div class="observablehq-drawExample"></div>
  <div class="observablehq-drawDots"></div>
  <div class="observablehq-oddNums"></div>
  <div class="observablehq-n"></div>
  <div class="observablehq-aba"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/geometric-intuition-for-sum-of-first-n-odd-numbers.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof n") return Inspector.into("#observablehq-c1e9a462 .observablehq-viewof-n")();
    if (name === "sumOfOdd") return Inspector.into("#observablehq-c1e9a462 .observablehq-sumOfOdd")();
    if (name === "n") return Inspector.into("#observablehq-c1e9a462 .observablehq-n")();
    if (name === "aba") return Inspector.into("#observablehq-c1e9a462 .observablehq-aba")();
  });
</script>
## Mathematical form

The formula to calculate this pattern is:

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

