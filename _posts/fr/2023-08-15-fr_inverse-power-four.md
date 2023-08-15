---
layout: post
title:  "Somme des puissances inverses de quatre"
author: georges
categories: [Series, Fractals]
image: assets/images/powerofi4.png
lang: fr
---
En mathématiques, une **série** est la somme de plusieurs nombres, dont le nombre peut être fini ou même infini. L'ensemble des nombres dont on fait la somme forme ce que l'on appelle une **série**.
Combien d'éléments contient la séquence?
- S'il s'agit d'une séquence <span style="color : red ;">*finie*</span>, cela signifie que nous avons un nombre limité d'éléments sur lesquels nous faisons la somme, la somme de cette séquence est une suite<span style="color: red;">*finie*</span>.  **Example**: [La somme des <math display="inline"><mi>n</mi></math> nombres entiers impairs](https://visualproofs.github.io/series/algebra/2023/08/15/fr_n-odd-numbers/) et [Somme de Gauss](https://visualproofs.github.io/series/2023/08/15/fr_gauss/)
- Alternativement, une série <span style="color: red;">*infinite*</span> est le résultat de l'addition d'une séquence de nombres <span style="color: red;">*infinie*</span>. L'utilisation de la limite permet de déterminer si une série infinie
converge ou diverge. Prenons un exemple!

### Prenez votre peinture et vos pinceaux! Nous peignons une toile
Nous commençons par une toile vide et carrée,

![walking]({{ site.baseurl }}/assets/images/canvas.png)

et nous voulons peindre <math display="inline"><mfrac><mn>1</mn><mn>4</mn></mfrac></math> en bleu:

![walking]({{ site.baseurl }}/assets/images/canvas1.png)

Nous obtenons donc quelque chose comme ceci. Maintenant, nous voulons peindre un autre <math display="inline"><mfrac><mn>1</mn><mn>16</mn></mfrac></math> en bleu:

![walking]({{ site.baseurl }}/assets/images/canvas2.png)

Voici le résultat. Nous avons donc peint en plus <math display="inline"><mfrac><mn>1</mn><mn>4</mn></mfrac></math> de <math display="inline"><mfrac><mn>1</mn><mn>4</mn></mfrac></math> de la toile originale. Nous poursuivons avec <math display="inline"><mfrac><mn>1</mn><mn>64</mn></mfrac></math>:

![walking]({{ site.baseurl }}/assets/images/canvas3.png)

Nous peignons ensuite <math display="inline"><mfrac><mn>1</mn><mn>4</mn></mfrac><mo>&times;</mo><mfrac><mn>1</mn><mn>64</mn></mfrac><mo>=</mo><mfrac><mn>1</mn><mn>256</mn></mfrac></math>.

![walking]({{ site.baseurl }}/assets/images/canvas4.png)

Ensuite, nous peignons en bleu un autre <math display="inline"><mfrac><mn>1</mn><mn>1024</mn></mfrac></math>:

![walking]({{ site.baseurl }}/assets/images/canvas5.png)

On peut continuer comme ça, à peindre en bleu <math display="inline"><msup><mrow><mfrac><mn>1</mn><mn>4</mn></mfrac></mrow><mi>n</mi></msup></math> de la surface à chaque étape.

Après chaque étape, nous avons trois carrés identiques, dont l'un est entièrement peint en bleu et les deux autres sont laissés en blanc. À la quatrième étape, le motif se répète à une échelle plus petite, nous avons à nouveau un carré bleu et deux carrés blancs. Ce schéma se poursuit à l'infini, de sorte que pour chaque échelle, il y a un carré bleu et deux carrés blancs. Au total, nous avons donc peint <math display="inline"><mfrac><mn>1</mn><mn>3</mn></mfrac></math> la toile en bleu.
Le motif bleu représente la somme des puissances inverses de quatre, et nous pouvons donc conclure que la somme des puissances inverses de quatre converge vers <math display="inline"><mfrac><mn>1</mn><mn>3</mn></mfrac></math>.


### Essayez vous-même
Utilisez le curseur ci-dessous pour voir comment le tableau converge vers le modèle susmentionné pour différentes valeurs de <math display="inline"><mi>n</mi></math>.

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

### Les mathématiques à l'œuvre
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
    <mo>+</mo>
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
    <mrow>
    <mo stretchy="false" form="prefix">(</mo>
    <mfrac>
      <mn>1</mn>
      <mn>4</mn>
    </mfrac>
    <msup>
    <mo stretchy="false" form="prefix">)</mo>  
    <mi>i</mi>
    </msup>
    </mrow>
    <mo>=</mo>
    <mfrac>
      <mn>1</mn>
      <mn>3</mn>
    </mfrac>
  </mrow>
</math>