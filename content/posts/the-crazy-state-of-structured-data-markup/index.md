---
author: michal
date: 2014-03-30T05:43:59.000Z
title: The crazy state of structured data markup
categories:
  - Technology
tags:
  - html
  - search engines
  - seo
  - social networks
  - structured data
---

You want to look good for Google. You want it to *understand* your website, so that it comes up in results often and stands out. You also want Facebook and Twitter to display your links prominently in their crowded timelines. Because you want all that, you'll likely turn to structured data markup, like I did with the new design of Michał's Bites. And then you'll shake your head in disbelief.

<!--more-->

Designing a fresh look for Michał's Bites nudged me to look into [Schema.org](http://schema.org/) - a co-product of Bing, Google, Yahoo! and Yandex, meant to help them make sense of the contents of a page. In the words of its publishers:

> On-page markup enables search engines to understand the information on web pages and provide richer search results in order to make it easier for users to find relevant information on the web.

And while choosing the [right entity](http://schema.org/docs/full.html) for your particular page element isn't always straightforward, it's easy to mark it up:

```html
&lt;article itemscope itemtype=&quot;http://schema.org/BlogPosting&quot;&gt;
  &lt;h1 itemprop=&quot;name headline&quot;&gt;The crazy state of structured data markup&lt;/h1&gt;
  &lt;section itemprop=&quot;articleBody&quot;&gt;
    &lt;p&gt;...&lt;/p&gt;
  &lt;/section&gt;
  &lt;p&gt;Written by &lt;span itemprop=&quot;author&quot; itemscope itemtype=&quot;http://schema.org/Person&quot;&gt;&lt;span itemprop=&quot;name&quot;&gt;Michał Paluchowski&lt;/span&gt;&lt;/span&gt;&lt;/p&gt;
&lt;/article&gt;
```

It's *consistent*. Most entities will have a way to markup `name`, `url` or `description`. Some have unique attributes, like a `BlogPosting` has an `articleBody` above. It's readable for both computers and humans.

But wait, there's more.

Since I'm using [WordPress]({{< ref "living-with-wordpress/index.md" >}}), some of its widgets output markup of the [microformats](http://microformats.org/) brand. These serve a similar purpose as Schema.org, but with a much smaller dictionary of entities. Little did I know that Google scanned it too and started complaining via Webmaster Tools that my implementation was incorrect:

![Google Webmaster Tools Microformats Error](/the-crazy-state-of-structured-data-markup/webmaster-tools-microformats-error.png "Google Webmaster Tools Microformats Error")

I complied, included the missing markup, and the code became:

```html
&lt;article class=&quot;h-entry&quot; itemscope…
  &lt;h1 class=&quot;p-name&quot; itemprop=...
```

There's *still* more. Facebook developed its [OpenGraph](https://developers.facebook.com/docs/opengraph/), and Twitter has their [Cards](https://dev.twitter.com/cards), all of which - with some extra markup - allow me to control and improve the way content will appear in the services' respective timelines. Otherwise Facebook may display a random snippet of text with a link, starting with something as "meaningful" as "Comments closed".

These meant adding some more markup to my code:

```html
&lt;meta property=&quot;og:type&quot; content=&quot;article&quot;&gt;
&lt;meta property=&quot;og:title&quot; content=&quot;The crazy state of structured data markup&quot;&gt;
&lt;meta name=&quot;twitter:card&quot; content=&quot;summary&quot;&gt;
&lt;meta name=&quot;twitter:title&quot; content=&quot;The crazy state of structured data markup&quot;&gt;
```

Now my content was nicely highlighted on Twitter (note: doesn't always show up):

{{< twitter 447115370965774336 >}}

As a consequence, I have **the same data three-four times in the page**:

1. reader-visible HTML, with the overhead of Schema.org and Microformats markup,
1. META markup for Facebook,
1. META markup for Twitter.

It's like adding extra CSS for some older versions of Internet Explorer with `<!--[if lt IE 9]>`. Overhead and waste.

There is, perhaps, an end to this in sight. The W3C, just a few months ago, published a [draft specification of Microdata](http://www.w3.org/TR/microdata/), which essentially is Schema.org as part of HTML5.

I like the Schema.org specification best, because it's rich, consistent and impossible to confuse with other markup. Using the `class` attribute for structured data is logically sound (`<article class="blog-post">` speaks well of the type of the article), but if you place it in any slightly complex web layout, maintained by many people, it's easy to mix and confuse with styling values. That means it's likely to be accidentally removed or changed.

At the same time, Schema.org markup gets added right onto content markup, without the overhead of duplication in the `<head>` or elsewhere - again a maintenance nightmare waiting to happen.

Both Facebook and Twitter are certainly powerful enough to enforce their own solutions (think Facebook's latest [announcement of Hack](https://code.facebook.com/posts/264544830379293/hack-a-new-programming-language-for-hhvm/)), but if Google and Bing were able to come together and agree on one standard, I'm sure other big names can join the party too. The fewer standards on the market, the broader the adoption, easier parsing and ultimately better content is served to end users.

*[HTML]: HyperText Markup Language
*[CSS]: Cascading Style Sheets
*[W3C]: World Wide Web Consortium
