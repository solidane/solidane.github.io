---
layout: post
title:  "Der Satz des Pythagoras"
author: moritz
categories: Geometry
image: assets/images/pytagora.jpeg
---
[Pythagoras von Samos (570-495 BC)](https://de.wikipedia.org/wiki/Pythagoras) war ein einflussreicher greichischer Philosoph der Antike, dessen Arbeit verschiedenste Felder von Musik und Philosophie bis hin zu Astronomie und Mathematik revolutionierte - auch wenn du ihn vermutlich nur vom berühmten Satz des Pythagoras kennst. $$a^2$$

![walking]({{ site.baseurl }}/assets/images/pitagora.jpg)

Der Satz des Pythagoras ist ein bekanntest und wegweisendes Theorem der Geometrie. Er besagt, dass in einem rechtwinkligen Dreieck (ein Dreieck mit einem 90°-Winkel) das Quadrat der Hypotenuse (die Seite gegenüber von dem 90°-Winkel) genauso groß ist wie die Fläche der beiden Quadrate über den kürzeren Seiten zusammengenommen.

Dieser Satz hat zahlreiche Anwendungen unter anderem in Ingenieurswissenschaften, Gesichtserkennung in Überwachungskameras, Navigationssystemen, etc...

**Zu zeigen:** In einem Dreieck mit einem rechten Winkel (90°-Winkel) hat das Quadrat über der längeren Seite die selbe Fläche wie die beiden Quadrate über der kürzeren Seite zusammen!

### Visualisieren wir ein Beispiel
Wir malen ein rechtwinkliges Dreieck und errichten an seinen Seiten Quadrate:
- 3*3-Quadrat an der vertikalen Seite
- 4*4-Quadrat an der horizontalen Seite
- 5*5-Quadrat an der Hypotenuse

![walking]({{ site.baseurl }}/assets/images/pyta.png)

Nach dem Satz sollten die kleineren Quadrate zusammen exakt genauso groß sein wie das Quadrat über der Hypotenuse.

##### Ist das in unserem Beispiel der Fall?
Schauen wir es uns an! Zähle die Anzahl der kleinen Quadrate und überprüfe, ob in den beiden kleineren Quadrate zusammen genauso viele sind wie im größeren.
Wenn du richtig gezäglt hast, solltest du 9 + 16 = 25 herausbekommen.

### Versuch es selbst
Spiele mit den Werten für a und b herum und schau dir an, warum der Satz gilt:
<div id="observablehq-21c7f424">
  <div class="observablehq-viewof-a"></div>
  <div class="observablehq-viewof-b"></div>
  <div class="observablehq-canvas"></div>
  <div class="observablehq-blla"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/untitled.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof a") return Inspector.into("#observablehq-21c7f424 .observablehq-viewof-a")();
    if (name === "viewof b") return Inspector.into("#observablehq-21c7f424 .observablehq-viewof-b")();
    if (name === "canvas") return Inspector.into("#observablehq-21c7f424 .observablehq-canvas")();
    if (name === "blla") return Inspector.into("#observablehq-21c7f424 .observablehq-blla")();
  });
</script>

### Die Mathematik dahinter
Die Gleichung im Satz des Pythagoras lautet:
<math display="block" xmlns="http://www.w3.org/1998/Math/MathML">
  <mrow>
    <msup>
      <mi>a</mi>
      <mn>2</mn>
    </msup>
    <mo>+</mo>
    <msup>
      <mi>b</mi>
      <mn>2</mn>
    </msup>
    <mo>=</mo>
    <msup>
      <mi>c</mi>
      <mn>2</mn>
    </msup>
  </mrow>
</math>

wobei a und b für die Länge der Katheten steht, die am rechten Winkel anliegen, und c für die Länge der Hypotenuse, die dem rechten Winkel gegenüber liegt.