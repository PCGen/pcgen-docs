+++
date = "2016-08-01"
title = "PRESPELLSCHOOLSUB (Global: PRErequisite)"
original_url = "/list/global/pre.html#prespellschoolsub"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRESPELLSCHOOLSUB"
    parent = "global_pre"
    identifier = "global_pre_PRESPELLSCHOOLSUB"
+++

## Status

Updated 5.12

## Syntax

`PRESPELLSCHOOLSUB:x,y=z,y=z`

## Parameters

-   x: Number (Number of spells known)
-   y: Text (Name of sub-school of magic.)
-   z: Number (Minimum spell level)



What it does
------------

-   Establishes a requirement for (x) number of spells from magic
    sub-school (y) of at least level (z).
-   You may include as many "Sub-School=Level" pairs as you require as a
    comma-delimited (",") list.

Example
-------

`PRESPELLSCHOOLSUB:3,Creation=2`

Character must have at least three 2nd level "Creation" spells to meet
the requirement.

