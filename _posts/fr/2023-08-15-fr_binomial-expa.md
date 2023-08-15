---
layout: post
title:  "Expansion polynomiale"
author: georges
categories: Algebra
image: assets/images/poexe.png
lang: fr
---
Un **polynôme** est défini comme une expression composée de variables, de constantes et d'exposants, qui sont fusionnés à l'aide d'opérations mathématiques telles que l'addition, la soustraction, la multiplication et la division par des nombres.
D'autre part, une **expansion** d'un produit de sommes en mathématiques l'exprime comme une somme de produits en raison des propriétés distributives de la multiplication par rapport à l'addition.

Après avoir défini ces deux termes, nous pouvons maintenant répondre à la question suivante:
### Qu'est-ce qu'un développement polynomial?
Le développement d'un polynôme est une expression du même polynôme, où aucune variable n'apparaît entre parenthèses et où tous les termes identiques ont été combinés.

## Comment développer un polynôme?

Si nous avons une ou deux expressions à multiplier, nous pouvons facilement le faire manuellement. Mais qu'en est-il si nous avons une expression de la forme : <math display="inline"> <mrow> <mo form="prefix" stretchy="false">(</mo> <mn>3</mn> <mi>a</mi> <mo>+</mo> <mn>2</mn> <msup> <mo form="postfix" stretchy="false">)</mo> <mn>4</mn> </msup> </mrow> </math>.
Multiplier le tout 4 fois à la main prend du temps. 
</p> <p>Par chance, il existe quelques modèles que nous pouvons utiliser.</p> <p>

### Expansion avec le triangle de Pascal

Le triangle de Pascal a été nommé d'après le célèbre et révolutionnaire mathématicien français du XVIIe siècle [Blaise Pascal (1623-1662 AD)](https://fr.wikipedia.org/wiki/Blaise_Pascal).
Il s'agit d'une représentation visuelle triangulaire des coefficients binomiaux, qui sont essentiels pour développer les polynômes. Ce modèle était connu et pratiqué en Extrême-Orient et au Proche-Orient des siècles avant le monde occidental.

#### Comment construire un tel triangle
- Le triangle commence par un 1 au sommet et, en dessous, par un 1 à gauche et à droite. 
- Pour les rangées suivantes, chaque nombre est la somme des deux nombres qui le précèdent dans la rangée précédente.

#### Comment développer à l'aide du triangle?
Étant donné  <math display="inline"><mrow><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><msup><mo form="postfix" stretchy="false">)</mo><mi>n</mi></msup></mrow></math>
pour toute puissance <math display="inline"><mi>n</mi></math>, vous pouvez écrire le développement en utilisant les coefficients du triangle. 
Notez que pour écrire les coefficients pour toute puissance <math display="inline"><mi>n</mi></math>, vous devez regarder la ligne <math display="inline"><mi>n</mi><mo>+</mo><mn>1</mn></math> pour trouver les coefficients.

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

Ainsi, pour l'exemple ci-dessus <math display="inline"> <mrow> <mo form="prefix" stretchy="false">(</mo> <mn>3</mn> <mi>a</mi> <mo>+</mo> <mn>2</mn> <msup> <mo form="postfix" stretchy="false">)</mo> <mn>4</mn> </msup> </mrow> </math>,
il faudrait vérifier la 5ème ligne du triangle de Pascal pour trouver les coefficients, qui sont 1, 4, 6, 4, 1.
En connaissant les coefficients, nous pouvons transformer le polynôme de la classe de 4e en:

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

Il suffit alors de multiplier:

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

### Développement des polynômes du 2e degré avec plus de deux variables
Dans les exemples précédents, nous avons vu comment développer des binômes, mais que se passe-t-il si nous avons plus de deux variables? Dans ce cas, comment procéder?

Dans ce qui suit, nous allons essayer de prouver visuellement comment les polynômes du 2e degré peuvent être développés.


#### Jouons au détective ! Pouvez-vous repérer un motif?
<span style="color: red;">*Alerte spoiler:*</span> Consultez le post sur [La somme de <math display="inline"><mi>n</mi></math> entiers impairs](https://visualproofs.github.io/series/algebra/2023/08/15/fr_n-odd-numbers/)
et voir ce que nous avons utilisé pour représenter les nombres carrés.

Comme vous l'avez peut-être deviné, nous avons utilisé un carré. Par exemple, si nous voulons calculer la somme de deux variables <math display="inline"><mrow><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><msup><mo form="postfix" stretchy="false">)</mo><mn>2</mn></msup> </mrow> </math>
le résultat est le même que celui que l'on obtiendrait en calculant la surface d'un carré de hauteur et de largeur <math display="inline"><mi>a</mi><mo>+</mo><mi>b</mi></math>.

![walking]({{ site.baseurl }}/assets/images/Identity.png)

et en construisant un carré tel que celui présenté dans l'image ci-dessus, on peut visiblement voir que la surface est la somme de <math display="inline"><msup><mi>a</mi><mn>2</mn></msup></math>, <math display="inline"><msup><mi>b</mi><mn>2</mn></msup></math> and <math display="inline"><mrow><mn>2</mn><mi>a</mi><mi>b</mi></mrow></math>, qui prouve
l'identité algébrique:
<math display="block"><mrow><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><msup><mo form="postfix" stretchy="false">)</mo><mn>2</mn></msup><mo>=</mo><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><mo form="postfix" stretchy="false">)</mo><mo form="prefix" stretchy="false">(</mo><mi>a</mi><mo>+</mo><mi>b</mi><mo form="postfix" stretchy="false">)</mo><mo>=</mo><msup><mi>a</mi><mn>2</mn></msup><mo>+</mo><mn>2</mn><mi>a</mi><mi>b</mi><mo>+</mo><msup><mi>b</mi><mn>2</mn></msup></mrow></math>

### Essayez vous-même

Utilisez le curseur ci-dessous pour développer le carré pour différents nombres de variables.
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