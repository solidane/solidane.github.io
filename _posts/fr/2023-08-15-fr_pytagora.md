---
layout: post
title:  "Théorème de Pythagore"
author: georges
categories: Geometry
image: assets/images/pytagora.jpeg
lang: fr
---
[Pythagore de Samos (570-495 av. J.-C.)] (https://fr.wikipedia.org/wiki/Pythagore) était un philosophe grec très influent, dont les travaux ont contribué à de nombreux domaines tels que la musique, la philosophie, l'astronomie et les mathématiques.
a contribué à de nombreux domaines tels que la musique, la philosophie, l'astronomie et les mathématiques, ces dernières incluant le célèbre théorème de Pythagore.

![walking]({{ site.baseurl }}/assets/images/pitagora.jpg)

Le théorème de Pythagore est un théorème géométrique fondamental et certainement très connu. Selon ce théorème, dans un triangle rectangle (dont l'un des angles est de 90°), l'hypoténuse (le côté le plus long, qui se trouve à l'opposé de l'angle de 90°) est égale à la racine carrée de la somme des aires des carrés des deux autres côtés.  


Ce théorème a de nombreuses applications, notamment dans les domaines de l'ingénierie et de la construction, de la reconnaissance faciale dans les caméras de sécurité, de la navigation et bien d'autres encore.

**À prouver:** Lorsqu'un triangle a un angle droit (90°) et que des carrés sont faits sur chacun des trois côtés, alors le plus grand carré a exactement la même surface que les deux autres carrés réunis !

### Visualisons l'énoncé ci-dessus
Nous dessinons un triangle rectangle et à côté des côtés du triangle, nous dessinons des carrés : 
- Un <math display="inline"><mn>3</mn><mo>&times;</mo><mn>3</mn></math> carré pour la hauteur (côté)
- Un <math display="inline"><mn>4</mn><mo>&fois;</mo><mn>4</mn></math> carré pour la largeur (côté)
- Un <math display="inline"><mn>5</mn><mo>&fois;</mo><mn>5</mn></math> carré pour l'hypoténuse. 

![walking]({{ site.baseurl }}/assets/images/pyta.png)

D'après le théorème, la somme des carrés des petits côtés doit être égale au carré de l'hypoténuse.

##### Est-ce le cas dans notre visualisation ?
Vérifions-le : Comptez les petits carrés des côtés, additionnez-les et comparez si la somme des côtés est égale à la somme des carrés de l'hypoténuse.
Vous devriez obtenir 9 + 16 = 25. 

### Essayez vous-même
Joue avec <math display="inline"><mi>a</mi></math> et <math display="inline"><mi>b</mi></math> vérifier la validité de ce théorème. Voyez comment les formes s'emboîtent les unes dans les autres, ce qui montre que ces zones sont de taille égale.
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

### Les mathématiques à l'œuvre
L'équation permettant d'exprimer le théorème dans un triangle rectangle est la suivante
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

où <math display="inline"><mi>a</mi></math> et <math display="inline"><mi>b</mi></math> représentent les cathéters, autrement dit les jambes adjacentes ou opposées de l'angle droit et <math display="inline"><mi>c</mi></math> est l'hypoténuse.