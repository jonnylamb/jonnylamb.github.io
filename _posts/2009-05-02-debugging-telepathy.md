---
title: Debugging Telepathy
date: 2009-05-02T00:31:29+00:00
layout: post
permalink: /2009/05/02/debugging-telepathy/
image: /wp-content/uploads/2009/05/debugging.png
categories:
  - planet-collabora
  - planet-debian
  - planet-gnome
---

Sometimes [debugging](http://live.gnome.org/Empathy/Debugging)
[Telepathy](http://telepathy.freedesktop.org/wiki) can be a pain. I
die a little every time I see _just run gabble from the command line
with GABBLE_DEBUG=all_ on #telepathy.

[Daf](http://dgh.livejournal.com/) started implementing a [debug
interface](http://git.collabora.co.uk/?p=telepathy-spec.git;a=blob;f=spec/Debug.xml;hb=HEAD)
in gabble but he fled the country, so I finished it off, and added a
hot [new dialog](http://bugzilla.gnome.org/show_bug.cgi?id=579725) to
Empathy.

{% include figure.html src="https://jonnylamb.com/wp-content/uploads/2009/05/debug-dialog-4.png" %}

Additionally, if you are a Telepathy developer, this may be an interesting addition to your shell startup file:

```
g () {
    project=$(basename `pwd`)
    GABBLE_DEBUG=all SALUT_DEBUG=all EMPATHY_DEBUG=all HAZE_DEBUG=all 
        GABBLE_PERSIST=1 SALUT_PERSIST=1 HAZE_PERSIST=1  EMPATHY_SRCDIR=. 
        libtool --mode=execute gdb -q --args ./src/$project --g-fatal-warnings
}
```
