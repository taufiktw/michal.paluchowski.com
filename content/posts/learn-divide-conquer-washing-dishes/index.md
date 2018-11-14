---
author: michal
title: "Learn divide & conquer by washing dishes"
date: 2018-11-14T10:03:30+01:00
categories:
  - People
tags:
  - programming
---

You wouldn't think washing dishes has something to teach you about programming, would you? In fact, you're likely to despise it and either let your partner do it, or bought yourself a machine to take care of things. But a sink full of dirty plates is not unlike a difficult, multi-faceted problem to tackle in a hairy codebase.

<!--more-->

Picture the situation: I have a dual sink of the more shallow types and a facet over it that's relatively low. After a serious dinner it's full with a combination of plates, cutlery, pots, glasses, jars and other pieces awaiting rinsing. So much that, especially with the larger items, it's difficult to manipulate them under a stream of water without hitting other ones already in the sink.

The natural tendency? Start with the smaller items---the forks, knives, glasses---the ones that are easy to handle. That does reduce the overall size of the problem, but it's doing *nothing* to solve the essential issue of having clunky, large pots taking up space in the chambers. Some of these might be especially dirty, if I managed to burn something.

The solution? Start *not* with the easiest items but with the ones that **reduce the remaining complexity of the problem**. Pick the smaller items off the large ones in the sink, then wash the large ones---that'll make space in the sink for the remaining stuff around it. Finish with whatever is left.

Same with building software. I remember having a conversation with a front-end developer, who needed to build something that required server-side rendering of React code. We didn't have that in the application, yet. He opted for some workaround. I asked: "how does this reduce the size of the problem?"---it certainly didn't bring us any closer to having proper server-side rendering. He agreed. We picked the problem apart and found a simple way to render on the server for this particular problem, that could later be extended for more complex cases.

The lesson is, of course, to keep our old enemy---procrastination---in check, by having the courage to tackle the large problems and the smarts to split them into smaller pieces where each, hopefully, moves us towards the complete solution. Voila! Divide & conquer.
