---
layout: post
title:  "La somme de n entiers impairs"
author: georges
categories: [Series, Algebra]
image: assets/images/oddn.jpg
lang: fr
---
Les nombres impairs sont tous les entiers qui ont un reste de un lorsqu'ils sont divisés par deux.
Si <math display="inline"><mi>n</mi></math> est un nombre entier, la forme générale d'un nombre impair serait <math display="inline"><mn>2</mn><mi>n</mi><mo>-</mo><mn>1</mn></math>, et de tels nombres seraient : 1, 3, 5, 7, 9, 11, 13...

La somme des <math display="inline"><mi>n</mi></math> entiers impairs n'est rien d'autre que la sommation (l'addition) d'une série de nombres impairs commençant à 1 jusqu'à un certain <math display="inline"><mi>n</mi></math>. 


## Découvrir des modèles

Commençons par de petits nombres et additionnons-les :
- les 2 premiers nombres impairs. 1 + 3 = 4   
- les 3 premiers nombres impairs : 1 + 3 + 5 = 9 
- les 4 premiers nombres impairs : 1 + 3 + 5 + 7 = 16

#### Voyez-vous une tendance se dessiner ? 
Si vous ne l'avez pas encore remarqué, ce schéma indique que si nous additionnons les premiers <math display="inline"> <mi>n</mi></math> nombres impairs, le résultat est <math display="inline"> <msup> <mi>n</mi> <mn>2</mn> </msup> </math>. 
Il se peut que nous soyons sur la bonne voie, vérifions si ce modèle est valable.

#### Les sommes des nombres impairs sont-elles liées aux nombres carrés ?
Jusqu'à présent, le modèle semble prometteur, mais nous devons encore nous assurer qu'il ne s'agit pas d'une simple coïncidence.

Réfléchissons aux différentes façons de représenter les nombres carrés. Un candidat trivial et très logique serait un carré de largeur et de hauteur égales.

Prenons par exemple les deux premiers nombres impairs, 1 et 3, et représentons-les par des ensembles de carrés :

![walking]({{ site.baseurl }}/assets/images/4cube.png)

Puisque nous cherchons une représentation visuelle de <math display="inline"> <msup> <mi>2</mi> <mn>2</mn> </msup> </math>, dans ce cas, la représentation la plus utile de 4 blocs serait la suivante :

![walking]({{ site.baseurl }}/assets/images/4cube2.png)

Cette représentation convient parfaitement puisque notre carré de largeur 2 est constitué de 4 briques.

Ajoutons le nombre impair suivant, 5, aux blocs existants.
![walking]({{ site.baseurl }}/assets/images/45Cubes.png)

Si nous essayons de l'ajouter gentiment au premier carré, cela ressemblerait à ceci :
![walking]({{ site.baseurl }}/assets/images/9cube.png)

Pour atteindre le nombre impair suivant, il suffit d'ajouter 2 au nombre impair précédent. De même, à chaque étape, nous avons besoin de 2 briques de plus qu'auparavant pour atteindre la case suivante. Bien que nous n'ayons illustré cela que pour <math display="inline"><mi>n</mi><mo>=</mo><mn>3</mn></math>, nous pouvons voir que ce modèle est valable !

### Essayez vous-même

Utilisez le curseur ci-dessous pour le tester pour différentes valeurs de <math display="inline"><mi>n</mi></math>.
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

### Les mathématiques à l'œuvre
La formule pour calculer ce modèle est la suivante
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

