---
layout: post-de
title:  "Pizza Theorem"
author: moritz
categories: Geometry
image: assets/images/pizza.jpg
lang: de
---
Hey, ich hab uns was mitgebracht…

![walking]({{ site.baseurl }}/assets/images/pizza-above.jpg){:style="width: 60%"}

Ich habe eine Pizza gekauft, die wir uns teilen können! Wer mag schon Mathe auf leeren Magen? Ich muss sie nur kurz in Stücke schneiden...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-1.png){:style="width: 60%"}

Ups. Das schaut ja gar nicht gut aus! Die Schnitte sind alle schön regelmäßig, so dass alle acht Winkel zwischen den Schnitten genau 45° und damit gleich groß sind. Aber ihr Schnittpunkt liegt nicht im Zentrum der Pizza, deshalb sehen alle Stücke ziemlich komisch aus. Aber keine Angst: **Wenn wir reihum im Kreis um den Schnittpunkt gehen und wir uns mit den Stücken abwechseln, hat am Ende jeder von uns beiden gleich viel Pizza!**

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-filled-alt.png){:style="width: 60%"}

Diese Aussage ist auch bekannt als **Pizza Theorem**. Wer soll da noch sagen, dass Mathematik nichts mit der echten Welt zu tun hat? Und wir werden diese Aussage sogar zusammen beweisen!

## Der Beweis für das Pizza Theorem

Wie können wir zeigen, dass deine vier Stücke dieselbe Fläche haben wie meine vier? Die sehen ja ganz verschieden aus... In diesen Fällen kann es sinnvoll sein, noch mehr Linien zu konstruieren - oder die Pizza noch mehr zu zerschneiden - um mehrere Flächen zu erstellen, die eindeutig dieselbe Fläche einnehmen. Wir nennen zwei Formen **kongruent**, wenn sie genau die gleiche Form, Größe und Fläche haben. Eine gute Methode um kongruente Flächen zu erstellen, ist Symmetrien auszunutzen, zum Beispiel durch Spiegelungen. Und das machen wir auch hier! Wir nehmen die Schnittlinien und verschieben sie in das Zentrum der Pizza (hier in rot). Wenn wir den Schnittpunkt an diesen Linien spiegeln, entsteht ein Achteck (in schwarz).

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-mirror.png){:style="width: 60%"}

Wenn wir auch noch die ursprünglichen Schnitte spiegeln, erhalten wir die folgende zerteilte Pizza.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-2-alt.png){:style="width: 60%"}

Keine Panik! Das sieht zwar kompliziert aus, aber wir konzentrieren uns in jedem Schritt nur auf ein Mini-Stück und finden die anderen Mini-Stücke, die genauso ausschauen. Fangen wir doch mal mit dem hier an:

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-aa-alt.png){:style="width: 60%"}

Drei andere Stücke sehen so ähnlich aus. Kannst du sie finden?

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-a-alt.png){:style="width: 60%"}

Perfekt! Wir haben vier solche Stücke, alle vier perfekte Spiegelbilder voneinander und damit haben sie die selbe Fläche! Und schau, zwei von denen gehören mir und zwei gehören dir. Also isst davon jeder seinen Teil und dann haben wir beide bisher die selbe Menge Pizza abbekommen.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-b-alt.png){:style="width: 60%"}

Was ist als nächstes dran?

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-c-alt.png){:style="width: 60%"}

Hier sind diese dickeren Stücke, jeweils eins links und rechts von den Stücken, die wir gerade gegessen haben. Also gibt es davon insgesamt acht, und wieder vier für dich und vier für mich. Bon appetit!

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-e-alt.png){:style="width: 60%"}

Neben diesen dickeren Stücken, haben wir kleine Teile, die wie Dreiecke aussehen. Wiedermal gibt es acht davon, vier für mich und vier für dich. Mjam!

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-f-alt.png){:style="width: 60%"}

Wir machen so weiter und suchen kongruente Formen. Hier sind acht gleiche...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-g-alt.png){:style="width: 60%"}

…acht von denen...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-i-alt.png){:style="width: 60%"}

…und nochmal vier von denen hier.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-k-alt.png){:style="width: 60%"}

Jetzt sind wir schon fast fertig! Von den 12 größeren Dreiecken gibt es jeweils sechs für uns...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-m-alt.png){:style="width: 60%"}

…und nochmal 12 kleinere Dreiecke.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-o-alt.png){:style="width: 60%"}

Für den Rest mache ich noch einen extra Schnitt in rot.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-q-alt.png){:style="width: 60%"}

Dann kriegt jeder von uns ein trapezförmiges Teil.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-r-alt.png){:style="width: 60%"}

…drei kleine Dreiecke...

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-s-alt.png){:style="width: 60%"}

…und zum Schluss noch ein dünnes Trapez.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-t.png){:style="width: 60%"}

Und das war's! Zusammen haben wir die gesamte Pizza aufgegessen und in jedem Stück haben wir gleich viele Stücke der selben Größe bekommen!

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-u.png){:style="width: 60%"}

## Versuch es selbst
Klick auf den Schnittpunkt und halte ihn gedrückt, um ihn im Kreis herumzuziehen. So kannst du sehen, wie sich die Stücke verändern. Findest du die Stücke, die kongruent zueinander sind?

{% include pizza.html %}