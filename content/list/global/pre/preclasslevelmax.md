+++
date = "2016-08-01"
title = "PRECLASSLEVELMAX (Global: PRErequisite)"
original_url = "/list/global/pre.html#preclasslevelmax"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRECLASSLEVELMAX"
    parent = "global_pre"
+++

## Status

None

## Syntax

`PRECLASSLEVELMAX:x,y=z,y=z`

## Parameters

-   x: Number (Number of listed classes required)
-   y: Text (Class name)
-   y: TYPE.Text (Class type)
-   y: SPELLCASTER
-   y: SPELLCASTER.Text (Spellcaster type)
-   z: Number (Maximum class level)



What it does
------------

-   Sets maximum class level limits.
-   Class types are defined in the loaded datasets. Examples from the
    RSRD are "Base", "PC", or "Prestige".
-   `SPELLCASTER` will check against all spellcasting classes.
-   `SPELLCASTER.Text` will check against spellcaster types, e.g. Arcane
    or Divine.

Example
-------

`PRECLASSLEVELMAX:2,Fighter=2,SPELLCASTER=2`

Character cannot have more than 2 levels of fighter and cannot have more
than 2 levels in any spellcasting class.

