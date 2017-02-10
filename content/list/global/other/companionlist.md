+++
date = "2016-08-01"
title = "COMPANIONLIST (Global: OTHER)"
original_url = "/list/global/other.html#companionlist"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "COMPANIONLIST"
    parent = "global_other"
+++

## Status

New 5.11.0

## Syntax

`COMPANIONLIST:x|y,y|z`

## Parameters




**Variables used (x):** Text (Companion Type)

**Variables used (y):** Text (Companion Race)

**Variables used (y):** RACETYPE=Text (Companion Race Type)

**Variables used (y):** RACESUBTYPE=Text (Companion Race Subtype)

**Variables used (y):** ANY

**Variables used (z):** FOLLOWERADJUSTMENT:Number (Level Adjustment)

What it does
------------

-   Adds a specific race or races to the list of available companions
    for the specified companion type.
-   PRExxx tags can be added at the end of `COMPANIONLIST` tags, PRExxx
    tags are checked against the master.
-   `FOLLOWERADJUSTMENT` will modify the masters effective level when
    determining the benefits gained from the companion creature.

Example
-------

`COMPANIONLIST:Familiar|Bat,Cat,Hawk,Lizard,Owl,Rat,Raven,Snake(Tiny/Viper),Toad,Weasel`

Would build the list consisting of the Bat, Cat, Hawk, Lizard, Owl, Rat,
Raven, Snake(Tiny/Viper), Toad, and Weasel and make them available to be
familiars.

`COMPANIONLIST:Pet|RACETYPE=Animal`

Would build a list of all animals and make them available to be a Pet.

`COMPANIONLIST:Pet|RACESUBTYPE=Fire`

Would build a list of all creatures with a race subtype of 'Fire' and
make them available to be a Pet.

`COMPANIONLIST:Familiar|Quasit|PREFEAT:1,Special Familiar|PREALIGN:CE`

A Quasit can be chosen as a Familiar but only if the master is evil and
has the Special Familiar feat.

`COMPANIONLIST:Animal Companion|Ape|FOLLOWERADJUSTMENT:-3`

An Ape companion to a 4th level master gains the benefits normally
granted to a companion of a 1st level master.

