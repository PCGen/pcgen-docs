+++
date = "2016-08-01"
title = "STATROLLTEXT (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#statrolltext"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "STATROLLTEXT"
    parent = "system_gamemode-miscinfo"
+++

## Status

None

## Syntax

`STATROLLTEXT:x <tab>
y`

## Parameters

-   x: Number (Stat number)
-   y: Text (Alternate stat number descriptive text)



What it does
------------

Provides a text-based descripter for stat roll numbers.

Examples
--------

`STATROLLTEXT:1 <tab> Poor`

`STATROLLTEXT:2 <tab> Low`

`STATROLLTEXT:3 <tab> Average`

`STATROLLTEXT:4 <tab> High`

`STATROLLTEXT:5 <tab> Exceptional`

`STATROLLTEXT:6 <tab> Awesome`

Character stat score of "1" will be labeled as "Poor", "2" as "Low", "3"
as "Average", "4" as "High", "5" as "Exceptional" and "6" as "Awesome".

