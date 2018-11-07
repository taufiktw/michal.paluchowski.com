---
author: michal
title: "Lessons Learned 2019 Refresher"
date: 2018-11-03T21:39:10+01:00
categories:
  - Personal
tags:
---

Notice anything new? [2014 was the last time I designed a new layout]({{< relref "/posts/living-with-wordpress/index.md" >}}) for this blog and it was time for a refresh. Five years is a lot of time to learn new things, so I thought I'd write up what's different about the blog this time---in code and in content.

<!--more-->

## New, bigger and better

__CSS grid and flexbox__ came of age and I learned to use those extensively. It's such a massive improvement over the last fifteen years of constructing layouts, ever since we departed from using tables. We finally have a sane way of aligning object height or putting something in the middle of the screen, vertically. The new layout makes use of both grid and flexbox.

__[BEM](http://getbem.com/)__ is an excellent way of organizing HTML and CSS code. I learned it from a large-scale web project, then started using it in small, personal ones as well. Now including this blog. Reading throught the old (S)CSS code was such a pain this time, trying to find the right selectors and what affected what. With BEM is always clear what the scope of each one is. There is a bit of duplication involved, but the gains in maintainability are massive.

I __moved from Wordpress to [Hugo](https://gohugo.io/)__---a static page generator, that I tried out for the first time with my travel blog. There's nothing wrong per se with Wordpress. I still use it whenever setting up a website for someone non-technical to manage. But Hugo feels much, much lighter and there's so much less overhead in customizing things to my liking. Plus, it's all static content, so performance and scalability are stellar and I don't need to worry about security exploits and such.

I'm setting up __automated deployments__ for every single application I maintian these days. Can't imagine I'd be uploading updates via FTP anymore. `git commit`, then `git push` and off it goes onto the server, including updating the content, theme, building SCSS, doing some other magic and copying files over to the web directory. I have a very simple setup for that here, while for large, commercial projects I obviously use proper CI and pipelines.

__Content discovery__ is an area where I continue to tinker. I always felt sad that people landed on this blog, maybe read a post and went away. There was the "reading list" menu and a way to page through posts, as well as go to the next and previous ones---a standard Wordpress pattern---but I didn't see any of those working. So I'm trying something new this time:

* the home page features three sections with different kinds of posts featured, from the latest ones, through my favorites, to a few randoms.
* each post finishes with links to random three other posts, in the hope that someone might get interested.

It's all "random", while perhaps "related" would be a better criterion, but for now Hugo doesn't support relating content that well (at least I couldn't get it to work), plus there's no real guarantee that someone who reads one post would like to continue reading about the same or related thing. Random gives them a chance to see something different, but perhaps also interesting.

I __dropped the comments__. There were a miniscule number of them here and I wouldn't have much time for keeping up with them even if there were more. I'm still happy to talk, though. Catch me on Twitter at [@mpaluchowski](https://twitter.com/mpaluchowski) any time!

Oh, and __I still can't design__, beyond simple, geometrical blocks. You'll notice this design is all plain colors and squares. I wish I could do it more vibrantly, like, say, [clothing from Desigual](https://www.desigual.com/), but clearly that's not my talent.

I did notice, however, how much photos and similar content breaks the flow of text it's in and makes reading difficult. I always found large photos in web articles visually appealing (and I make extensive use of that in the travel blog), but it's easy to go too far with that and suddenly the text becomes chopped up into small pieces in between media objects. I'm trying to avoid that here, while keeping the content lively with some media breaking it up.

## Old, valid truths

Content is king. __Content comes first__. I always believed it and I still do. There's very little chrome on the pages here, leaving lots of space for text, which I tried to lay out to the best of my abilities. I want as little as possible distracting the reader. I can't _stand_ pages that put thousands of notifications in my face before I get to see any content, which itself is surrounded by a million vaguely related pieces. Not here. This is tranquility and focus.

Moving uproots content and one always needs to __[take care of the URLs]({{< relref "/posts/for-the-love-of-urls/index.md" >}})__. Some will inevitably go away, like the comments I removed and thus there are no more RSS feeds for them. These are fine to cause 404 errors, but for everything else there should be proper 301 redirects. I set up the `.htaccess` file to cover for these and keep watching the 404 logs for other items I might have missed.

The design is __mobile first__. I actually started designing for the iPhone 6 screen and only once this was finished and usable did I expand to the bigger screens. There's a good chance you're reading this on a mobile device. I hope you're enjoying the results.

I continue to use __[SASS](https://sass-lang.com/) for CSS preprocessing__. It's extremely useful even on small scale websites, cleaning up the code, easing maintenance. I'm also working with [LESS](http://lesscss.org/) on other projects, which is likewise fine and in many ways similar. But SASS has a feature or two that I prefer to have.

## What's next?

A redesign is usually a good, motivational boost for writing up new posts. I like to publish just to see some new content in this beautifil layout. I have a few ideas for what to post on and I might have some extra time for doing that in the next few weeks.

I'm also planning a bit of cleanup, starting with the retiring of [www.nethut.pl](https://www.nethut.pl)---my almost twenty-year-old Polish website on webmastering and technology. I haven't posted to it in forever, the HTML code is very old, and I can't see myself updating it in any foreseeable future. I'll just redirect the address to this website.

Otherwise, this layout here isn't fully finished yet. There will be tweaks I'll come up with in the coming days and weeks, as always. Then it'll settle down for a few years, until the next time I feel like redesigning it and writing up another summary of learning.
