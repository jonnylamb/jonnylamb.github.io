---
title: Telepathy Extras
date: 2010-01-14T12:30:00+00:00
layout: post
permalink: /2010/01/14/telepathy-exras/
image: /wp-content/uploads/2010/01/telepathy.png
categories:
  - planet-collabora
  - planet-debian
  - planet-gnome
---
A few weeks ago, I got [a cool Christmas present](http://blog.barisione.org/2009-12/early-christmas/) from [work](http://www.collabora.co.uk/). It's pretty sweet, and I've been writing some apps for it. I'll try and blog about them here.

{% include figure.html src="https://jonnylamb.com/wp-content/uploads/2010/01/telepathy-extras.png" %}

A while ago, I wrote some a number of account plugins for Maemo 5, so that other Telepathy connection managers could be used and well-integrated into the N900's Contacts and Conversations User interface. This enables the following extra protocols:
* [AIM](http://maemo.org/packages/view/account-plugin-haze/)
* [GaduGadu](http://maemo.org/packages/view/account-plugin-haze/)
* [Groupwise](http://maemo.org/packages/view/account-plugin-haze/)
* [ICQ](http://maemo.org/packages/view/account-plugin-haze/)
* [IRC](http://maemo.org/packages/view/account-plugin-idle/) (currently only supports 1-to-1 private messages)
* [MSN](http://maemo.org/packages/view/account-plugin-butterfly/) (soon to gain calling support)
* [QQ](http://maemo.org/packages/view/account-plugin-haze/)
* [link-local XMPP](http://maemo.org/packages/view/account-plugin-salut/)
* [Sametime](http://maemo.org/packages/view/account-plugin-haze/)
* [Yahoo](http://maemo.org/packages/view/account-plugin-haze/)

There are still a few problems which I'll try to iron out soon enough
but they appear to be working pretty well. The best thing about it is
clearly the integration with the rest of the phone, as demonstrated by
Marco in the screenshot above.

The [PR1.1 update](http://wiki.maemo.org/Maemo_5/PR1.1), which is due
today, also opens the door for enabling other protocols dynamically by
providing libpurple plugins. I will be adding Facebook Chat support
soon, and someone else has made a package for Twitter.

This is in extras-testing for you all to download and try out. You can
find all the packages in the _Network_ category of the Application
manager. The _Extra protocol plugins for Conversations and Contacts_
metapackage (telepathy-extras, in reality) pulls in all the cool
account plugins and connection managers of the time. File bugs from
the maemo.org package link.
