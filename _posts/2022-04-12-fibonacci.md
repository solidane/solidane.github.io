---
layout: post
title:  "Fibonacci Sequence"
author: solida
categories: Series
image: assets/images/fibospi.jpg
---
A **sequence** is in mathematics a list of numbers or objects that are in a certain <span style="color: purple;">*order*</span>, where repetition is allowed. Sequences
are called <span style="color: red;">*finite*</span>, if they have a limited number of objects and oppositely <span style="color: red;">*infinite*</span>.

Examples:
- {1, 2, 3, 4,...} - is a <span style="color: red;">*infinite*</span> sequence of the natural numbers
- {2, 4, 6, 8, 10} - is a <span style="color: red;">*finite*</span> sequence of the <span style="color: purple;">*first five*</span>  even numbers
- {Z, Y, X, W, V}  - is a <span style="color: red;">*finite*</span> sequence of the <span style="color: purple;">*last five*</span>  letters of the english alphabet.
- {X, O, X, O,...} - is a <span style="color: red;">*infinite*</span> sequence in an <span style="color: purple;">*alternating*</span> order of X and O.

### How is Fibonacci's sequence defined
The **Fibonacci sequence** is in mathematics a sequence of numbers, where each number is the result of the sum of the two preceding ones. 
This sequence typically starts from 0 and 1 (the examples in the following are also based on this), although there are other alterations.  
A sequence given the above-mentioned starting would be 0,1,1,2,3,5,8,13... and so on forever. 

The Fibonacci numbers were mentioned by Indian mathematicians way back in 200BC, but were first properly introduced 
to the Western mathematics by Leonardo of Pisa in the 13th century.

In terms of nature the Fibonacci numbers appear very often. Things like the number of petals in a flower, seed heads, shells, hurricanes often are a Fibonacci number.
This famous sequence has appliance in many departments from computer science to photography, where it's also strongly
correlated to what we know as the [golden ratio](https://en.wikipedia.org/wiki/Golden_ratio). 

There are many beautiful number patterns that emerge from the Fibonacci numbers.


![walking]({{ site.baseurl }}/assets/images/GoldenRatio.png)


### How to visually understand these numbers
Let's start by putting two one-by-one squares next to one another. 
![walking]({{ site.baseurl }}/assets/images/fib1.png)

As a result we get a one by two rectangle. Beneath that I will put a two-by-two square
![walking]({{ site.baseurl }}/assets/images/fib2.png)

And next to that, a three-by-three square
![walking]({{ site.baseurl }}/assets/images/fib3.png)
Beneath that a five-by-five square
![walking]({{ site.baseurl }}/assets/images/fib5.png)
Creating one giant rectangle. Now let me ask you a question:

##### Whats the area of the final rectangle?
Well, the most trivial answer would be the sum of the areas of all the squares inside it, right! But since it 
is a rectangle one could also multiply base and height to get the total area which would be: <math display="inline"><mrow><mn>5</mn><mo>*</mo><mo form="prefix" stretchy="false">(</mo><mn>5</mn><mo>+</mo><mn>3</mn><mo form="postfix" stretchy="false">)</mo><mo>=</mo><mn>5</mn><mo>*</mo><mn>8</mn></mrow></math>
,with 8 also being the next Fibonacci number on the sequence.

If we continue like this we will be generating rectangles of the following forms:
- <math display="inline"><mrow><mn>8</mn><mo>*</mo><mn>13</mn></mrow></math> 
- <math display="inline"><mrow><mn>13</mn><mo>*</mo><mn>21</mn></mrow></math>
- <math display="inline"><mrow><mn>21</mn><mo>*</mo><mn>34</mn></mrow></math>
- <math display="inline"><mrow><mn>34</mn><mo>*</mo><mn>55</mn></mrow></math>
- <math display="inline"><mrow><mn>55</mn><mo>*</mo><mn>89</mn></mrow></math>

Now check this out, by diving the bigger number to the smaller one we get:
- <math display="inline"><mrow><mn>13</mn><mo lspace="0.2222em" rspace="0.2222em">:</mo><mn>8</mn><mo>=</mo><mn>1.625</mn></mrow></math>
- <math display="inline"><mrow><mn>21</mn><mo lspace="0.2222em" rspace="0.2222em">:</mo><mn>13</mn><mo>=</mo><mn>1.615</mn></mrow></math>
- <math display="inline"><mrow><mn>34</mn><mo lspace="0.2222em" rspace="0.2222em">:</mo><mn>21</mn><mo>=</mo><mn>1.619</mn></mrow></math>
- <math display="inline"><mrow><mn>55</mn><mo lspace="0.2222em" rspace="0.2222em">:</mo><mn>34</mn><mo>=</mo><mn>1.6176</mn></mrow></math>
- <math display="inline"><mrow><mn>89</mn><mo lspace="0.2222em" rspace="0.2222em">:</mo><mn>55</mn><mo>=</mo><mn>1.61818</mn></mrow></math>

as we continue we get closer to about 1.618 known to many people as the golden ratio.
### Try it yourself

Get your hand dirty and use the slider below to explore how the pattern grows for different n-values.


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

### The math behind it
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
