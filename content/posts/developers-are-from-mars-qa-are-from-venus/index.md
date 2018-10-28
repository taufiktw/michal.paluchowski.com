---
author: michal
date: 2012-10-21T15:51:00.000Z
title: Developers are from Mars, QA are from Venus
categories:
  - People
tags:
  - management
  - organizations
  - quality assurance
  - software development
---

Designed, developed, handed over to QA for testing. Then all hell breaks loose. "*How do I test it?*" "*Where's the documentation?*" "*This is broken; not it's not, it's not our component.*" "*I'm not signing this off!*" Or my personal favorite: "*I've other priorities to test now. I'll get to your stuff tomorrow.*" for three days in a row. Keeping QA separate from development teams is a recipe for trouble, friction and lots of missed opportunities. It has to stop.

<!--more-->

Once you put a QA Engineer in the same team with developers, sharing the same manager, several things happen:

* **QA shares the same goal** with developers - to deliver an excellent product on schedule & budget. No more bouncing tickets back and forth "*this isn't working!*", "*it's not a bug, it's a feature!*" "*this isn't a blocker!*" Shared goal, shared ownership, shared responsibility.
* **QA knows product first-hand** by spending time with developers as they work, talking over each feature and scenario. Ever tried asking a developer to write a test script for QA? Good luck with that. Sit the QA next to a developer and they can write the scripts perfectly themselves.
* **Testing gets done early and often** because QA doesn't have any other priorities or anyone else shouting louder at them to get their work done faster. User story finished? Alright, let's see how it works. Right now. And iron out all the bugs right there, on the spot.
* **Testing gets automated** when QA sets up [Selenium][selenium] (or any other) scripts together with developers, that they can later re-run as frequently as needed to check whether they've not broken something.
* **Developers spend more time coding** because they don't need to setup their own testing data and other environment pieces. QA can do it in parallel and whenever needed.

Sounds obvious if you're an Agile zealot, right? Notice how I never used [the "A" word][mbagile]? I didn't have to, because the above ideas have nothing to do with the movement. Even [Microsoft knew the value][mstesting] [PDF] of pairing developers and testers way before Agile was even manifested.

Testing is not separate from developing. It never has been, but today, when software requirements and markets change all the time, and so does source code, it's more expensive than ever to keep a QA team separated from development. For the sake of your company's success, stop doing that now.

[selenium]: http://seleniumhq.org/
[mbagile]: /what-does-it-mean-to-be-agile
[mstesting]: http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.92.1577&rep=rep1&type=pdf

*[QA]: Quality Assurance
