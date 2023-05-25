---
layout: post
title:  "Die Summe negativer Potenzen von 4"
author: solida
categories: [Series, Fractals]
image: assets/images/powerofi4.png
---
In der Mathematik ist eine **Reihe** definiert als die Summe der Elemente einer zugehörigen Folge, also schlicht eine Summe von Zahlen.
Je nachdem wie viele Elemente die Folge besitzt, nennen wir die Reihe
- <span style="color: red;">*endlich*</span>, wenn die zugehörige Folge endlich ist, das heißt wenn wir nur eine endliche Anzahl an Zahlen zusammenaddieren. Ein Beispiel dafür ist die [die Summe der ersten n ungeraden Zahlen](https://visualproofs.github.io/series/algebra/2022/04/15/n-odd-numbers.html) und [die Summe von Gauss](https://visualproofs.github.io/series/2022/05/12/gauss.html).
- <span style="color: red;">*unendlich*</span>, wenn die zugehörige Folge kein Ende hat. Durch die Nutzung von Grenzwerten können wir herausfinden, ob die Reihe konvergiert (also sich einem bestimmten endlichen Wert annähert) oder das nicht tut; wir sagen dann, dass die Reihe divergiert.
Wir starten mit einem Beispiel!

### Holt die Pinsel raus: Wir bemalen eine Leinwand
Wir haben den Auftrag bekommen eine wunderschön leere, quadratische Leinwand zu bemalen.

![walking]({{ site.baseurl }}/assets/images/canvas.png)

Wir fangen an genau 1/4 des Quadrats blau anzumalen. Das Ganze sieht dann in etwa so aus.

![walking]({{ site.baseurl }}/assets/images/canvas1.png)

Als nächstes bemalen wir 1/16, also 1/4 von 1/4, der Fläche blau, was dann so ausschaut.

![walking]({{ site.baseurl }}/assets/images/canvas2.png)

Weiter geht's mit 1/64, also 1/4 von 1/16.

![walking]({{ site.baseurl }}/assets/images/canvas3.png)

Wir fahren nach diesem Muster fort und bemalen nun 1/4 * 1/64 = 1/256

![walking]({{ site.baseurl }}/assets/images/canvas4.png)

Danach bemalen wir wieder 1/4 der vorherigen Fläche, dieses Mal also 1/1024.

![walking]({{ site.baseurl }}/assets/images/canvas5.png)

Wir machen immer so weiter und bemalen im n-ten Schritt genau 1/4^n der Fläche blau.

Nach jedem Schritt haben wir genau 3 gleich große Quadrate von dem jeweils eins blau und die anderen beiden weiß sind. Im vierten Quadrat findet sich genau das selbe Muster im kleineren Maßstab, auch hier ist wieder eins der Quadrate blau und die anderen beiden weiß. Dieses Muster wiederholt sich unendlich und demnach haben wir am Ende genau 1/3 unserer Leinwand blau angemalt.
Dieses blaue Muster repräsentiert die inversen Potenzen der Zahl 4 und wir können daraus schließen, dass die Summe der inversen Potenzen von 4 im Grenzwert genau 1/3 ist.



### Versuch's selbst
Nutze den Schieber um zu sehen, wie sich der Malprozess mit jedem Schritt dem genannten Muster annähert.

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

### Die Mathematik dahinter

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