---
author: michal
date: 2014-06-20T06:42:21.000Z
title: Coding is cheating
categories:
  - Technology
tags:
  - algorithms
  - computers
  - constraints
  - programming
image: https://michal.paluchowski.com/files/2014/06/sphere-triangles.gif
---

Programming is perhaps the only job where lying, cheating and deceiving will not only get you paid but also praised for being innovative and creative. That's because computers are _severely_ limited. We're literally fitting square pegs (real world) into round holes (0's and 1's).

Assuming you already know that everything in the computer world is represented in binary - combinations of 0's and 1's - consider the simplest example - trying to store the value `0.2`:

```
0.2 decimal = 0.00110011... binary
```

There __is no precise representation in binary__ for the decimal `0.2`. Instead it's a repeating pattern of `0011` after the mark. To make matters worse, a computer will only store a limited amount of digits for a number, say 32 for a fraction like the one above. But due to the specifics of number storage, the actual representation will only keep __26 digits__ from the recurring pattern of `00110011...`. The rest will be cut and gone as if it never existed. So the number a computer will _actually_ store is:

```
0.199999988079071044921875
```

Close enough to round it off to `0.2`, but still, what a cheat!

We continue to work around constraints, this time of memory. All computer memory is limited and we shouldn't waste it unnecessarily. So when we want to store a value in a program, we often won't store the actual value, but a __[pointer][wppointer]__ instead:

```
value = &quot;banana&quot;
valuePointer = &amp;value
```

The exact code will differ depending on the language used, but essentially it says:

1. save the value `banana` under the name `value`, then
2. assign to the name `valuePointer` the _memory address_ of `value` (it _points to_ where the original value is stored).

![Pointer illustration](/wp-content/uploads/sites/2/2014/06/pointer.png)

In consequence we're using much less memory, because the `banana` is stored only once, but as a side effect (sometimes desired), if we change to `value = "kiwi"` later, then `valuePointer` will also suddenly return `kiwi`.

Let's look at something more tangible - a sphere.

![Sphere](/wp-content/uploads/sites/2/2014/06/sphere.png)

You know how a sphere looks like, you can recognize one if you see it. But a computer is __inherently incapable of producing a real sphere__ (though that'll change once [ray tracing][wpraytracing] goes mainstream, thanks [Marek][fbmarekcomment]). For reasons that require a university course to explain, 3D spheres are drawn with... triangles.

![Sphere](/wp-content/uploads/sites/2/2014/06/sphere-triangles.gif)

There's just so many of them and so tiny that you are fooled and see a smooth surface. In the first 3D games that surfaced in the 90's you could actually see the edgy surfaces. Nowadays computers have enough horsepower to draw millions of triangles without much sweat.

Another funny concept is __[lazy loading][wplazyloading]__. We're usually storing data in some kind of database, which makes it expensive to retrieve. There's the time needed for a network call, the database engine reading files from disk etc. It all adds up, hence we want to make as few database calls as possible, so that users won't have to constantly stare at a screen saying "loading".

Let's say you want to open up a contract. We'll represent it in code as an object that includes all relevant information - ID, date of signing, ship-to and bill-to companies etc. We'll also tell you it has line items, which we may conveniently program as:

```
getLineItems()
```

where calling the above function will return the list of line items. However... we don't really have those line items ready to display, because we purposefully __didn't ask the database__ for them just yet. You might not need them at all - just want to check some basic details of the contract. So only the moment you ask for line items explicitly, and `getLineItems()` is called, do we make the query to the database (and let you wait for it), then return and display the list.

Finally, some problems in computing are very hard and extremely expensive to calculate at scale. Even for the modern beastly machines we have available. If you're using any sort of map application, you're seeing one such problem: calculating the best route between two points.

In order to _perfectly_ calculate the best route - be that the shortest or the quickest one, whatever the criterion - the computer would have to have to __calculate the distances and routes between every single point__ in the database. The number of calculations to perform would be the square of the number of points. Warsaw alone has thousands of addresses. Think how many points would there be on the route between, say, Warsaw and Berlin.

The trick we use in these hard cases is __[heuristics][wpheuristics]__ which boils down to using extra information we may have, and allowing for suboptimal results, providing the ones we deliver are good enough. For finding the best route on a map, we already know the locations (latitude and longitude) of all points. We can use that information to limit the area in which we'll calculate the routes, often to a shape resembling an ellipse:

![Shortest path calculation area](/wp-content/uploads/sites/2/2014/06/shortest-path.png)

We won't consider points and roads outside of this area _at all_. That's why when trying to cross Warsaw North (say Marymont) to South (Ursynów), the GPS might offer you a straight line through the city center, while a quicker and more convenient route may lead along the city bypass. But the calculation is much faster.

It's all cheating. Bending, stretching the material we are working with - computers - in order to deliver bigger, better and more vibrant experiences to users. We're not sorry, not at all. It's like solving elaborate puzzles every single day, while getting pay and praise for it. The joy of [programming][mbdevelopercost].

{{< youtube nKIu9yen5nc >}}

[wppointer]: http://en.wikipedia.org/wiki/Pointer_(computer_programming)
[wpheuristics]: http://en.wikipedia.org/wiki/Heuristics
[wplazyloading]: http://en.wikipedia.org/wiki/Lazy_loading
[mapscrosswarsaw]: https://www.google.pl/maps/dir/Marymont/Ursyn%C3%B3w,+Warsaw/@52.1955721,20.969994,12z/data=!4m14!4m13!1m5!1m1!1s0x471ecbb9e1556c1f:0x63c3d449c86a8300!2m2!1d20.95!2d52.26!1m5!1m1!1s0x47192d87247dae6b:0x84e20824775dbf76!2m2!1d21.0291229!2d52.1378544!5i2
[mbdevelopercost]: {{< ref "how-much-does-a-good-developer-cost.md" >}}
[fbmarekcomment]: https://www.facebook.com/michalpaluchowski/posts/4319571882936?comment_id=4320339102116&offset=0&total_comments=1
[wpraytracing]: http://en.wikipedia.org/wiki/Ray_tracing_(graphics)

*[GPS]: Global Positioning System

