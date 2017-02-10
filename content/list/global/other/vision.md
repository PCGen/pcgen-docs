+++
date = "2016-08-01"
title = "VISION (Global: OTHER)"
original_url = "/list/global/other.html#vision"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "VISION"
    parent = "global_other"
    identifier = "global_other_VISION"
+++

## Status

None

## Syntax

`VISION:x (y)|x (y)`

## Parameters

-   x: Text (Vision type)
-   x: .SET.Text (Vision type)
-   x: .CLEAR.Text (Vision type)
-   y: Number or Formula (Distance)



**What it does:**

-   This tag grants the specified pipe-delimited (|) list of vision
    types to the character
-   .CLEAR. will clear the vision listed after it from the character.
-   .SET. will change the character's vision to the new vision.

Examples
--------

`VISION:Low-light`

This gives the "Low-Light" vision mode to the PC.

`VISION:Darkvision (60')`

This gives the "Dark" vision mode of 60 foot to the PC.

`VISION:Darkvision (10*TL)`

This gives the "Dark" vision mode of 10 x their total level to the PC.

`VISION:Darkvision (120')|Low-light`

This gives the "Dark" vision mode of 120 foot and the "Low-Light" vision
mode to the PC.

`VISION:.CLEAR.Low-light`

Removes the Low-light vision from the character

`VISION:Darkvision (0')<tab>BONUS:VISION|Darkvision|30`

If character does not have Darkvision, receives it at 30, or extends
Darkvision by 30 if it already has it.

