---
layout: post
title:  "Die Summe von n ungeraden Zahlen"
author: moritz
categories: [Series, Algebra]
image: assets/images/oddn.jpg
lang: de

---
{% include reading-time.html %}

Ungerade Zahlen sind alle ganzen Zahlen, die beim Teilen durch 2 einen Rest lassen.
Für eine natürliche Zahl <math display="inline"><mi>n</mi></math> hat die <math display="inline"><mi>n</mi></math>-te natürliche Zahl die Form <math display="inline"><mn>2</mn><mi>n</mi><mo>-</mo><mn>1</mn></math>. Das gibt uns dann die bekannte Folge 1, 3, 5, 7, 9, 11, ...

Nun die Frage: Was ist die Summe der ersten <math display="inline"><mi>n</mi></math> ungeraden Zahlen?

## Muster entdecken

Starten wir mit ein paar kleinen Beispielen
- die Summer der ersten beiden ungeraden Zahlen: 1 + 3 = 4   
- die Summe der ersten drei ungeraden Zahlen: 1 + 3 + 5 = 9 
- die Summe der ersten vier ungeraden Zahlen: 1 + 3 + 5 + 7 = 16

#### Siehst du das Muster? 
Falls es dir noch nicht aufgefallen ist: Es sieht so aus als wäre die Summe der ersten <math display="inline"><mi>n</mi></math> ungeraden Zahlen genau <math display="inline"> <msup> <mi>n</mi> <mn>2</mn> </msup> </math>. 
Können wir zeigen, dass dieses Muster auch für größere Summen gilt?

#### Hängt die Summe von ungeraden Zahlen mit den Quadratzahlen zusammen?
Das Muster hält bereits für die ersten drei Beispiele, aber wir müssen noch zeigen, dass es auch allgemein gilt und nicht einfach ein Zufall war.

Überlegen wir mal, wie wir die <math display="inline"><mi>n</mi></math>-te Quadratzahl darstellen können. Natürlich mit einem Quadrat, dessen Breite und Höhe genau <math display="inline"><mi>n</mi></math> enstpricht.

Nehmen wir also die ersten beiden ugneraden Zahlen, 1 und 3, und fügen sie zu einem Quadrat zusammen:

![walking]({{ site.baseurl }}/assets/images/4cube.png)

Da wir nach einem Quadrat für die zweite Quadratzahl <math display="inline"> <msup> <mi>2</mi> <mn>2</mn> </msup> </math> suchen, können wir die 4 Blöcke wie folgt zusammenfügen:

![walking]({{ site.baseurl }}/assets/images/4cube2.png)

Das passt tatsächlich, schließlich besteht unser Quadrat mit Breit 2 aus genau 4 Blöcken.

Fügen wir nun die nächste ugnerade Zahl, 5, zu unseren Blöcken hinzu.
![walking]({{ site.baseurl }}/assets/images/45Cubes.png)

Wenn wir versuchen alles zu einem Quadrat zu ergänzen, sieht es wie folgt aus.
![walking]({{ site.baseurl }}/assets/images/9cube.png)

Wenn wir die nächste ungerade Zahl haben wollen, müssen wir 2 zur letzten ungeraden Zahl addieren. Gleichzeitig brauchen wir in jedem Schritt zwei Blöcke mehr, um zum nächst-größeren Quadrat zu gelangen. Obwohl wir diese Idee nur für <math display="inline"><mi>n</mi><mo>=</mo><mn>3</mn></math> aufgemalt haben, bleibt dieses Muster auch für größere Zahlen bestehen!

### Versuch es selbst

Benutze den Schieber um verschiedene Werte für <math display="inline"><mi>n</mi></math> auszuprobieren.
<div id="observablehq-98f591e4">
  <div class="observablehq-viewof-n"></div>
  <div class="observablehq-aba"></div>
  <div class="observablehq-sumOfOdd"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/geometric-intuition-for-sum-of-first-n-odd-numbers.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof n") return Inspector.into("#observablehq-98f591e4 .observablehq-viewof-n")();
    if (name === "aba") return Inspector.into("#observablehq-98f591e4 .observablehq-aba")();
    if (name === "sumOfOdd") return Inspector.into("#observablehq-98f591e4 .observablehq-sumOfOdd")();
  });
</script>

## Die Mathematik dahinter

Die Formel zu diesem Muster lautet:

<math display="block" xmlns="http://www.w3.org/1998/Math/MathML">
  <mrow>
    <munderover>
      <mo>∑</mo>
      <mrow>
        <mi>i</mi>
        <mo>=</mo>
        <mn>1</mn>
      </mrow>
      <mi>n</mi>
    </munderover>
    <mrow>
      <mo stretchy="true" form="prefix">(</mo>
      <mn>2</mn>
      <mi>i</mi>
      <mo>-</mo>
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

