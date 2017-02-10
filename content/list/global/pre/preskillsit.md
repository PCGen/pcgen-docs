+++
date = "2016-08-01"
title = "PRESKILLSIT (Global: PRErequisite)"
original_url = "/list/global/pre.html#preskillsit"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRESKILLSIT"
    parent = "global_pre"
    identifier = "global_pre_PRESKILLSIT"
+++

## Status

New 6.03.00

## Syntax

`PRESKILLSIT:w,x,y=z,y=z`

## Parameters

-   w: Number (Number of skills)
-   x: SKILL=Text (Skill name)
-   y: Text (Situation)
-   z: Number, Variable, or Formula (Skill ranks)



What it does
------------

Sets situational skill requirements.

Examples
--------

`PRESKILLSIT:1,SKILL=Spot,Woodlands=10`

Character must have at least 10 ranks in "Spot (Woodlands)".

