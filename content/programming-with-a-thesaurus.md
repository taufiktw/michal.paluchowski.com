---
author: michal
date: 2017-10-28T07:43:02.000Z
title: Programming with a thesaurus
categories:
  - People
tags:
  - naming
  - programming
  - writing
---

Source code needs to read like a book, with characters introduced in proper order and the plot unfolding logically for the reader to follow. Naming is key. The right word used in the right place---a function, class, variable name---will help avoid many a bug. That's where a thesaurus will come in handy.

A thesaurus is a reference of words with similar meanings, used "to find the word, or words, by which [an] idea may be most fitly and aptly expressed" (as [the architect of, apparently, the best-known English thesaurus wrote][peter-mark-roget]). That's _exactly_ what we aim for in code---express our intent for future programmers, including ourselves, to precisely understand. It's easy to write code computers understand. When they don't they tell you at compilation time.

A function or class name must "most fitly and aptly" match what it's doing. A variable name must likewise accurately describe what it holds.

How many `get...()` functions did you see in your life? How many of them were actually "getting" things, and _only_ getting them? How many were additionally storing data, creating entities, causing all sorts of side effects?

It's not just a matter of sloppy programming. Naming creates the boundaries within which a programmer will naturally try to navigate. If you call a class a `CompanyManager` then _anything_ you try to do with companies will fit into it---retrieving, storing, filtering, listing, sorting etc. That class will eventually evolve into a multi-thousand-line monster.

Help yourself to a thesaurus. Any old one will do, and I personally use [thesaurus.com][thesaurus.com] whenever I have trouble finding the right word. For instance, try "[create][thesaurus-create]":

> build, construct, discover, establish, form, generate, initiate, shape, start, compose

... and many other alternatives. These are just the ones I thought might be useful in a code base. Say, you want a function to setup a connection to a remote service. You could name it `createConnection()` but from the above list I'd prefer `initiateConnection()`. A factory method could be named `createInstance()` but I'd rather use `constructInstance()`---referring to the well-known constructor pattern. A function that'll search for a specific service to connect to, could be called `discover...()` and so on.

It's _fun_, though perhaps I'm biased here, as I find great enjoyment in playing with words, where others will prefer to get on with their work. But it's worth the effort.

[peter-mark-roget]: https://en.wikipedia.org/wiki/Peter_Mark_Roget
[thesaurus.com]: http://www.thesaurus.com/
[thesaurus-create]: http://www.thesaurus.com/browse/create?s=t

