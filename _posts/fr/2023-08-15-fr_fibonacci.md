---
layout: post
title:  "Séquence de Fibonacci"
author: georges
categories: Series
image: assets/images/fibospi.jpg
lang: fr
---
Une **séquence** est une liste de nombres ou d'objets dans un certain <span style="color: purple;">*ordre*</span>, où la répétition est autorisée.
Les séquences sont dites <span style="color: red;">*finies*</span> si elles ont un nombre limité d'objets et <span style="color: red;">*infinies*</span> dans le cas contraire.

Examples:
- {1, 2, 3, 4, ...} - est une <span style="color: red;">*infinite*</span> suite d'entiers naturels
- {2, 4, 6, 8, 10} - est une <span style="color: red;">*finite*</span> suite des <span style="color: purple;">*cinq premiers*</span> nombre pairs
- {Z, Y, X, W, V} - est une <span style="color: red;">*finite*</span> suite de <span style="color: purple;">*cinq les cinq dernières*</span>  lettres de l'alphabet anglais.
- {X, O, X, O, ...} - est une <span style="color: red;">*infinite*</span> séquence de X et O dans un ordre<span style="color: purple;">*alterné*</span>.

### Comment la suite de Fibonacci est-elle définie ?
La **séquence de Fibonacci** est une suite de nombres, où chaque nombre est déterminé comme la somme des deux précédents. 
Cette séquence commence généralement par 0 et 1 (les exemples suivants sont également basés sur ce principe), bien qu'il y ait d'autres modifications.  
Une telle séquence commencerait par 0, 1, 1, 2, 3, 5, 8, 13... et se poursuivrait ainsi à l'infini.

Les nombres de Fibonacci ont été mentionnés par des mathématiciens indiens dès 200 avant J.-C., mais c'est Léonard de Pise qui les a introduits pour la première fois dans les mathématiques occidentales au 13e siècle.

Les nombres de Fibonacci apparaissent très souvent dans le monde naturel. Le nombre de pétales d'une fleur, les têtes de graines, les coquillages et même les ouragans suivent souvent des schémas conformes aux nombres de Fibonacci.
Cette célèbre séquence trouve des applications dans de nombreux départements, de l'informatique à la photographie, où elle est également fortement corrélée à ce que l'on appelle le "nombre de Fibonacci".
fortement corrélée à ce que nous appelons le [nombre d'or] (https://fr.wikipedia.org/wiki/Nombre_d%27or). 

Les nombres de Fibonacci sont à l'origine de nombreux modèles numériques magnifiques.

![walking]({{ site.baseurl }}/assets/images/GoldenRatio.png)


### Comment comprendre visuellement ces nombres
Commençons par placer deux <math display="inline"><mn>1</mn><mo>&times;</mo><mn>1</mn></math> carrés l'un à côté de l'autre. 
![walking]({{ site.baseurl }}/assets/images/fib1.png)

Nous obtenons ainsi un <math display="inline"><mn>1</mn><mo>&fois;</mo><mn>2</mn></math> rectangle. En dessous, plaçons un <math display="inline"><mn>2</mn><mo>&fois;</mo><mn>2</mn></math> carré pour que les longueurs des côtés adjacents correspondent.
![walking]({{ site.baseurl }}/assets/images/fib2.png)

Et à côté, un <math display="inline"><mn>3</mn><mo>&times;</mo><mn>3</mn></math> carré
![walking]({{ site.baseurl }}/assets/images/fib3.png)
En dessous, un <math display="inline"><mn>5</mn><mo>&fois;</mo><mn>5</mn></math> carré
![walking]({{ site.baseurl }}/assets/images/fib5.png)
Nous avons maintenant créé un rectangle géant. Laissez-moi maintenant vous poser une question :

##### Quelle est l'aire du rectangle final ?
La réponse la plus triviale serait la somme des aires de tous les carrés à l'intérieur du rectangle. Mais comme il s'agit d'un rectangle 
Mais comme il s'agit d'un rectangle, nous pouvons également multiplier la base et la hauteur pour obtenir l'aire totale, qui serait la suivante <math display="inline"><mrow><mn>5</mn><mo>&times;</mo><mo form="prefix" stretchy="false">(</mo><mn>5</mn><mo>+</mo><mn>3</mn><mo form="postfix" stretchy="false">)</mo><mo>=</mo><mn>5</mn><mo>&times;</mo><mn>8</mn></mrow></math>
, le 8 étant également le prochain nombre de Fibonacci de la séquence.

Si nous continuons ainsi, nous générerons des rectangles des formes suivantes :
- <math display="inline"><mrow><mn>8</mn><mo>&times;</mo><mn>13</mn></mrow></math> 
- <math display="inline"><mrow><mn>13</mn><mo>&times;</mo><mn>21</mn></mrow></math>
- <math display="inline"><mrow><mn>21</mn><mo>&times;</mo><mn>34</mn></mrow></math>
- <math display="inline"><mrow><mn>34</mn><mo>&times;</mo><mn>55</mn></mrow></math>
- <math display="inline"><mrow><mn>55</mn><mo>&times;</mo><mn>89</mn></mrow></math>

En divisant la longueur du côté le plus grand par la longueur du côté le plus petit, on obtient.. :
- <math display="inline"><mrow><mn>13</mn><mo lspace="0.2222em" rspace="0.2222em">&divide;</mo><mn>8</mn><mo>=</mo><mn>1.625</mn></mrow></math>
- <math display="inline"><mrow><mn>21</mn><mo lspace="0.2222em" rspace="0.2222em">&divide;</mo><mn>13</mn><mo>=</mo><mn>1.615</mn></mrow></math>
- <math display="inline"><mrow><mn>34</mn><mo lspace="0.2222em" rspace="0.2222em">&divide;</mo><mn>21</mn><mo>=</mo><mn>1.619</mn></mrow></math>
- <math display="inline"><mrow><mn>55</mn><mo lspace="0.2222em" rspace="0.2222em">&divide;</mo><mn>34</mn><mo>=</mo><mn>1.6176</mn></mrow></math>
- <math display="inline"><mrow><mn>89</mn><mo lspace="0.2222em" rspace="0.2222em">&divide;</mo><mn>55</mn><mo>=</mo><mn>1.61818</mn></mrow></math>
      
Au fur et à mesure que nous avançons, nous nous rapprochons de 1,618034... connu par beaucoup comme le nombre d'or.

### Essayez vous-même

Utilisez la barre de défilement ci-dessous pour découvrir comment le motif s'agrandit avec l'ajout de carrés.


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

### Les mathématiques à l'œuvre
La formule utilisée pour générer une telle séquence est la suivante
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

et

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

pour <math display="inline"><mi>n</mi><mo>></mo><mn>1</mn></math>.
