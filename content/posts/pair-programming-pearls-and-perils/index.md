---
author: michal
title: "Pair programming pearls &\u00A0perils"
date: 2019-02-17T05:38:18Z
categories:
  - People
tags:
  - pair programming
  - communication
---

If pair programming was easy, and universally better than working individually, we'd all be doing it *all* the time. But we don't. Most people I met need to make a conscious effort to pair and stay paired. All the while saying they "like it" and "need to do more of it".

<!--more-->

The way practicioners talk about pair programming reminds me of how people talk about exercising: "yeah, I should do this more often". They *know* there are benefits, they may be able to recite some of them, but it certainly doesn't come naturally.

## The good parts

Perhaps the best part of working in a pair is that **you can't hide**:

> Pairs naturally arouse engagement, even intensity. In a larger group, an individual may lie low, phone it in. But **nobody can hide in a pair**. "The decisive characteristic of the dyad is that each of the two must actually accomplish something," wrote Georg Simmel, "and that in the case of failure only the other remains—not a supra-individual force, as prevails in a group even of three." [emphasis mine]
>
> <cite>Joshua Wolf Shenk, [Powers of Two: How Relationships Drive Creativity][amazon-powers-of-two]</cite>

The presence of another gives you a pace, much like you have in a group of cyclists. You can't go slower than your partner. You can't procrastinate, idly browse Facebook or otherwise distract yourself. There's good focus and things move fowrard quicker.

It also helps, that two heads **bring together more and more diverse experience**. Your partner may have seen a particular problem already and know the solution. You may have worked with a required technology before.

This brings up the point of **learning by doing**, with guidance. But also the broader topic of **exchanging information**. You keep talking as your work progresses and both of you are on the same page with regards to customer requirements, system architecture, standards, patterns and plans moving forward.

Finally, [as Linus likes to say][wikipedia-linus-law], "given enough eyeballs, all bugs are shallow". Pair programming is **a form of code review**---an informal, lightweight, continuous one. Your partner will often see bugs or consequences that you don't, or will claim that a particular section of your code is difficult to comprehend---a somewhat annoying remark, but one that eventually leads to better code.

## The parts that irk

The blessing is also the primary curse, because **in a pair, you can't hide**. Sometimes you need your time alone. Some personal space, perhaps to idly do some busywork to relieve your brain, or to process a particular problem in silence and solitude. That applies especially if you're an introvert and continuous communication drains your energy.

Your partner may have a **different pace of working** than yours. May like to take more, or fewer, breaks, setting a rhythm of work that will not be to your comfort. May like to crunch quickly through sections of code that you like to deliberate more on. There's a related issue of **differences of temper**, where I personally like to think through solutions and understand their impact before touching the keyboard, while I worked with people who are more "trigger happy" and prefer to try things out and see where it brings us.

Finally, there's the same problem as when walking with someone who knows the way while you do not. Many people will not be able to learn to navigate on their own when being navigated with someone experienced. If you're new to the system and pairing with someone who's and old chap on it, there's a good change you'll take more time to find your way around it than if you were walking through on your own.

---

Sometimes and some of the time, would be my answer to whether programmers should work in pairs. Certainly not mandatory, neither by policy nor peer pressure. And make it conscious (which, incidentally, is a great general policy for life): see what parts work for you and which ones annoy you.

See with whom you're doing your best work---it'll *not* be everybody. One can always make the argument that working with someone you consider "difficult" puts you out of your comfort zone and teaches you new things, but I find you can learn just as much, without the added tension, by working with people you're more comfortable with.

By all means, try it out if you haven't yet. [Don't ask your boss for permission][mb-dont-need-permission], just do it. You'll be happy you did, because the pair programming *does* produce better code in the end, it makes you better, and you'll know it when you feel it.


[amazon-powers-of-two]: https://www.amazon.com/Powers-Two-Relationships-Drive-Creativity-ebook/dp/B00E9FYT0O/
[mb-dont-need-permission]: {{< ref "you-dont-need-permission-you-need-to-act/index.md" >}} "You don't need permission, you need to act"
[wikipedia-linus-law]: https://en.wikipedia.org/wiki/Linus%27s_Law
