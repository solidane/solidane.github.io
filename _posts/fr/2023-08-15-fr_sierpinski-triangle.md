---
layout: post
title:  "Triangle de Sierpinski"
author: georges
categories: Fractals
image: assets/images/sptriangle.png
lang: fr
---
Les fractales sont des formes géométriques irrégulières et autosimilaires. 
En d'autres termes, une fractale est un motif qui, lorsque l'on zoome, fait apparaître des motifs similaires à toutes les échelles inférieures. Les fractales peuvent être considérées comme des motifs sans fin.
Elles sont capables de décrire de nombreux objets de forme irrégulière ou des phénomènes naturels non uniformes dans l'espace, tels que les côtes et les chaînes de montagnes.


## Maintenant que nous savons ce que sont les fractales, qu'est-ce que le triangle de Sierpinski ?
L'un des exemples les plus connus de fractales est le triangle de Sierpinski. La façon la plus simple de construire un tel triangle est de commencer par un triangle équilatéral. Nous divisons ensuite ce triangle en quatre triangles équilatéraux plus petits et nous enlevons la copie centrale pour construire une forme composée de trois triangles. C'est ce qu'on appelle la première approximation du triangle de Sierpinski. Nous procédons ensuite de manière récursive en appliquant la même procédure à ces triangles, ce qui crée des triangles plus petits auxquels nous appliquons à nouveau cette procédure, et ainsi de suite. 

[Wacław Sierpiński (1828-1969 AD)](https://fr.wikipedia.org/wiki/Wac%C5%82aw_Sierpi%C5%84ski) a été le premier mathématicien à réfléchir aux propriétés de ce triangle, mais on retrouve ce schéma dans des œuvres d'art, des motifs et des mosaïques datant de plusieurs siècles, comme dans les images ci-dessous :

![walking]({{ site.baseurl }}/assets/images/collage.jpg)

### Méthode d'élimination des triangles

Le triangle de Sierpinski peut être construit à partir d'un triangle équilatéral par élimination répétée de sous-ensembles triangulaires :
1. Commencez par un triangle équilatéral.
2. Subdivisez-le en quatre petits triangles équilatéraux congruents et retirez le triangle central.
3. Répétez l'étape 2 avec les plus petits triangles pour toujours


#### Essayez par vous-même
Nous pouvons visualiser ce processus en utilisant le curseur pour contrôler l'étape de la construction ci-dessous :
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

### Le jeu du chaos

Le jeu du chaos est une méthode pour générer des fractales à l'aide de polygones.

Les règles seront expliquées à l'aide de l'exemple d'un triangle. Il a les points d'angle $$A$$, $$B$$ et $$C$$. Vous commencez le jeu du chaos à un point aléatoire $$P_1$$ à l'intérieur du triangle. Pour calculer la position suivante $$P_2$$, vous choisissez au hasard l'un des trois points d'angle du triangle et placez $$P_2$$ au milieu de la route entre le point $$P_1$$ et le point d'angle choisi au hasard. 
Vous répétez ce processus autant de fois que vous le souhaitez et dessinez à l'écran tous les points que vous obtenez.

Certaines zones du triangle sont inaccessibles lors des étapes suivantes. 
Ces zones forment un motif fractal. Seules les premières étapes permettent d'atteindre ces zones, tous les autres points se situant entre les deux.

#### Essayez par vous-même

Cliquez sur le bouton démarrer pour générer un tel triangle.
Vous pouvez redémarrer pour régénérer le triangle différemment.
Cliquez sur le bouton Effacer pour réinitialiser la simulation.
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
