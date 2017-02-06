+++
date = "2016-08-01"
title = "PRESR (Global: PRErequisite)"
original_url = "/list/global/pre.html#presr"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRESR (Global: PRErequisite)"
    parent = "pre"
+++

## Status

None

## Syntax

`PRESRx:y`

## Parameters

-   x: EQ (Equals).
-   x: GT (Greater Than).
-   x: GTEQ (Greater Than or Equal to).
-   x: LT (Less Than).
-   x: LTEQ (Less Than or Equal to).
-   x: NEQ (Not Equal to).
-   y: Number (The minimum Spell Resistance required).



What it does
------------

Makes a character's spell resistance (not including SR from equipment) a
prerequisite.

Example
-------

`PRESRGTEQ:10`

Character must have spell resistance of 10 or greater.

`PRESREQ:10`

Character must have spell resistance of exactly 10.

