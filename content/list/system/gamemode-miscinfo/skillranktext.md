+++
date = "2016-08-01"
title = "SKILLRANKTEXT (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#skillranktext"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "SKILLRANKTEXT"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_SKILLRANKTEXT"
+++

## Status

None

## Syntax

`SKILLRANKTEXT:x <tab>
y`

## Parameters

-   x: Number (Skill rank)
-   y: Text (Alternate skill rank text)



What it does
------------

Provides a text-based identifier for skill rank numbers.

Examples
--------

`SKILLRANKTEXT:1 <tab> Incompetant`

`SKILLRANKTEXT:2 <tab> Novice`

`SKILLRANKTEXT:3 <tab> Competant`

`SKILLRANKTEXT:4 <tab> Expert`

`SKILLRANKTEXT:5 <tab> Professional`

`SKILLRANKTEXT:6 <tab> Master`

`SKILLRANKTEXT:7 <tab> Supreme`

Character skills with ranks of 1 through 7 will be labeled as
"Incompetent", "Novice", "Competent", "Expert", "Professional", "Master"
or "Supreme" as appropriate.

