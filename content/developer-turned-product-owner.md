---
author: michal
date: 2015-12-17T06:59:34.000Z
title: Developer  turned Product Owner
categories:
  - People
tags:
  - agile
  - backlog
  - product owner
  - specifications
---

The backlog is a _mess_. The order is random. There's no grouping or coherence, let alone a _vision_ of any kind. Stories are unclear, if at all described, and sprint planning takes forever while developers try to figure out what the product owner wants. I heard these complaints over and over again from teams, and then I had a chance to become a product owner myself. Turns out it's __not much different from a developer's work__.

## TDD

Taking an [agile approach][mp_mean_agile] means __making small steps and testing__ how they influence the product. Just like TDD in programming:

1. __Think__ what you want to do.
2. Decide how you will __measure__ success, like you code a test.
3. Have the team __implement__ your idea, usually by writing code and just enough to make the test pass.
4. __Evaluate__ the idea against your KPIs, like you would run your test.
5. With the findings, go back to 1 to __adjust__ your hypothesis and approach.

## Clean Code

The backlog items you're preparing---usually stories, will be read and relied on by the team to build a product increment. The clearer the language, the easier it'll be to understand and follow.

* clear, unambiguous, expressive naming,
* precise vocabulary,
* short paragraphs,
* good English (or any other language you use),

all of these are qualities that'll help the team deliver faster and with fewer misinterpretations. All the same in code, where good naming for variables, functions, objects matters, and short, focused functions and components are preferred.

## Abstraction

A good backlog is well organized, with related items grouped together into epics, aligned along a vision for the product. This in turn provides _direction and focus_ for both the team and stakeholders, guiding conversations on how the product should be shaped, deciding what fits in and more importantly what _doesn't_. It allows setting release and sprint goals, that the team can measure their progress against.

All this is exactly like abstraction in code, where similar logic gets grouped into objects, similar objects grouped into packages, [named after the domain they cover][wp_ddd]. From an orderly, well-named code base one should easily be able to identify the purpose of the system, decide where to put new code and whether it belongs in there at all.

## I know what the team's doing

My programming experience is helping me tremendously in shaping the backlog and working with the team. Requirements are crisp, or quickly refactored to become so, order is clear and it's easy to see what fits into our current vision and what should be deferred.

On top of that, I know the work the team does. When they come back reporting issues with implementing certain items, I understand those and we can easily adjust plans to reality, with the new information we received. Everyone's work becomes easier and we're steadily moving forward.

Obviously __not every developer would make a good product owner__. There's a lot of [touchy-feely people work][mp_knows_talking_about] involved, while many will likely prefer to deal with the clear, binary logic of computers. But for those who always liked to work on the edge between technology and people, this might just be the right career advance. One that's surprisingly easy to make.

*[TDD]: Test-Driven Development
*[KPIs]: Key Performance Indicators

[mp_knows_talking_about]: {{< ref "not-everyone-knows-what-theyre-talking-about.md" >}}
[mp_mean_agile]: {{< ref "what-does-it-mean-to-be-agile.md" >}}
[wp_ddd]: https://en.wikipedia.org/wiki/Domain-driven_design

