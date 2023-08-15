---
layout : post
title :  "Théorème de la pizza"
author : georges
catégories : Geometry
image : assets/images/pizza.jpg
lang : fr
---
Hé, j'ai apporté quelque chose pour nous...

![walking]({{ site.baseurl }}/assets/images/pizza-above.jpg){:style="width : 60%"}

J'ai acheté une pizza à partager pour nous deux! Qui peut faire des maths l'estomac vide? Il ne me reste plus qu'à la découper en tranches...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-1.png){:style="width : 60%"}

Oups. Ça n'a pas l'air joli du tout! J'ai fait toutes les coupes de manière régulière, de sorte que les huit angles entre les coupes sont également espacés et forment un angle de 45°. Mais je n'ai pas du tout touché le centre de la pizza, ce qui fait que toutes les parts ont l'air vraiment bizarres. Mais ne vous inquiétez pas: **si nous faisons le tour du cercle, que vous prenez une part sur deux et que je prends le reste, nous aurons exactement la même quantité de pizza!**.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-filled-alt.png){:style="width : 60%"}

C'est ce qu'on appelle aussi le **théorème de la pizza**. Qui a dit que les mathématiques n'étaient pas utiles dans le monde réel? Et nous allons même le prouver ensemble!

## Prouver le théorème de la pizza

Comment prouver que vos quatre tranches ont la même surface que mes quatre tranches? Après tout, elles ont toutes l'air complètement différentes. Dans ce cas, il peut être utile d'ajouter quelques lignes à votre construction géométrique - ou de découper votre pizza - afin de créer davantage de formes ayant clairement la même surface. Deux formes sont dites **congruentes** si elles ont exactement la même forme, la même taille et la même surface. Une bonne façon de créer des formes congruentes est d'utiliser des symétries, par exemple en faisant miroiter certaines lignes. C'est exactement ce que nous allons faire! Nous prenons les coupes que nous avons faites et nous les déplaçons vers le centre de la pizza (en rouge). En réfléchissant le point de coupe le long de ces lignes, nous obtenons un octogone (en noir).

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-mirror.png){:style="width : 60%"}

Si nous reflétons également les coupes que nous avons effectuées précédemment, nous obtenons la pizza découpée suivante.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-2-alt.png){:style="width : 60%"}

Ne paniquez pas ! Cela semble très compliqué, mais nous allons nous concentrer sur une mini-tranche à chaque fois et trouver toutes les autres mini-tranches qui lui ressemblent exactement. Commençons par celle-ci:

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-aa-alt.png){:style="width : 60%"}

Il y a trois autres parties comme celle-ci. Pouvez-vous les trouver?

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-a-alt.png){:style="width : 60%"}.

Parfait! Nous avons quatre de ces formes, qui sont toutes des images miroir parfaites les unes des autres et qui ont donc la même taille. Et regardez, deux d'entre elles font partie de vos tranches et deux font partie des miennes. Mangeons-les et nous aurons tous les deux mangé la même quantité de pizza jusqu'à présent.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-b-alt.png){:style="width : 60%"}

Voyons la suite.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-c-alt.png){:style="width : 60%"}

Il y a ces tranches plus épaisses, une de chaque côté des quatre formes que nous venons de manger. Nous en avons donc huit au total et, encore une fois, quatre d'entre elles sont les vôtres et quatre sont les miennes. Bon appétit!

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-e-alt.png){:style="width : 60%"}

À côté des tranches plus épaisses, nous avons les morceaux qui ressemblent à des triangles. Là encore, il y en a huit, quatre m'appartiennent et quatre sont à vous. C'est l'heure du dîner!

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-f-alt.png){:style="width : 60%"}

Nous continuons ainsi, en trouvant toujours des formes congruentes. Ces formes sont au nombre de huit...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-g-alt.png){:style="width : 60%"}

...huit d'entre eux...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-i-alt.png){:style="width : 60%"}

...et quatre autres de ce type.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-k-alt.png){:style="width : 60%"}

Nous avons presque terminé ! Il y a 12 des plus grands triangles, six pour nous deux...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-m-alt.png){:style="width : 60%"}

...et 12 triangles plus petits.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-o-alt.png){:style="width : 60%"}

Pour la partie restante, je ferai une coupe supplémentaire en rouge.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-q-alt.png){:style="width : 60%"}

Ensuite, nous obtenons tous les deux un grand trapèze...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-r-alt.png){:style="width : 60%"}

...trois petits triangles...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-s-alt.png){:style="width : 60%"}

...et enfin un trapèze plus fin.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-t.png){:style="width : 60%"}

Et c'est tout. Nous avons mangé toute la pizza et à chaque étape, nous avons eu les mêmes parts!

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-u.png){:style="width : 60%"}

## Essayez vous-même
Saisissez et déplacez le point de coupe dans le cercle et voyez si vous pouvez trouver les tranches congruentes.

{% include pizza.html %}