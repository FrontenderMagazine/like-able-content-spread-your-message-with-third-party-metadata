# “Like”-able Content: Spread Your Message with Third-Party Metadata

Giving content proper structure is one of the most important things we can
do—because the more structure we have in our content, the freer it becomes. Most
of the time, [structured content’s][1] classifications and divisions allow for
the content’s presentation on a multitude of platforms.

By breaking content down into its natural components, we ensure current and
future compatibility and display in a wide range of devices and environments.
Third-party metadata schemas, like Facebook’s Open Graph protocol and Twitter
Cards, build on this ideal. And they are quickly becoming part of what it means
to have a modern and complete online presence.

Facebook’s Open Graph protocol, or OG (not to be confused with rapper Ice-T’s
1991 album, “O.G.”), builds on the notion of compatibility by way of
appropriately breaking down content into chunks, but from a platform-specific
point of view. Twitter also rolled out a [metadata scheme of its own][2], called
Twitter Cards. These metadata protocols serve a similar function—to provide a
better user experience around content shared on social platforms.

Basically, Twitter Cards and OG are discrete sets of metadata. Certain social
platforms look at that metadata and display parts of it, as appropriate. In
Twitter, you might see them as summaries of news articles or images in your
feed. On Facebook, OG most visibly manifests itself in the image, title, and
description of a shared website. (Note that this is separate from Facebook’s
recently unveiled “Graph Search.” OG provides a common language for content,
while Graph Search allows you to search for Facebook users based upon
relationships and associations within Facebook itself.)

Now, if the rest of our content is already future-friendly, why would we have a
need for such a thing?

## People share things

When we see something we really like online, we share it. Some copy and paste
the URL into an e-mail. Some print it out and mail it with a stamp. And millions
upon millions of others use their favorite social networks: Facebook, Twitter,
LinkedIn, etc.

If you share a link via e-mail, you’ll probably provide a bit of context so
they’ll know what’s what. A single, unsolicited URL in an e-mail without context
raises red flags for all sorts of spammy, phishy reasons. Most folks avoid this
situation by adding something like, “Hey, check out this cat video. SOOO
CUUUTE.” But even that takes some effort.

Content producers don’t have much influence in this arena. We can’t bring along
page metadata when someone pastes a URL in a blank e-mail. However, the social
realm affords us a bit more room.

## Standards for sharing

In olden times, when that cat video was shared on Facebook, it filled in the
title, description, and image slots with whatever metadata existed on the page.
It may have been a garbled title with some errant HTML all up in it. Maybe you’d
see the description of the homepage from 1998. Or you might get a badly cropped
version of the logo as the image. The case was clear: we would all benefit from
some standards, here.

When Facebook sought to establish a standard for populating those little shared-
content boxes that show up in our social network feeds, they were kind enough to
do it in an open fashion. The beloved [Dublin Core Metadata Element Set][3], a
standard from the library and computer science world, serves as its foundation
and starting point.

Facebook created this standard for its own use—it has the level of complexity
and functions that Facebook requires. However, other platforms, like LinkedIn
and Google+, populate their content-sharing boxes with OG metadata as well.

Facebook, LinkedIn, and Google+ all look to OG when dealing with shared content;
but in its absence, these social platforms will ultimately take whatever
metadata they can get. This may not put forth the best face for an organization,
adding up to a poor experience for everyone involved.

Twitter Cards, on the other hand, serve the singular purpose of providing an
experience in Twitter and its supported apps only. The minor differences between
Twitter Cards and OG address Twitter’s own content and display needs.

Twitter’s unique environment of sharing via retweets created some attribution
problems. I might share a link, but the 140-character limit doesn’t always allow
me to fit in a comment and proper attribution to the content creators or owners.
Twitter Cards seek to officially establish and preserve content authorship and
ownership with dedicated fields in the Twitter Card metadata schema.

Smartly, Twitter crafted its own metadata schema to maintain parity with other
social platforms. Content creators and site owners who incorporate the Twitter
Cards schema can now provide a richer shared-content preview experience. Twitter
Cards allow people to view, watch, or listen to content like images, video, and
audio without leaving the Twitter environment. As a result, people may stick
around on Twitter longer, which Twitter likes. (Not just out of niceness, mind
you. They can place more ads in front of more eyeballs that way.)

## Content-y fields forever

How does this all work? If you’ve gone down the path of structured content, or
are about to, adding third-party metadata schemas should be relatively easy.
Code placed in the head of each page does the heavy lifting. In fact, it lives
right next to the old-school meta tags.

Those in the old guard might remember the browser-specific tags of HTML 3.2 in
1997. Luckily, OG and Twitter Cards aren’t dependent upon Netscape Navigator. NO
WORRIES. But this might still reek of catering to the flavor of the moment,
shackling us all to a rigid standard dictated by an outside entity. Structured
content intends to set content free, not rein it in. And what happens when yet
another metadata schema comes along?

Granted, there are some similarities between these third-party metadata schemas
and browser-specific tags. Implementing them may seem like the least future-
friendly thing to do. Ultimately, site owners will weigh the costs of
implementation against the improvements to user experience and benefits to a
significant potential user base (like Facebook and its 1 billion users). The
available field options in both of these schemas encompass multiple formats and
types. That’s a great thing, since shared content takes many forms—from cat
videos to animated GIFs to regular old web pages.

For the sake of efficiency, it’s best to implement basics and only add support
for the content formats and types you plan to publish (and by extension,
encourage the sharing of). If audio isn’t your stock and trade, then there’s
little need to set up your CMS to handle third-party metadata schemas for it.

Both OG and Twitter cards aim to provide an appropriate, in-platform
presentation of shared content in its most popular forms:

* Articles get a text summary and small image preview
* Audio files get an audio player
* Video clips get a video player
* Images get a larger image preview

OG developers created several predefined objects—content types like videos,
audio files, web pages, etc.—each with its own meta properties. When the object
type is an audio file or video clip, the metadata associates it with a suitable
player, if applicable. This list of attributes provides detail on each meta tag
for an article:

	<meta property="og:type"	 content="article"> 
	<meta property="og:url"		 content="URL of this object">
	<meta property="og:site_name"	 content="Name of site hosting 	article">
	<meta property="og:image"	 content="URL to an image">
	<meta property="og:title"	 content="Name of article">
	<meta property="og:description"  content="Description of object"> 
	<meta property="article:author"	 content="URL to Author object">
	<meta property="article:section" content="Section of article">
	<meta property="article:tag"	 content="Keyword">
	
It all adds up to look like this on Facebook:

![Facebook link to the St. Paul Chamber Orchestra website][Figure 1]

Twitter Cards have a similar protocol, with specific properties established for
articles, video, audio, and images. The article-type content Twitter Card
metadata looks like this:

	<meta name="twitter:card"	 content="summary">
	<meta name="twitter:url"	 content="URL of this content">
	<meta name="twitter:title"	 content="Name of article">
	<meta name="twitter:description" content="Description of content">
	<meta name="twitter:image"	 content="URL to an image">
	
These optional Twitter Card items also allow you to attribute content to an
organization’s or creator’s Twitter handle:

	<meta name="twitter:site"	content="@username">
	<meta name="twitter:site:id"	content="Twitter ID">
	<meta name="twitter:creator"	content="@username">
	<meta name="twitter:creator:id"	content="Twitter ID">
	
This is how it looks on Twitter:

![Twitter card for a New York Times article link][Figure 2]

## Creating this content: focus and fill it up

Metadata is content, too. It’s subject to all of the same [process, workflow, and governance protocols][4] 
you may already have in place. As always, it should support the core message(s) 
of the page. These third-party metadata schemas do have some practical 
constraints as well.

### Field limits

Be aware that certain fields have display limits on different devices,
particularly the description fields. When writing these descriptions, keep it to
160 characters or fewer and this field’s automatic (and sometimes display-
dependent) truncation shouldn’t be a problem.

### Image selection

Effective, appropriate images can make the difference between a friend avoiding
or clicking on a link in her news feed. Image guidelines for article-type pages
in OG are pretty straightforward: 200×200px minimum with a maximum aspect ratio
of 3:1. However, a square image will allow the best use of the space. Twitter
cards resize any image over 120×120px, so you would be safe using that same
200×200px image you’ve already created for your `og:image`.

### Messaging

As you focus your message on the page, focus that message in the metadata. If
you’ve crafted a page with a single idea or concept in mind, the description
should come fairly easily. If not, prioritize and ensure that the message is
consistent. If a page has four key points, focus on a single one. The title,
description, and image should all align with the point you wish to showcase in
these social platforms.

For example: Microsoft’s new Surface tablet enjoyed quite a bit of press as it
launched. The [Surface Windows 8 Pro][5] page on Microsoft.com did not enjoy
preparation for a new Open Graph world. (It uses neither OG nor Twitter Cards.)

This page has several messages, with hierarchy established by placement upon the
page:

1. Buy this device
2. You can put apps on this device
3. This device is safe
4. You’ll enjoy stellar performance on this device
5. This device has a nice screen
6. Use a stylus to write on this device like a Palm Pilot
7. Buy this device

However, this hierarchy is not reinforced by the metadata. Microsoft gives the
Surface’s performance top billing by titling the page “Surface Windows 8 Pro is
powerful.” But I don’t see anything about the performance until I scroll down
and reach the fourth message on the page. That’s a pretty big disconnect. The
page’s meta description delivers even less.

Try to share this link in Facebook, and this unfocused approach becomes even
more apparent. People can choose between two 1280×450px images, far from the
ideal size or aspect ratio for display on any social platform news feed.
Meanwhile, the rote “Learn more” call to action mercifully stops short of an
old-timey “click here,” but still screams old-school marketing models.

![Facebook link to a Microsoft page][Figure 3]

What could Microsoft have done in this situation? Better represent the page on
social platforms by focusing on one of those core page messages. Then:

* Use a more compelling and descriptive title. Sure, Surface Windows 8 Pro is 
powerful, but compared to what? The competition? A weightlifter? A Ford 
Mustang? How will it help me do what I need to do? And they haven’t yet 
mentioned that it is a tablet. Pretty important detail, that.
* Take advantage of those 160 characters in the description. Sum up the page 
here, then maybe say “learn more.” What will I learn if I visit this page? Can 
I buy one there? Does it have Solitaire? Why should I consider this versus the 
competition?
* Provide an interesting and representative image. Social platforms are stingy 
with real estate. Use it up. Create an image that accurately represents and 
supports your message. And format it properly to avoid its dissection via 
automatic image cropping.
* Give them a reason to click. Present a clear, concise call to action 
appropriate for the platform. And make sure you deliver on what you offer. 
(All time-tested, these tips.)

## Workflow and implementation become triage and training

Adding OG and Twitter Cards to older, existing pages might be a bit tougher than
incorporating them in new content. Especially if you have thousands upon
thousands of pages.

Consider a phased approach to provide consistency across your entire online
presence, while allowing improvements to other, lower-profile areas as time
allows. Focus on getting things in place on high-impact assets first, such as
pages already seeing strong share activity. Then, meet minimum standards on
others.

Though most pages on a site are technically shareable, people aren’t necessarily
going to share them. Think of optimizing your “Contact Us” page for sharing. Bad
idea. Map your current page types to some simple third-party metadata divisions:

### Frequently shared pages

Pages supporting active campaigns, blog posts, product pages, and pages with
high profiles and traffic.

* Requires the most time and resources.
* Create page-specific metadata with input from subject matter experts. Write 
it with the same gravity as other marketing or promotional content.
* Use unique titles, descriptions, and images.

### Infrequently shared pages

Transactional, transitional, or navigation pages.

* Less resource-intensive.
* Create section- or topic-specific metadata content to provide relevant 
(but not page-level) detail.
* Use specific titles and section-specific descriptions across pages, but 
generic images (like your logo or icon).

### Pages not intended for sharing

These include pages like contact, legal disclosure, and the sitemap.

* Least impact on resources, easiest to maintain.
* Create generic metadata content to meet minimum brand standards.
* Use specific titles, but a generic, site-wide description and generic images 
(your logo or icon works well, here, too).

Communicate the importance of these new fields to content creators and
approvers, many of whom are likely avid Facebook users. Show them a good example
of a site successfully using OG. Then show them a site not using OG at all.
Chances are, they’ll get it right away.

A clear understanding of the uses of structured content chunks will give them
the context they need to create appropriate content. (It’s worth noting that
this isn’t unique to OG or Twitter Cards—this understanding is important for all
structured content.)

## A word of (cautionary) encouragement

As with any third-party relationship, certain things are slightly out of your
control. We’ve become accustomed to regular changes in hardware, Google search
algorithms, and Facebook privacy settings. These changes are inevitably
disruptive; all the more reason to keep a close eye on the evolution and
development of these (and other) third-party tools and platforms.

While implementing third-party metadata schemas will add to the content creation
workload, that extra effort will provide a much better user experience across
multiple platforms and devices, both current and upcoming. Crafting content in
discrete chunks with an eye on universal application and flexibility is the way
of the future. “Like” it or not (groan).

[1]: http://alistapart.com/article/future-ready-content
[2]: https://dev.twitter.com/docs/cards
[3]: http://en.wikipedia.org/wiki/Dublin_Core
[4]: http://blog.braintraffic.com/2011/03/brain_traffic_lands_quad/
[5]: http://www.microsoft.com/Surface/en-US/surface-with-windows-8-pro/home

[Figure 1]: img/FacebookOrchestra_b.png
[Figure 2]: img/TwitterNYTimes_b.png
[Figure 3]: img/FacebookMicrosoft_c.png