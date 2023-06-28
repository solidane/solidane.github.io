---
layout: post
title:  "Pizza theorem"
author: moritz
categories: Geometry
image: assets/images/pizza.jpg
lang: en
---
Hey, I brought something for us…

![walking]({{ site.baseurl }}/assets/images/pizza-above.jpg){:style="width: 60%"}

I’ve bought a pizza for us two to share! Who can do math with an empty stomach? Now, I only need to cut it into slices..

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-1.png){:style="width: 60%"}

Oops. Now that doesn’t look nice at all! I made all the cuts nice and regular so that the eight angles between the cuts are equally spaced and form a 45° angle. But I didn’t hit the center of the pizza at all, so now all the slices look really weird. But don’t worry: **If we go round the circle, you take every second slice and I take the rest, we will have exactly the same amount of pizza!**

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-filled-alt.png){:style="width: 60%"}

This is also known as the **Pizza theorem**. Who says math isn't useful in the real world? And we will even prove it together!

## Proving the pizza theorem

Now, how do we want to prove that your four slices together have the same area as my four slices? After all, they all look completely different. In these scenarios, it can be helpful to add a few more lines to your geometric construction - or cuts to your pizza - to create more shapes which clearly have the same area. We call two shapes **congruent** if they have the exact same form, size and area. A good way to create congruent shapes is by using symmetries, for example by mirroring some lines. That’s exactly what we are going to do! We take the cuts that we made and shift them to the center of the pizza (shown in red). Mirroring the cutting point along those lines give us an octagon (in black).

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-mirror.png){:style="width: 60%"}

If we also mirror the cuts we have made earlier, we get the following cut-up pizza.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-2-alt.png){:style="width: 60%"}

Don’t freak out! This looks very complicated but we will just concentrate on one mini-slice every time and find all the other mini-slices that look exactly like it. Let’s start with this one:

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-aa-alt.png){:style="width: 60%"}

There are three more parts like it. Can you find them?

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-a-alt.png){:style="width: 60%"}

Perfect! We have four of these shapes, all perfect mirror images of eachother and therefore, they have the same size. And look, two of these are part of your slices and two are part of mine. So let’s eat those and we’ll both have had the same amount of pizza so far.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-b-alt.png){:style="width: 60%"}

Let’s see what’s next.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-c-alt.png){:style="width: 60%"}

There are these thicker slices, one on each side of the four shapes we just ate. So we have eight in total and again, four of them are yours and four are mine. Bon appetit!

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-e-alt.png){:style="width: 60%"}

Next to the thicker slices, we have the bits that look like triangles. Again, there are eight of them, four belong to me and four are yours. Dinner time!

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-f-alt.png){:style="width: 60%"}

We continue this way, always finding congruent shapes. There are eight of these shapes…

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-g-alt.png){:style="width: 60%"}

…eight of these…

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-i-alt.png){:style="width: 60%"}

…and another four of these ones.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-k-alt.png){:style="width: 60%"}

Now we are almost done! There are 12 of the bigger triangles, six for both of us…

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-m-alt.png){:style="width: 60%"}

…and 12 smaller triangles.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-o-alt.png){:style="width: 60%"}

For the remaining bit, I will make one extra cut in red.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-q-alt.png){:style="width: 60%"}

Then, both of us get one large trapezoid…

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-r-alt.png){:style="width: 60%"}

…three small triangles…

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-s-alt.png){:style="width: 60%"}

…and finally one thinner trapezoid.

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-t.png){:style="width: 60%"}

And that’s it. We ate the entire pizza and in every step, we both got the same slices!

![walking]({{ site.baseurl }}/assets/images/pizza-sketch-u.png){:style="width: 60%"}

## Try it yourself
Grab and move the cutting point around in the circle and see how if you can find the congruent slices.

{% include pizza.html %}