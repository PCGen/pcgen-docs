+++
date = "2016-08-01"
title = "ENCUMBRANCE (Game Mode: load.lst"
original_url = "list/system/gamemode-load.html#encumbrance"
categories = [ "all-tag", "gamemode-load-tag" ]
+++

## Status

None

## Syntax

`ENCUMBRANCE:w|x|y|z`

## Parameters

-   w: Text (Name of load category)
-   x: Number (Multiplier - Portion of full load
    covered by encumbrance category)
-   y: Text (Move formula. Optional)
-   z: Number (Check Penalty)



<span id="encumbrance"></span> \*\*\* New 5.7.12

What it does
------------

-   This tag defines the Load Categories used by the output sheets and
    is set by gameMode.
-   The `ENCUMBRANCE` tag expects either two or four parameters with
    parameters (y) and (z) being optional.
-   If the move formula, parameter (y), is not included the gameMode's
    default move formula will be used.
-   The following six load categories are hardcoded into PCGen and are
    required to be included in all <span class="lstfile"> load.lst
    </span> files:
    -   Light
    -   Medium
    -   Heavy
    -   OverHead
    -   OffGround
    -   PushDrag
-   Additional categories may be defined as needed.
-   The `ENCUMBRANCE` tag defines the output token used. See the entry
    for the output token
    [WEIGHT](/outputsheet/tokens/general.html#weight)

Note: Parameter (z) can be included without parameter (y) but you will
need to include a double pipe (||) in its place as PCGen still expects 4
parameters. Examples are provided below.

Example
-------

`ENCUMBRANCE:Light|1/3||0`

`ENCUMBRANCE:Medium|2/3||-3`

`ENCUMBRANCE:Heavy|1||-6`

`ENCUMBRANCE:OverHead|1||-6`

`ENCUMBRANCE:OffGround|2||-6`

`ENCUMBRANCE:PushDrag|5||-6`

These six categories must be included in all gameModes.

`ENCUMBRANCE:FooBar|8`

The OS output token for this load category is `WEIGHT.FOOBAR` .

