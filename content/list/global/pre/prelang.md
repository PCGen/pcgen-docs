+++
date = "2016-08-01"
title = "PRELANG (Global: PRErequisite)"
original_url = "/list/global/pre.html#prelang"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRELANG (Global: PRErequisite)"
    parent = "pre"
+++

## Status

None

## Syntax

`PRELANG:x,y,y`

## Parameters

-   x: Number (The number of languages a character
    must know).
-   y: Text (The name of a language the character
    must know).
-   y: ANY (Indicator the any language will be allowed
    to help meet the required number).



What it does
------------

Makes speaking certain languages a prerequisite.

Examples
--------

`PRELANG:1,Dwarven,Elven`

Character must be able to speak either "Dwarven" or "Elven".

`PRELANG:2,Dwarven,Elven`

Character must be able to speak both "Dwarven" and "Elven".

`PRELANG:2,Dwarven,Elven,Halfling`

Character must be able to speak any two of "Dwarven", "Elven" or
"Halfling".

`PRELANG:3,ANY`

Character must be able to speak any three languages.

`PRELANG:4,TYPE=Spoken`

Character must be able to speak any four languages that can be spoken.

