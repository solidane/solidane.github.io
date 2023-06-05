---
layout: post
title:  "Fibonacci-Folge"
author: moritz
categories: Series
image: assets/images/fibospi.jpg
---
Eine **Folge** ist eine Liste von Zahlen oder Objekten in einer bestimmten <span style="color: purple;">*Reihenfolge*</span>, wobei Wiederholungen von Objekten erlaubt sind. Wir nennen Folgen <span style="color: red;">*endlich*</span>, wenn sie eine endliche Anzahl an Objekten umfassen. Sonst nennen wir sie <span style="color: red;">*unendlich*</span>.

Beispiele:
- {1, 2, 3, 4,...} - ist eine <span style="color: red;">*unendliche*</span> Folge der natürlichen Zahlen.
- {2, 4, 6, 8, 10} - ist eine <span style="color: red;">*endliche*</span> Folge der <span style="color: purple;">*ersten fünf*</span>  positiven geraden Zahlen.
- {Z, Y, X, W, V}  - ist eine <span style="color: red;">*endliche*</span> Folge der <span style="color: purple;">*letzten fünf*</span>  Buchstaben des Alphabets.
- {X, O, X, O,...} - ist eine <span style="color: red;">*unendliche*</span> Folge, die zwischen X und O alterniert.

### Was ist die Fibonacci-Folge?
Die **Fibonacci-Folge** ist eine Folge von Zahlen, wobei jedes Element als die Summe seiner beiden Vorgänger definiert ist. Normalerweise definieren wir die ersten beiden Elemente der Folge als 0 und 1, aber auch andere Starts sind möglich. Eine Folge mit diesem Anfang sähe wie folgt aus: 0, 1, 1, 2, 3, 5, 8, 13, ...

Die Fibonacci-Zahlen wurden von indischen Mathematikern bereits 200 v.Chr. entdeckt, aber zum ersten Mal vom italienischen Mathematiker [Leonardo of Pisa (1170-1240 n. Chr.)](https://de.wikipedia.org/wiki/Leonardo_Fibonacci) im 13. Jahrhundert eingeführt.

Die Fibonacci-Folge erscheint in der Natur sehr häufig. Die Blüten von Blumen, Fruchständen von Pflanzen, Muscheln oder Orkane folgen zumeist dem Muster der Fibonacci-Zahlen.
Anwendung findet diese berühmte Folge in verschiedensten Bereichen von Computerwissenschaften bis zu Fotografie, wo sie eng mit dem Phänomen des [Goldenen Schnitts](https://de.wikipedia.org/wiki/Goldener_Schnitt) verwandt ist.

Tausende von bezaubernden Mustern ergeben sich durch die Fibonacci-Folge.


![walking]({{ site.baseurl }}/assets/images/GoldenRatio.png)


### Wie können wir die Fibonacci-Folge visuell verstehen?
Beginnen wir mit zwei <math display="inline"><mn>1</mn><mo>&times;</mo><mn>1</mn></math>-Quadraten nebeneinander.
![walking]({{ site.baseurl }}/assets/images/fib1.png)

Zusammen ergeben diese ein <math display="inline"><mn>1</mn><mo>&times;</mo><mn>2</mn></math>-Rechteck. Bauen wir nun unterhalb ein <math display="inline"><mn>2</mn><mo>&times;</mo><mn>2</mn></math>-Quadrat an.
![walking]({{ site.baseurl }}/assets/images/fib2.png)

Neben dieses Gebilde kommt nun, entsprechend der Höhe, ein <math display="inline"><mn>3</mn><mo>&times;</mo><mn>3</mn></math>-Quadrat.
![walking]({{ site.baseurl }}/assets/images/fib3.png)
Darunter fügen wir als nächstes ein <math display="inline"><mn>5</mn><mo>&times;</mo><mn>5</mn></math>-Quadrat hinzu.
![walking]({{ site.baseurl }}/assets/images/fib5.png)
Zusammen ergibt dies ein gigantisches Rechteck. Nun die Frage:

##### Was ist die Fläche dieses Rechtecks?
Die offensichtlichste Antwort ist einfach die Flächen all dieser Quadrate zusammenzuaddieren. Aber da die finale Form ein Rechteck ist, können wir auch einfach seine Breite mit siner Höhe multiplizieren um die Fläche zu bestimmen: <math display="inline"><mrow><mn>5</mn><mo>&times;</mo><mo form="prefix" stretchy="false">(</mo><mn>5</mn><mo>+</mo><mn>3</mn><mo form="postfix" stretchy="false">)</mo><mo>=</mo><mn>5</mn><mo>&times;</mo><mn>8</mn></mrow></math>, wobei 8 auch die nächste Zahl in der Fibonacci-Folge ist.

Wenn wir so weitermachen erhalten wir Rechtecke der folgenden Größen:
- <math display="inline"><mrow><mn>8</mn><mo>&times;</mo><mn>13</mn></mrow></math> 
- <math display="inline"><mrow><mn>13</mn><mo>&times;</mo><mn>21</mn></mrow></math>
- <math display="inline"><mrow><mn>21</mn><mo>&times;</mo><mn>34</mn></mrow></math>
- <math display="inline"><mrow><mn>34</mn><mo>&times;</mo><mn>55</mn></mrow></math>
- <math display="inline"><mrow><mn>55</mn><mo>&times;</mo><mn>89</mn></mrow></math>

Wenn wir nun die längere Seitelänge des Rechtecks durch die kürzere dividieren, erhalten wir
- <math display="inline"><mrow><mn>13</mn><mo lspace="0.2222em" rspace="0.2222em">&divide;</mo><mn>8</mn><mo>=</mo><mn>1,625</mn></mrow></math>
- <math display="inline"><mrow><mn>21</mn><mo lspace="0.2222em" rspace="0.2222em">&divide;</mo><mn>13</mn><mo>=</mo><mn>1,615</mn></mrow></math>
- <math display="inline"><mrow><mn>34</mn><mo lspace="0.2222em" rspace="0.2222em">&divide;</mo><mn>21</mn><mo>=</mo><mn>1,619</mn></mrow></math>
- <math display="inline"><mrow><mn>55</mn><mo lspace="0.2222em" rspace="0.2222em">&divide;</mo><mn>34</mn><mo>=</mo><mn>1,6176</mn></mrow></math>
- <math display="inline"><mrow><mn>89</mn><mo lspace="0.2222em" rspace="0.2222em">&divide;</mo><mn>55</mn><mo>=</mo><mn>1,61818</mn></mrow></math>

Je größer unsere Rechtecke werden, desto näher kommen wir einem Wert von rund 1,618, der auch als goldener Schnitt bekannt ist.
### Versuch es selbst

Nutze den Schieber und untersuche wie das Rechteck anwächst.


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

### Die Mathematik dahinter
Die Formeln, um die Fibonacci-Folge zu generieren, lauten:

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

und

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

für <math display="inline"><mi>n</mi><mo>></mo><mn>1</mn></math>
