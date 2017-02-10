+++
date = "2016-08-01"
title = "PREDEITY (Global: PRErequisite)"
original_url = "/list/global/pre.html#predeity"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREDEITY"
    parent = "global_pre"
+++

## Status

None

## Syntax

`PREDEITY:x,y`

## Parameters

-   x: Number (The number of the deity's name or
    pantheons that must match).
-   y: Y (The character must have chosen a deity).
-   y: N (The character must not have chosen a deity).
-   y: Text (The name(s) of deities).
-   y: PANTHEON.Text (The name(s) of pantheons).



What it does
------------

Sets deity requirements by presence, name or pantheon name.

Examples
--------

`PREDEITY:1,Y`

Character must have a deity chosen.

`PREDEITY:1,N`

Character must NOT have a deity chosen.

`PREDEITY:1,Zeus,Odin`

Character must have chosen either "Zeus" or "Odin".

`PREDEITY:1,Zeus,PANTHEON.Celtic,Odin`

Character must have chosen either "Zeus", "Odin" or a deity in the
"Celtic" pantheon.

`CLASS:Druid.MOD <tab> PREDEITY:1.Saluwe,Yarris,Belisarda,Fire Dragon`

Character must have chosen either "Saluwe" "Yarris" "Belisarda" or "Fire
Dragon".

