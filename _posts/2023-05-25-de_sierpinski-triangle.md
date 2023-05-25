---
layout: post
title:  "Sierpinski-Dreieck"
author: moritz
categories: Fractals
image: assets/images/sptriangle.png
---
Fraktale sind unregelmäßige selbstähnliche geometrische Formen. Das heißt Fraktale bestehen aus Mustern, in welche man unendlich reinzoomen und das selbe Muster auf kleinerer Ebene immer wiederentdecken kann. 
Sie können viele unregelmäßig geformte Objekte oder Phenomene in der Natur wie Küsten oder Bergketten beschreiben.

## Jetzt wo wir Fraktale kennen, was ist das Sierpinski-Dreieck?
Eins der bekanntesten Fraktale ist das sogenannnte Sierpinski-Dreieck. Die einfachste Art der Konstruktion funktioniert so: Man starte mit einem gleichseitigen Dreieck, was man in vier gleich große gleichseitige Dreiecke zerteilt. Nun entfernen wir das mittlere Dreieck, sodass nur noch drei Dreiecke übrig bleiben. Diese utnerteilen wir nun wiederum in je vier kleinere Dreiecke und entfernen das mittlere. So verfahren wir rekursiv weiter und wenden das selbe Verfahren für alle Dreiecke an.


Wacław Sierpiński war der erste Mathematiker, der über die Eigenschaften dieses Dreiecks nachdachte, aber das Muster selber findet sich schon in Kunststücken und Mosaiken viele Jahrhunderte vor ihm:

![walking]({{ site.baseurl }}/assets/images/collage.jpg)

### Die Dreieck-Entfern-Methode

Wie vorhin beschrieben lässt sich das Sierpinski-Dreieck durch wiederholtes Entfernen von Dreiecken aus einem ursprünglichen gleichseitigen Dreieck konstruieren.
1. Beginne mit einem gleichseitigen Dreieck.
2. Teile das Dreieck in vier gleichgroße Dreiecke und entferne das mittlere.
3. Wiederhole den 2. Schritt in den kleineren Dreiecken für immer und ewig.

#### Versuch es selbst
Wir visualisieren den Prozess und benutzen den Schieber, um den Konstruktionsprozess zu steuern:
<div id="observablehq-f40c7c08">
  <div class="observablehq-viewof-sierp_steps"></div>
  <div class="observablehq-sierp_approx"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/construction-of-the-serpinski-triangle.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof sierp_steps") return Inspector.into("#observablehq-f40c7c08 .observablehq-viewof-sierp_steps")();
    if (name === "sierp_approx") return Inspector.into("#observablehq-f40c7c08 .observablehq-sierp_approx")();
  });
</script>

### Das Chaosspiel

Das Chaosspiel ist eine Methode um Fraktale mithilfe von Polygonen zu generieren.

Wir erklären die Regeln am Beispiel eines gleichseitigen Dreiecks. Dieses hat drei Eckpunkte A, B und C. Wir starten das Chaosspiel an einem zufälligen Punkt P1 im Inneren des Dreiecks. Um die Position des nächsten Punkts P2 zu bestimmen, wählen wir zufällig einen der drei Eckpunkte des Dreiecks und legen den Punkt P2 in die Mitte zwischen P1 und dem zufällig ausgewählten Eckpunkt.
Wir wiederholen diesen Prozess und malen jeden Punkt auf.

Einige Bereiche des Dreiecks werden in späteren Schritten unerreichbar. Diese leeren Flächen entsprechen genau den Flächen, die wir aus dem Sierpinski-Dreieck herausgeschnitten haben.
So formen die Punkte nach und nach das Fraktal.


#### Versuch es selbst

Klick auf den Knopf um das Chaosspiel zu starten.
Du kannst das Chaosspiel von vorne beginnen lassen, um ein neues zufälliges Muster zu generieren.

<div id="observablehq-a077419d">
  <div class="observablehq-viewof-start"></div>
  <div class="observablehq-viewof-clear"></div>
  <div class="observablehq-canvas"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/construction-of-the-serpinski-triangle.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof start") return Inspector.into("#observablehq-a077419d .observablehq-viewof-start")();
    if (name === "viewof clear") return Inspector.into("#observablehq-a077419d .observablehq-viewof-clear")();
    if (name === "canvas") return Inspector.into("#observablehq-a077419d .observablehq-canvas")();
  });
</script>
