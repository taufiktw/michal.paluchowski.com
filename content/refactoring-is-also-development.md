---
author: michal
date: 2010-10-22T03:43:00.000Z
title: Refactoring is also development
categories:
  - Technology
tags:
  - coding
  - maintenance
  - software development
---

Try cooking in your kitchen for a week without cleaning. Just leave all the used packaging around and all the dirty cutlery in the sink. I bet you'll not only be unable to walk safely from door to window, you may also feel like throwing up due to the spreading reek. Do that for a few months and it'll be easier for you to move than clean up.

Something similar is happening daily all over the world at software vendors. Because there's always a business reason to write new code and never to clean up the existing one, everyone ends up managing thousands and millions of lines of code, often written three generations of employees ago. "_Where is this method used? Uhm... I don't know. Carl wrote it and he left the company during last year's layoffs._" At some point writing any new change requires more impact analysis than designing and coding. Then someone comes up with the bright idea of scrapping it all and writing from scratch.

Refactoring __must__ be treated like any other part of the development process:

1. Designing
1. Testing
1. Coding
1. __Refactoring__
1. Go to 1

It __must__ be expected, planned and estimated for. Not "_when we have time_" or "_when we're done with all the coding_" but right after we're done with the current chunk of code. It may be more expensive upfront, but then so much cheaper in the long run.
