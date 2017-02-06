+++
date = "2016-08-01"
title = "PREDR (Global: PRErequisite)"
original_url = "/list/global/pre.html#predr"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREDR (Global: PRErequisite)"
    parent = "pre"
+++

## Status

None

## Syntax

`PREDR:x,y=z,y=z`

## Parameters

-   x: Number (The number of the DR conditions that
    must be met).
-   y: Text (The type of DR).
-   z: Number (Value the DR must be greater or
    equal to).



What it does
------------

Set's requirements for a character's Damage Resistance.

Examples
--------

`PREDR:1,+1=10`

Must have DR of 10/+1 or greater (but DR Type must be +1).

`PREDR:1,-=10,+1=10,+2=10,+3=10,+4=10,+5=10,Silver=10`

Must have DR of 10 or greater of any type listed.

