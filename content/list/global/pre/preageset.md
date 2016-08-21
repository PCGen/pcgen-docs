+++
date = "2016-08-01"
title = "PREAGESET (Global: PRErequisite)"
original_url = "list/global/pre.html#preageset"
categories = [ "all-tag", "pre-tag" ]
+++

## Status

Updated 5.13.12

## Syntax

`PREAGESET:x,y,y`

## Parameters

-   x: Number (Number of agesets required)
-   y: Text (Ageset abbreviation)



What it does
------------

-   Requires the PC to have the specified Ageset or older.
-   Agesets are defined in
    [biosettings.lst](/list/system/biosettings.html) files by the
    [AGESET](/list/system/biosettings/ageset.html) tag.
-   *Biosettings.lst* files can be placed in the gameMode or in the
    applicable datasets.
-   There are four Agesets defined in the 35e gameMode: Adulthood,
    Middle Age, Old, and Venerable.

Example
-------

`PREAGESET:1,Old`

Requires the PC to be "Old" or "Venerable".

`PREAGESET:1,Venerable`

Requires the PC to be "Venerable".

`!PREAGESET:1,Venerable`

Requires the PC to be younger than "Venerable".

`PREMULT:2,[PREAGESET:1,Middle Age],[!PREAGESET:1,Old]`

Requires the PC to be "Middle Age" but not older.

