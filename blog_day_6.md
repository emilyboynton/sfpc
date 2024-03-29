# Code Societies 

###  Origami II

Monday, Feb. 11 • Class 6 
Robby Kraft


_This class will be covered in three parts. The first section is all about the hard parts of origami, beginning with the frontiers of origami: curved creases and crumpling. We'll discuss what makes this hard and and why there are unsolved problems. Discuss what is easily solvable leads us into origami software and we'll take a look under the hood of Rabbit Ear. Again, we'll look at some difficult problems in origami software and what makes them hard. We'll end this section with a demonstration of how to create a crease pattern in code and render it in Origami Simulator_.

_The second component begins with an introduction to origami tessellations, followed by a workshop where we create our own tiling. Students will be able to prototype a design and perform their own foldability tests_.

_The final component is an introduction to rigid folding and a look at software by Tomohiro Tachi: Freeform Origami, and Origamizer. We'll look at the "algorithm that can make anything" (Tachi, Demaine), and an exercise in a collapsable cardboard creation_.


For our second and final origami class, we covered a lot of material with Robby. We looked at contemporary origami techniques, we examined the mathematical principles found in crease patterns, and we talked about how to problem solve and approach creating our own patterns. What I appreciated the most about this class is that although we covered a lot of information, I found that my two biggest takeaways from this class were that we were building our intuition for origami construction and that we were lined up with the tools and resources to keep learning and to create our own patterns even after our session ends.

#### Contemporary Techniques

Robby started class with a quick gluing paper demonstration and a walk-through of how to use the Cricut. I know, I know, "gluing paper", sounds like it would be listed right at the top of "Origami Don'ts." However! The technique that Robby demonstrated--using methyl cellulose to afix a sheet of unryu to watercolor paper--is on the "Totally Fine" list. This is simply a technique to create a double-sided piece of paper which allows the artist to add an element of color and texture to their origami. 

Robby also walked us through how to use the Cricut machine. Since so much of contemporary origami uses computer generated patterns, curved creases, and intricate, precise folds, a Cricut proves to be incredibly useful as it is able to lightly score whatever pattern you send it. That said, we also talked about the [types of software](https://github.com/robbykraft/SVG) and solutions we can use to bridge the gap between the math the crease pattern might demand and the capabilities of Illustrator (e.g. Illustrator can't produce accurate sine curves).


![Robby Gluing Paper](images/robby_1.jpg) | 
:-----------------------------: |
Gluing Paper Demonstration

#### Curved Creases

Our class was _very_ excited to cover [curved creases](http://erikdemaine.org/curved/history/). Personally, I had already found myself drawn to a variety of curved crease structures and artists over course of Week 1. Some of my fascinations included, the movement and dynamism of Erik and Martin Demaine's [sculptures](http://erikdemaine.org/curved/FullerCraft/); David Huffman's [striking work](https://erikdemaine.org/papers/Huffman_Origami5/paper.pdf), where a few hyper-clean, curved folds can render paper surreal; the [figural works of Giang Dinh](https://giangdinh.com/portfolio/), which showcase narrative and emotion through the simple lines of curved creases and wet folding; and finally, the pleated, sweeping, and modular works of [Richard Sweeney](https://www.richardsweeney.co.uk/works). 

In order to help us think about properties of curved creases, we watched a small part of a [talk delivered by Jun Mitani](https://www.youtube.com/watch?v=Aq9b_HelQ3E) where he explains how a number of designs are based on mirror reflections of conics. [David Huffman](https://en.wikipedia.org/wiki/David_A._Huffman), claimed that all of his creases were conics. Having these ideas in mind when folding is definitely helpful as you can imagine the paper fitting to a shape, rather than just looking at the crease itself.

For curved creases to try, we were given two patterns: the first, a small Huffman pattern with two curved lines, and the second, a donut-shaped paper with a series of concentric circles. Both of these patterns were scored by the Cricut. The circular pattern we were given has origins in the Bauhaus as the result of a paper study. When folded tightly enough in alternating mountain and valley folds, the pattern will want to flip in on itself, creating a dynamic, twisted-looking shape.

Some Tips!
* Whenever making a new crease, flatten all other creases
* Imagine the crease fitting to either a cylinder or a cone
* Work in small sections and start folding at small degrees
* Watercolor paper works well


![Huffman](images/huffman.jpg) | 
:-----------------------------: |
Curved Crease Patterns


#### Flat-Foldability

One of my favorite parts of this class was when Robby introduced the concept of flat-foldability. Flat-foldability, unsurprisingly, describes the ability of a crease pattern to be flattened but not damaged. I appreciated this section of the class so much because by doing a few simple folding exercises, examining two theorems of flat-foldability, and by noting where we had already seen examples of these theorems, we were able to build our intuition and understanding of paper folding principles. 

The first mini-exercise that we did was to take a piece of paper and bring three mountain folds together at a single vertex. By pinching around the vertex so that the creases start to form something more "flap"-like, we could then choose any of the three to fold down. However, to make it flat, we need to add one valley crease. This new fold radiates from the same vertex, but unlike our other folds, this last one seems to decide for itself where it lies. With that in mind, Robby then prompted us to unfold our paper to examine and extract information from our new crease patterns (three mountain, one valley). This exercise and observation was our introduction to Kawasaki's theorem, stating that sum of each set of alternating angles is 180. We could clearly this to be true in our own examples and then again when we tried to fold down a different flap or recreate the exercise with three new folds at a different angles.

That exercise also provided the perfect example for introducing Maekawa's Theorem of flat-foldability. This second theorem states that in any given flat-foldable vertex, the number of mountain creases and the number of valley creases will always differ by two. For me this also helped inform my understanding of Kawasaki's theorem (i.e. there will always be an even number of folds, and therefore an even number of angles to create sums). For our second mini-exercise, we took another piece of paper and vertically smashed in an effort to demonstrate that we could easily find evidence of Maekawa's Theorem in even "naturally occurring" flat folds.

![Robby Demonstrating Maekawa Exercise](images/robby_2.jpg) | ![Smashed Origami](images/smashed.jpg)
:-----------------------------: | :-------------------------:
Robby Demonstrating the Maekawa Exercise | Maekawa Evidence


Since there are two general ways you can think about flat-folding--on its side, like we'd seen, or by twisting it using a series of folds to keep the face of the paper upright--this led right into tessellations!

#### Tessellations

Building on the flat-folding concepts, we started with another mini-exercise. We started by drawing a convex polygon in the middle of a piece of paper. Next, we creased each side and for each point on our polygon, we also folded an outward radiating angle bisector. All the creases should be the same direction (mountain) at this point. Finally, for each point we made a (valley) crease in order to make each vertex flat-foldable per the Kawasaki theorem. All of these new folds should be created in the same direction. Attempting to flat-fold these points when the folded sides don't reach the edge of the paper proved to be much harder than before! This twist exercise helps identify the behavior and principles involved in flat tessellations. (Not all tessellations are flat!)

As a way to start to explore tessellations on our own, Robby suggested pre-creasing some paper in either a tiled square or triangular pattern to use as a base to start twisting and folding our own shapes. From this process, we can see the relationship between the twisted and folded paper and unfolded paper. This would help us build out a larger tessellation pattern. 

We looked at a handful of artists who use folded tessellations in a variety of different ways. Ilan Garibi, in addition to folding paper tessellations, also makes jewelry by [rigid folding metal](https://www.garibiorigami.com/jewelry). [Ekaterina Lukasheva](https://www.instagram.com/ekaterina.lukasheva/) makes incredibly intricate and dynamic tessellations. Eric Gjerde makes tessellations, [sometimes backlighting them](http://www.ericgjerde.com/portfolio/arms-of-shiva/) to draw attention to the pattens created by the layers of folding. 

#### A Few Last Resources

Throughout the class, Robby showed and demonstrated a variety of origami/pattern generating software. While I haven't even tried them all, I'm putting my favorites toward the top, and listing others as reference.

* Robby Kraft, [Rabbit Ear](https://rabbitear.org/) Aside from the fact its great and easy to use, it's Robby's project!
* Amanda Ghassaei, [Origami Simulator](http://apps.amandaghassaei.com/OrigamiSimulator/)
* Jun Mitani, [Various Pattern Applications](http://mitani.cs.tsukuba.ac.jp/origami_application/)
* Tomohiro Tachi, [Freeform Origami and Origamizer](http://origami.c.u-tokyo.ac.jp/~tachi/software/)
* Robert Lang, [Treemaker](https://langorigami.com/article/treemaker/) and [Reference Finder](https://langorigami.com/article/referencefinder/)
* Alex Bateman, [Tess](http://www.papermosaics.co.uk/software.html)
