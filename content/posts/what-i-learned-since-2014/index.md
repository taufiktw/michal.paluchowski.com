---
author: michal
title: "What I learned since 2014"
date: 2018-11-03T21:39:10+01:00
categories:
  - Personal
tags:
---

Notice anything new? [2014 was the last time I designed a new layout]({{< relref "/posts/living-with-wordpress/index.md" >}}) for this blog and it's time for a refresh. It's also a good moment to note what I'm doing differently now, with the knowledge acquired over the last five years. Here's a write-up of what's different about the blog---in code and in content.

<!--more-->

## New, bigger and better

__CSS [grid](https://css-tricks.com/snippets/css/complete-guide-grid/) and [flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)__ came of age and I learned to use those extensively. It's such a massive improvement over the last fifteen years of building layouts, ever since we stopped using tables. We finally have a sane way of producing same-height objects or placing something in the middle of the screen, vertically. This blog's new layout makes use of both grid and flexbox.

__[BEM](http://getbem.com/)__ is an excellent way of organizing HTML and CSS code. I learned it from a large-scale web project, then started using it in small, personal ones as well. Now, also on this blog. Reading my 2014 (S)CSS code was such a pain, trying to find the right selectors and what caused what. With BEM, all CSS is separated into reusable modules with a clear scope, independent of specific HTML tags. There is a bit of duplication involved, but the gains in maintainability are well worth the cost.

I __moved from Wordpress to [Hugo](https://gohugo.io/)__---a static page generator, that I tried out for the first time with [my travel blog](https://travel.paluchowski.com/). There's nothing wrong per se with Wordpress. I still use it whenever setting up a website for someone non-technical to manage. But Hugo feels much, much lighter and there's so much less overhead in customizing things to my liking. Plus, it's all static content, so performance and scalability are stellar and I don't need to worry about security exploits and such.

I'm setting up __automated deployments__ for every single application I maintian these days. Can't imagine I'd be uploading updates via FTP anymore. `git commit`, then `git push` and off it goes onto the server, including updating the content, theme, building SCSS, doing some other magic and copying files over to the web directory. I have a very simple setup for that here, while for large, commercial projects I obviously use proper CI pipelines.

__Content discovery__ is an area where I keep tinkering. I always felt sad that people landed on this blog, maybe read a post and went away. There was the "reading list" menu and a way to page through posts---a standard Wordpress pattern---but I didn't see any of those working. So I'm trying something new this time:

* the home page features three sections with different kinds of posts: the latest ones, then my favorites, and finally a few randoms.
* each post finishes with links to random three other posts, in the hope that someone might get interested.

It's all "random", while some might suggest that "related" would be a better criterion, but for now Hugo doesn't support relating content that well ([at least I couldn't get it to work](https://gohugo.io/content-management/related/)), plus there's no real guarantee that someone who reads one post will continue reading about the same thing. Random gives a chance to serendipity.

I __dropped the comments__. There were a miniscule number of them here and I wouldn't have much time for keeping up even if there were more. I'm still happy to talk, though. Catch me on Twitter at [@mpaluchowski](https://twitter.com/mpaluchowski) any time!

Oh, and __I still can't design__ beyond simple, geometrical blocks. You'll notice this design is all plain colors and squares. I wish I could put together something vibrant, like, say, [clothing from Desigual](https://www.desigual.com/), but clearly that's not my talent.

I did, however, notice how photos and similar content placed in-between paragraphs break the flow of text and make reading difficult. I still find large photos in web articles visually appealing (and I make extensive use of them in the travel blog), but it's easy to go too far with these and suddenly you can barely see the words in between images. I'm trying to improve the balance here, between all-text and some visuals to spice it up.

## Old, valid truths

Content is king. __Content comes first__. I always believed it and I still do. There's very little chrome on the pages here, leaving lots of space for text, which I tried to lay out to the best of my abilities. I want as little as possible distracting the reader. I can't _stand_ pages that put thousands of notifications in my face before I get to see any content, which then is surrounded by a million vaguely related widgets. Not here. This is tranquility and focus.

Moving CMS engines uproots content and one always needs to __[take care of the URLs]({{< relref "/posts/for-the-love-of-urls/index.md" >}})__. Some will inevitably go away, like the RSS feeds for comments, that I removed. These are fine to cause 404 errors, but for everything else there should be proper 301 redirects. I set up the `.htaccess` file to cover for these and keep watching the 404 logs for other items I missed.

The design is __mobile first__. I actually started designing for the iPhone 6 screen and only once this was finished did I expand to bigger screens. There's a good chance you're reading this on a mobile device. I hope you're enjoying the result.

I continue to use __[SASS](https://sass-lang.com/) for CSS preprocessing__. It's extremely useful even on small scale websites, letting me maintain less code, easing maintenance. I'm working with [LESS](http://lesscss.org/) on other projects, which is likewise fine and in many ways similar. But SASS has a feature or two that I prefer to have.

## What's next?

A redesign is usually a good, motivational boost for writing up new posts. I like to publish just to see new content in this beautiful layout. I have a few ideas for what to post on and I might have some extra time for doing that in the next few weeks.

I'm also planning a bit of cleanup, ~~starting with the retiring of [www.nethut.pl](https://www.nethut.pl)~~ (already gone)---my almost twenty-year-old Polish website on webmastering and technology. I haven't posted to it in forever, the HTML code is very old, and I can't see myself updating it in any foreseeable future. I'll just redirect the address to this website.

Otherwise, this layout here isn't fully finished yet. There will be tweaks in the coming days and weeks, as always. For starters, I might need to expand the line height on text. It feels stuffy on big screens. At some point, this theme will settle for a few years, until the next time I feel like redesigning it and writing up another summary of learning.
