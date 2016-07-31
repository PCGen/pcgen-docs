+++
date = "2016-08-01"
title = "SHOWCLASSDEFENSE (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#showclassdefense"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

None

## Syntax

`SHOWCLASSDEFENSE:x`

## Parameters

-   x: Boolean (YES or NO).



What it does
------------

-   Determines whether Defensive bonus from classes is displayed on the
    Class Tab.
-   YES - Allow bonuses of the BONUS:COMBAT|AC|x|TYPE=ClassDefense type
    to be displayed.
-   NO - Do not allow bonuses of the BONUS:COMBAT|AC|x|TYPE=ClassDefense
    type to be displayed (Default).
-   If this tag is YES, then the Class tab will reflect any AC bonuses
    given with a BONUS:COMBAT|AC|x|TYPE=ClassDefense tag.

Example
-------

`SHOWCLASSDEFENSE:YES`

Allow bonuses of the BONUS:COMBAT|AC|x|TYPE=ClassDefense type to be
displayed.

