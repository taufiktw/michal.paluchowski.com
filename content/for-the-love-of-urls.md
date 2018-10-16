---
author: michal
date: 2014-04-21T04:59:18.000Z
title: For the love of URLs
categories:
  - Technology
tags:
  - Internet
  - search engines
  - seo
  - user experience
image: /img/for-the-love-of-urls/github-404.png
---

[Aula Polska][aulapolska] is a regular meetup of Warsaw's entrepreneurial community, that I loved to attend until... its website had a facelift. It took a while to realize that I wasn't seeing announcements of new meetings anymore. They broke their URLs, including the RSS feed I was subscribing to. I scoffed, *how dumb!* And then I thought "*wait a second... did I check the URL for Michał's Bites' RSS feed after [moving to Wordpress][mpwordpress]?*" I was the pot calling the kettle black.

<!--more-->

The process that breaks the links around the web is known as [link rot][wplinkrot] - an epidemic deteriorating the online experience:

* readers, who bookmarked pages, cannot find them back,
* links from other websites stop working, and
* search engines cannot crawl the missing pages, so they impose ranking penalties.

Clearly, the damage hits everyone who is ever interacting with your content. Luckily, yours is also the power to save everyone the trouble, by showing some **love for your URLs**. In particular, when changing CMS platforms:

* strive to keep the URLs identical,
* setup [permanent redirects][google301] for inevitably changed URLs,
* communicate truly removed pages and offer alternatives.

In March 2013 I had to [move Michał's Bites from Posterous][mpwordpress] and chose a self-hosted Wordpress platform, partly *because* it **allowed me to configure and maintain identical URLs** for most pages, particularly the posts and tags. The [Safe Redirect Manager][pluginsaferedirect] plugin took care of the remaining pieces. I forgot about the RSS feed because it's somewhat removed from sight and only ever accessed by feed readers. Clicking through the new platform, or even running automated link checking didn't bring it up.

What *should have* helped were server logs, parsed by any reasonable software like [AWStats][awstats]. Place your new platform online, then keep an eye on the reports, looking particularly at the **404 errors section**. You'll see the most commonly accessed, but missing URLs. Fix or redirect them, if possible.

Some pages will be truly gone - removed and nowhere present in your new website structure. These should correctly return a `404 (not found)` or `410 (gone)` HTTP code. You can still go the extra mile and make the experience of hitting links like those slightly more bearable.

![GitHub's 404 page](/img/for-the-love-of-urls/github-404.png)

It can be fun, self mocking, but on top of that you should provide users with a way to move forward from there:

* At the very least offer a big, prominent **link to your home page**.
* The list of latest, or most popular articles.
* A search box for the website's content.
* Or a list of somewhat related pages to the one that's gone now, *if* you can reliably setup that kind of intelligence. Links to random pages help nobody.

Don't expect miracles - most readers will still bounce back and head somewhere else upon hitting a `404`, but at least they may smile, leaving with a pleasant memory. Some might stay and dive into your content.

Remember, **the Internet is forever** and [once you publish something][mpifyoudontappear], everybody's free to link, index and bookmark that piece of content. Help them find it back - by any means *they* choose - and you'll be building relationships that last.

[mpifyoudontappear]: {{< ref "if-you-dont-appear-you-disappear.md" >}}
[awstats]: http://awstats.sourceforge.net/
[pluginsaferedirect]: http://wordpress.org/plugins/safe-redirect-manager/
[aulapolska]: http://www.aulapolska.pl/
[wplinkrot]: http://en.wikipedia.org/wiki/Link_rot
[mpwordpress]: {{< ref "living-with-wordpress.md" >}}
[google301]: https://support.google.com/webmasters/answer/93633?hl=en

*[CMS]: Content Management System
*[URLs]: Uniform Resource Locator
*[URL]: Uniform Resource Locator
*[RSS]: Rich Site Summary
*[HTTP]: HyperText Transfer Protocol

