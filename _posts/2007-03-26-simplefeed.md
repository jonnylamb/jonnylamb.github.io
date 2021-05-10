---
title: SimpleFeed
date: 2007-03-26T10:01:13+00:00
layout: post
permalink: /2007/03/26/simplefeed/
image: /wp-content/uploads/2007/03/rss.png
---

I was looking for a [MediaWiki](http://www.mediawiki.org) extension that could read RSS feeds and output them onto the page. The trouble was, the extensions I found either didn't work, or were very uncustomisable. For example, for one that actually worked, adding this to the wiki page:

```
<feed>http://jonnylamb.com/feed/</feed>
```

forced this output on me:

```
<h3><a href="http://jonnylamb.com/2007/03/22/minimo-bongo/">Minimo Bongo</a></h3>
<small>22 March 2007, by jonnylamb</small>

<h3><a href="http://jonnylamb.com/2007/03/22/durham-visit/">Durham Visit</a></h3>
<small>22 March 2007, by jonnylamb</small>

<h3><a href="http://jonnylamb.com/2007/03/22/musically-active/">Musically Active</a></h3>
<small>22 March 2007, by jonnylamb</small>

<h3><a href="http://jonnylamb.com/2007/03/05/age/">++age</a></h3>
<small>5 March 2007, by jonnylamb</small>
```

This is not ideal. Instead of looking further for a better extension,
I wrote one. It is called SimpleFeed and it lives on the
[Extension:SimpleFeed](http://www.mediawiki.org/wiki/Extension:SimpleFeed)
page on [mediawiki.org](http://www.mediawiki.org).

It is simple for two reasons:
1. It uses the [SimplePie](http://simplepie.org) feed parsing library
2. It's exactly that- simple.

Here is a quick tour on how to use it:

Once it is installed, one can choose the syntax each item is outputted in. For example:

```
<feed url="http://jonnylamb.com/feed/">
== [{PERMALINK} {TITLE}] ==
<small>{DATE} by {AUTHOR}</small>

{DESCRIPTION}
</feed>
```

For each item from the feed, the curly-bracketed words get replaced
with their corresponding values. Note the use of wiki-markup as this
is then parsed by the MediaWiki parser, producing something like this:

```
<a name="Minimo_Bongo"></a><h2> <span class="mw-headline"> <a href="http://jonnylamb.com/2007/03/22/minimo-bongo/" class="external text" title="http://jonnylamb.com/2007/03/22/minimo-bongo/" rel="nofollow">Minimo Bongo</a> </span></h2>

<p>22 March 2007 by jonnylamb
</p>
<p>I shoved
[...]
```

So of course there's a whole load of MediaWiki stuff added which makes
it integrate into the wiki much better, and the killer feature is the
customisation possible!

There's more information on [its mediawiki.org
page](http://www.mediawiki.org/wiki/Extension:SimpleFeed).
