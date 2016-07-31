+++
date = "2016-08-01"
title = "PRESPELLSCHOOL (Global: PRErequisite)"
original_url = "list/global/pre.html#prespellschool"
categories = [ "all-tag", "pre-tag" ]
+++

## Status

NEW 5.12

## Syntax

`PRESPELLSCHOOL:x,y=z,y=z`

## Parameters

-   x: Number (Number of spells known)
-   y: Text (Name of a school of magic).
-   z: Number (Minimum spell level)



What it does
------------

-   Establishes a requirement for (x) number of spells from magic
    school (y) of at least level (z).
-   You may include as many "School=Level" pairs as you require as a
    comma-delimited (",") list.

Example
-------

`PRESPELLSCHOOL:3,Necromancy=2`

Character must have at least three 2nd level or higher Necromancy spells
to meet the requirement.

