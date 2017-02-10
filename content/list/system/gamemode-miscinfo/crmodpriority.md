+++
date = "2016-08-01"
title = "CRMODPRIORITY (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#crmodpriority"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "CRMODPRIORITY"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 6.1.2

## Syntax

`CRMODPRIORITY:x`

## Parameters

-   x: Integer.



What it does
------------

If a character has multiple classes with different class types (such as,
for example, an aristocrat/fighter), this tag determines which CRMOD is
applied. For Pathfinder, if a character has a PC class, the CRMOD is
â€“1, but if he has ONLY NPC classes, the CRMOD is â€“2. Thus, the PC
CRMOD takes priority. The CRMODPROIRITY tag determines the priority in a
way that PCGen will choose the CRMOD with the lowest value of
CRMODPROIRITY.

Example
-------

`CRMODPRIORITY:1`

The CRMOD of this class type has the higher priority.

Where it is used
----------------

CLASSTYPE Line.

