---
author: michal
date: 2015-11-01T17:12:55.000Z
title: Antique inspirations for software architects
categories:
  - Technology
tags:
  - design
  - quality
  - software architecture
  - usability
image: /antique-inspirations-for-software-architects/millau-viaduct.jpg
favorites: true
---

The Roman architect [Vitruvius][wp_vitruvius] around the year 15 BC completed his impressive, ten-volume treatise on architecture---[De Architectura][wp_de_architectura]. It covers every possible type of man-made structure ever needed by the people of his time, but starts out wisely by prescribing _basic_ qualities that good architecture _must_ embody:

<!--more-->

> All... must be built with due reference to __durability__, [__utility__], and __beauty__. Durability will be assured when foundations are carried down to the solid ground and materials wisely and liberally selected; [utility], when the arrangement of the apartments is faultless and presents no hindrance to use, and when each class of building is assigned to its suitable and appropriate exposure; and beauty, when the appearance of the work is pleasing and in good taste, and when its members are in due proportion according to correct principles of symmetry. [emphasis mine, and I prefer 'utility' over 'convenience' in the original quote]
>
> <cite>Vitruvius, [De Architectura][wq_vitruvius], Wikiquote</cite>

Sounds familiar? It certainly did for me when I was brainstorming the set of values that our newly minted team of software architects was to adopt. __Durability__, __Utility__ and __Beauty__ described perfectly how I thought about good software architecture.

* __Durability__ means that software _must stand the test of time_. Work as long as necessary without crashing or requiring mid-way reboots. And it shouldn't need to be rewritten from scratch every few years, but instead [adapt well to changing needs][mb_agile_approach]. This principle guides the selection of languages, platforms, frameworks and tools.
* __Utility__ means the software _must fulfill requirements_ that it was given and must do so well. If it's a user-facing application, it must be [easy to use and supportive][mb_trusting_software], if it's meant to handle high load, it needs to scale well. If it [exposes an API][mb_api] for others to connect to, that has to be comprehensive and flexible. We need to build software always with its intended purpose in mind.
* __Beauty__ means the software _must be pleasing to the eye_. A clean, simple UI, laid-out and colored for readability. Inside, a logical layout of components, packages and modules. Good, clear but concise naming, plenty of whitespace, short functions, variables of unambiguous purpose. Computers will read anything. We need to code for people. This principle underlies front-end and coding style guides.

We unanimously decided to adopt these two-millennia-old qualities as our team's values and to visualize them, I proposed an image that would become our logo: the [Millau Viaduct][wp_millau_viaduct]---a spectacular bridge designed by sir Norman Foster, built [near the city of Millau in southern France][maps_millau_viaduct].

<figure>
<img src="/antique-inspirations-for-software-architects/millau-viaduct.jpg" alt="Millau Viaduct">
<figcaption>Millau Viaduct by <a href="https://www.flickr.com/photos/flissphil/2892568426">Phillip Capper</a>.</figcaption>
</figure>

Bridges ideally __embody durability__, some serving the public for centuries, like the [Charles Bridge in Prague, opened in 1402][wp_charles_bridge]. Getting people efficiently and safely across rivers, valleys and canyons is as clear an __illustration of utility__ as we could hope for. And while beauty is in the eye of the beholder, to us __Millau Viaduct truly is beautiful__, with its slender structure suspended over the Tarn valley like a delicate web of strings.

We're using these values to [ask better questions][mb_feed_it_back]. Is it durable? Will this fancy framework you have spotted at some conference be around in two years? Are you sure we need the user to click three times to submit the order? Can we make it easier? Can you read your own code? Can your new team colleague read and understand it? Old lessons that continue to hold true in an age technically so much more sophisticated than when they were put in writing.

*[UI]: User Interface

[maps_millau_viaduct]: https://goo.gl/maps/t5R2pjBj5Ys
[mb_agile_approach]: {{< ref "agile-is-the-business-approach-to-software-en/index.md" >}}
[mb_api]: {{< ref "api-thinking-vs-client-thinking/index.md" >}}
[mb_feed_it_back]: {{< ref "feed-it-back/index.md" >}}
[mb_trusting_software]: {{< ref "trusting-software/index.md" >}}
[wp_charles_bridge]: https://en.wikipedia.org/wiki/Charles_Bridge
[wp_de_architectura]: https://en.wikipedia.org/wiki/De_architectura
[wp_millau_viaduct]: https://en.wikipedia.org/wiki/Millau_Viaduct
[wp_vitruvius]: https://en.wikipedia.org/wiki/Vitruvius
[wq_vitruvius]: https://en.wikiquote.org/wiki/Vitruvius#De_architectura_.28The_Ten_Books_On_Architecture.29_.28.7E_15BC.29
