---
layout: post
title:  "Polynomielle Erweiterung"
author: moritz
categories: Algebra
image: assets/images/poexe.png
lang: de
---
Ein **Polynom** ist ein mathematischer Ausdruck, der aus Variablen, Konstanten und Exponenten besteht, welche durch mathematische Operationen wie Addieren, Subtrahieren, Multiplizieren oder Dividieren durch Konstanten zusammengefügt wurden. 
Eine **Erweiterung** eines Produkts von Summen nutzt das sogenannte Distributivgesetz der Multiplikation und Addition um das Produkt von Summen anders darzustellen. Wir sagen dazu auch **ausmultiplizieren**.

Nachdem wir diese beiden Begriffe eingeführt haben, können wir die folgende Frage beantworten:

### Was ist eine polynomielle Erweiterung?
Die Erweiterung eines Polynoms ist die Erweiterung eines Polynoms, in der keine der Veriablen in Klammern vorkommt und alle Summanden miteinander kombiniert wurden.

## Wie erweitert man ein Polynom?

Falls wir einen oder zwei Ausdrücke haben, die wie ausmultiplizieren sollen, können wir das einfach per Hand machen. Aber was, wenn wir eine komplexere Formel haben wie zum Beispiel: <math display="inline"> <mrow> <mo form="prefix" stretchy="false">(</mo> <mn>3</mn> <mi>a</mi> <mo>+</mo> <mn>2</mn> <msup> <mo form="postfix" stretchy="false">)</mo> <mn>4</mn> </msup> </mrow> </math>.
Diesen gesamten Ausdruck viermal per Hand auszumultiplizieren dauert sehr lange.
<p>Glücklicherweise gibt es dabei einige Muster, die wir uns zu Nutze machen können.</p>

### Erweiterung mithilfe des Pascalschen Dreiecks Expansion with Pascal's Triangle
Das Pascalsche Dreieck hat seinen Namen dank des berühmten und revolutionären französischen Mathematiker [Blaise Pascal (1623-1662 n. Chr.)](https://de.wikipedia.org/wiki/Blaise_Pascal). Hier werden in Form eines Dreiecks sogenannte Binomialkoeffizienten dargestellt, die essentiell für das Ausmultiplizieren von Polynomen sind. Dieses Muster war der östlichen Welt schon lang bekannt, bevor es im Westen entdeckt wurde.

#### Wie konstruiert man dieses Dreieck?
- Das Dreieck startet mit einer 1 auf der linken und rechten Seite
- Jede weitere Zahl ergibt sich als die Summe der beiden Zahlen schräg links und schräg rechts über ihr.

#### Wie kann man diesen Dreieck für polynomielle Erweiterung benutzen?
Für einen beliebigen Exponennten <math display="inline"><mi>n</mi></math> können wir den Ausdruck  <math display="inline"><mrow><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><msup><mo form="postfix" stretchy="false">)</mo><mi>n</mi></msup></mrow></math> mithilfe der Koeffizienten im Dreieck umschreiben. 
Um die richtigen Koeffizienten für den Ausdruck <math display="inline"><mrow><mi>n</mi></mrow></math> zu erhalten, müssen wir uns die <math display="inline"><mrow><mi>n</mi><mo>+</mo><mn>1</mn></mrow></math>-te Reihe ansehen.

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

Demnach müssen wir uns für das Beispiel von oben <math display="inline"> <mrow> <mo form="prefix" stretchy="false">(</mo> <mn>3</mn> <mi>a</mi> <mo>+</mo> <mn>2</mn> <msup> <mo form="postfix" stretchy="false">)</mo> <mn>4</mn> </msup> </mrow> </math>, 
die fünfte Reihe des Pascalschen Dreiecks anschauen, wo wir die folgenden Koeffizienten finden: 1, 4, 6, 4, 1.
Mithilfe dieser Koeffizienten können wir dieses Polynom von viertem Grad umschreiben als:

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

Jetzt müssen wir nur noch ein wenig ausmultiplizieren:

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

### Erweiterung von Polynomen zweiten Grades mit mehr als zwei Variablen
In den vorherigen Beispielen haben wir gesehen, wie wir Binome erweitern können. Aber was, wenn wir mehr als zwei Variablen haben?

Jetzt zeigen und beweisen wir euch, wie man Polynome vom zweiten Grad erweitern kann.
#### Kannst du das Muster erkennen?
<span style="color: red;">*Spoiler:*</span> Schau dir den Beitrag zu [der Summe von <math display="inline"><mi>n</mi></math> ungeraden Zahlen](https://visualproofs.github.io/series/algebra/2023/05/25/de_n-odd-numbers.html) an und sieht, wie wir dort Quadratzahlen darstellen.

Wie du dir bestimmt gedacht hast, nutzen wir dafür ein Quadrat. Demnach ist das Quadrat der Summe zweier Variablen <math display="inline"><mrow><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><msup><mo form="postfix" stretchy="false">)</mo><mn>2</mn></msup> </mrow> </math> nichts anderes als die Fläche eines Quadrats mit Höhe und Breite <math display="inline"><mrow><mi>a</mi><mo>+</mo><mi>b</mi></mrow></math>

![walking]({{ site.baseurl }}/assets/images/Identity.png)

Durch die Konstruktion eines solchen Quadrats können wir sehen, in welche kleineren Flächen sich das größere Quadrat aufteilen lässt: <math display="inline"><msup><mi>a</mi><mn>2</mn></msup></math>, <math display="inline"><msup><mi>b</mi><mn>2</mn></msup></math> and <math display="inline"><mrow><mn>2</mn><mi>a</mi><mi>b</mi></mrow></math>
Das beweist die folgende algebraische Identität:
<math display="block"><mrow><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><msup><mo form="postfix" stretchy="false">)</mo><mn>2</mn></msup><mo>=</mo><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><mo form="postfix" stretchy="false">)</mo><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><mo form="postfix" stretchy="false">)</mo><mo>=</mo><msup><mi>a</mi><mn>2</mn></msup><mo>+</mo><mn>2</mn><mi>a</mi><mi>b</mi><mo>+</mo><msup><mi>b</mi><mn>2</mn></msup></mrow></math>

### Versuch es selbst

Benutze den Schieber um verschiedene Werte für <math display="inline"><mi>n</mi></math> auszuprobieren.
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