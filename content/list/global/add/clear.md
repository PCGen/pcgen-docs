+++
date = "2016-08-01"
title = "CLEAR (Global: ADD)"
original_url = "/list/global/add.html#clear"
categories = [ "all-tag", "add-tag" ]
[menu.main]
    name = "CLEAR"
    parent = "global_add"
    identifier = "global_add_CLEAR"
+++

## Status

Updated 5.11.11

## Syntax

`ADD:.CLEAR`

## Parameters

-   x: Number (Class level)



**Tag Name:** ADD:.CLEAR.LEVELx

What it does
------------

-   Used to clear an ADD tag.
-   Can be used in conjunction with the
    [.MOD](/list/global/other/mod.html) tag to alter a class or
    other objects.
-   Using an ADD.CLEAR.LEVELx on a class line or on a level line where
    the level does not equal X will result in a warning, and may not be
    supported in the future.

Example
-------

`ADD:.CLEAR.LEVEL2`

If this were used in a CLASS:Rogue.MOD line it would clear the
`ADD:FEAT(Evasion, Improved Evasion)` tag normally found there and allow
you to add a new one, perhaps:
`ADD:FEAT (Evasion,Improved Evasion,Shadow)` .

`ADD:.CLEAR`

If this were used in a Zombie.MOD line it would clear the
`ADD:FEAT (TYPE=SlamWeapons)` tag normally found in that template.

`CLASS:Gunslinger.MOD <tab> ADD:.CLEAR.LEVEL2 <tab> ADD:.CLEAR.LEVEL3 <tab> ADD:.CLEAR.LEVEL6 <tab> ADD:.CLEAR.LEVEL8 <tab> ADD:.CLEAR.LEVEL9`

This modification of the Gunslinger Class removes the benefits of levels
2, 3, 6, 8, and 9, replacing them with nothing.

