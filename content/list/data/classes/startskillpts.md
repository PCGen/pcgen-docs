+++
date = "2016-08-01"
title = "STARTSKILLPTS (Data: classes.lst)"
original_url = "/list/data/classes.html#startskillpts"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "STARTSKILLPTS"
    parent = "data_classes"
+++

## Status

None

## Syntax

`STARTSKILLPTS:x`

## Parameters

-   x: Number



What it does
------------

This is how many skill points a character gains per level.

Formulas can be used as well.

Example
-------

`STARTSKILLPTS:4`

Class gets 4 skill points per level, before any modifiers.

`STARTSKILLPTS:4+INT`

Class gets 4 skill points per level plus the INT Bonus points, before
any modifiers.

`STARTSKILLPTS:4/CHA`

Class gets 4 skill points per level divided by the CHA Bonus points,
before any modifiers.

`CLASS:Blackguard.MOD <tab> STARTSKILLPTS:2 <tab> CSKILL:.CLEAR|Handle Animal|Ride <tab> CSKILL:Concentration|TYPE.Craft|Diplomacy|Heal|Intimidate|Knowledge (Religion) |TYPE.Profession|Climb|Jump|Listen|Spot|Swim|Pilot <tab> CCSKILL:Handle Animal|Ride`

Modified Class that changes all of these Tags from their starting
values..

Where it is used
----------------

Class Line.

