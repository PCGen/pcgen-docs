+++
date = "2016-08-01"
title = "PREMULT (Global: PRErequisite)"
original_url = "/list/global/pre.html#premult"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREMULT (Global: PRErequisite)"
    parent = "pre"
+++

## Status

None

## Syntax

`PREMULT:x,y,y`

## Parameters

-   x: Number (Number of Prereqs)
-   y: \[Text\] (Embedded PRExxx tags)



What it does
------------

-   PREMULT is a special PRExxx tag in that one embeds other PRExxx tags
    in it, allowing for the application of a logical OR across
    PRExxx tags.
-   PREMULT can be embedded into itself.

Examples
--------

`PREMULT:1,[PRERACE:Gnome],[PRECLASS:1,Cleric=1]`

Character must be either a "Gnome" or a "Cleric".

`PREMULT:1,[PRERACE:Gnome],[PREMULT:2,[PRESIZEGTEQ:M],[PREFEAT:1,Alertness]]`

Character must be "Gnome" OR a medium sized or larger creature with the
"Alertness" feat.

`PREMULT:1,[!PRERACE:%],[PRERACE:Bunch of Rocks]`

Character only be from a "Bunch of Rocks".

`Stamina.MOD <tab> PRE:.CLEAR <tab> PREMULT:1,[PREFEAT:1,Robust],[PRECLASS:1,Super Soldier=1]`

The Stamna feat is modified to remove all PRE tags and replace with the
following.

