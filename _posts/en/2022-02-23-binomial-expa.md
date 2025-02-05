---
layout: post
title:  "Polynomial expansion"
author: solida
categories: Algebra
image: assets/images/poexe.png
lang: en
---
A **polynomial** is defined as an expression which is made of variables, constants and exponents, that are merged using mathematical operations such as addition, subtraction, multiplication and division by numbers.
On the other hand, an **expansion** of a product of sums in mathematics expresses it as a sum of products as a result of distributive properties of multiplication over addition.

So now after we defined these two terms we can answer the question:
### What is a Polynomial Expansion?
The expansion of a polynomial is an expression of the same polynomial, where no variable appears within parentheses and all identical terms have been combined.

## How to expand a Polynomial?

If we have one or two expressions to be multiplied, we can easily do it manually. But what if we have an expression of the form: <math display="inline"> <mrow> <mo form="prefix" stretchy="false">(</mo> <mn>3</mn> <mi>a</mi> <mo>+</mo> <mn>2</mn> <msup> <mo form="postfix" stretchy="false">)</mo> <mn>4</mn> </msup> </mrow> </math>.
Multiplying the whole thing 4 times by hand sure does take some time. 
<p>To our luck, there are some patterns we can use.</p>

### Expansion with Pascal's Triangle

Pascal's triangle was named after the famous and revolutionary french mathematician of the 17th century [Blaise Pascal (1623-1662 AD)](https://en.wikipedia.org/wiki/Blaise_Pascal)
and it is a visual triangular representation of the binomial coefficients, which are essential for expanding polynomials. This pattern was known and practiced in the far and near east centuries before the western world.

#### How to construct a such triangle
- The triangle starts with a 1 on top and below that a 1 on the left and right side. 
- For the following rows below, every number is the sum of the two numbers that are above it in the previous row.

#### How to expand with the help of the triangle?
Given  <math display="inline"><mrow><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><msup><mo form="postfix" stretchy="false">)</mo><mi>n</mi></msup></mrow></math>
for any power <math display="inline"><mi>n</mi></math> you can write out the expansion using the coefficients from the triangle. 
Note that to write the coefficients for any power <math display="inline"><mi>n</mi></math>, you need to look at row <math display="inline"><mi>n</mi><mo>+</mo><mn>1</mn></math> to find the coefficients.

<div id="observablehq-c7e957ce">
  <div class="observablehq-viewof-values"></div>
  <div class="observablehq-pascal"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/pascals-sierpinski.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof values") return Inspector.into("#observablehq-c7e957ce .observablehq-viewof-values")();
    if (name === "pascal") return Inspector.into("#observablehq-c7e957ce .observablehq-pascal")();
  });
</script>

So for the example above <math display="inline"> <mrow> <mo form="prefix" stretchy="false">(</mo> <mn>3</mn> <mi>a</mi> <mo>+</mo> <mn>2</mn> <msup> <mo form="postfix" stretchy="false">)</mo> <mn>4</mn> </msup> </mrow> </math>,
we would have to check the 5th row of Pascal's triangle to find the coefficients, which are 1, 4, 6, 4, 1.
Knowing the coefficients we can transform the polynom of the 4th grade to:

<math display="block">
  <mrow>
    <mo form="prefix" stretchy="false">(</mo>
    <mn>3</mn>
    <mi>a</mi>
    <msup>
      <mo form="postfix" stretchy="false">)</mo>
      <mn>4</mn>
    </msup>
    <mo>+</mo>
    <mn>4</mn>
    <mo>&times;</mo>
    <mo form="prefix" stretchy="false">(</mo>
    <mn>3</mn>
    <mi>a</mi>
    <msup>
      <mo form="postfix" stretchy="false">)</mo>
      <mn>3</mn>
    </msup>
    <mo>&times;</mo>
    <mn>2</mn>
    <mo>+</mo>
    <mn>6</mn>
    <mo>&times;</mo>
    <mo form="prefix" stretchy="false">(</mo>
    <mn>3</mn>
    <mi>a</mi>
    <msup>
      <mo form="postfix" stretchy="false">)</mo>
      <mn>2</mn>
    </msup>
    <mo>&times;</mo>
    <msup>
      <mn>2</mn>
      <mn>2</mn>
    </msup>
    <mo>+</mo>
    <mn>4</mn>
    <mo>&times;</mo>
    <mn>3</mn>
    <mi>a</mi>
    <mo>&times;</mo>
    <msup>
      <mn>2</mn>
      <mn>3</mn>
    </msup>
    <mo>+</mo>
    <msup>
      <mn>2</mn>
      <mn>4</mn>
    </msup>
  </mrow>
</math>

Then it's only a matter of multiplying:

<math display="block">
  <mrow>
    <mn>81</mn>
    <msup>
      <mi>a</mi>
      <mn>4</mn>
    </msup>
    <mo>+</mo>
    <mn>216</mn>
    <msup>
      <mi>a</mi>
      <mn>3</mn>
    </msup>
    <mo>+</mo>
    <mn>216</mn>
    <msup>
      <mi>a</mi>
      <mn>2</mn>
    </msup>
    <mo>+</mo>
    <mn>96</mn>
    <mi>a</mi>
    <mo>+</mo>
    <mn>16</mn>
  </mrow>
</math>

### Expansion of polynomials of the 2nd degree with more than two variables
In the previous examples we saw how one could expand binomials, but what if we have more than two variables. How do we proceed in that case?

In the following we are going to try and visually prove how polynomials of the 2nd degree can be extended.

#### Let's play detective! Can you spot a pattern?
<span style="color: red;">*Spoiler Alert:*</span> Check the post about [The sum of <math display="inline"><mi>n</mi></math> odd integers](https://visualproofs.github.io/series/algebra/2022/04/15/n-odd-numbers.html)
and see what we used to represent square numbers.

As you may have guessed it, we used a square. So for example if we want to calculate the sum of two variables <math display="inline"><mrow><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><msup><mo form="postfix" stretchy="false">)</mo><mn>2</mn></msup> </mrow> </math>
the result is the same as what we would get when calculating the surface area of a square of height and width <math display="inline"><mi>a</mi><mo>+</mo><mi>b</mi></math>.

![walking]({{ site.baseurl }}/assets/images/Identity.png)

and by constructing such a square such as shown in the picture above, one can visibly see that the surface area is the sum of <math display="inline"><msup><mi>a</mi><mn>2</mn></msup></math>, <math display="inline"><msup><mi>b</mi><mn>2</mn></msup></math> and <math display="inline"><mrow><mn>2</mn><mi>a</mi><mi>b</mi></mrow></math>, which proves
the algebraic identity:
<math display="block"><mrow><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><msup><mo form="postfix" stretchy="false">)</mo><mn>2</mn></msup><mo>=</mo><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><mo form="postfix" stretchy="false">)</mo><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><mo form="postfix" stretchy="false">)</mo><mo>=</mo><msup><mi>a</mi><mn>2</mn></msup><mo>+</mo><mn>2</mn><mi>a</mi><mi>b</mi><mo>+</mo><msup><mi>b</mi><mn>2</mn></msup></mrow></math>

### Try it yourself

Use the slider below to expand the square for different numbers of variables.
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
  });
</script>