+++
date = "2016-08-01"
title = "PRESKILLMULT (Global: PRErequisite)"
original_url = "/list/global/pre.html#preskillmult"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRESKILLMULT"
    parent = "global_pre"
+++

## Status

None

## Syntax

`PRESKILLMULT:x,y=z,y=z`

## Parameters

-   x: Number (The number of skills that must be equal
    to or greater than the numbers specified for the check to succeed).
-   y: Text (A defined skill name).
-   y: TYPE=Text (A defined skill type).
-   z: Number (The number of ranks the associated skill
    must meet or exceed).



What it does
------------

-   Similar to PRESKILL.
-   This tag will set a flag on the character.
-   It only works as a prereq if the rank in the skill divided by the
    rank needed is equal to the flag.
-   The flag starts at 1, but goes up by one every-time the prereq
    is met. So the first feat would require 'rank' in the skill, the
    second feat 'rank\*2', and so on. That would support the way
    regional feats are described in FR.
-   If you require multiples of that type, you need to add TYPE.x for
    each instance in the comma delimited list.
-   This tag is merely a dummy tag that works like PRESKILL so we don't
    have to redesign the lst files when this tag gets working.

NOTE: This tag has some problems. It will work in some files but not
all.

Example
-------

`PRESKILLMULT:1,Spot=10,Listen=10`

Character must have a Spot or Listen at 10 or above.

