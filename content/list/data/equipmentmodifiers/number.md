+++
date = "2016-08-01"
title = "NUMBER (Data: equipment_modifiers.lst)"
original_url = "list/data/equipmentmodifiers.html#number"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
+++

## Status

None

## Syntax

`CHOOSE:NUMBER|v|w|x|y|z`

## Parameters

-   v: Number (Number choice)
-   w: MIN=Number (Lowest value to choose from. Not
    used if descrete number choices provided.)
-   x: MAX=Number (Highest value to choose from)
-   y: INCREMENT=Number (Steps between Min and Max.
    Optional - Used only if MIN and Max are used.)
-   z: TITLE=Text (Chooser dialog title)



<span id="number"></span> \*\*\* Updated 5.13.8

What it does
------------

Produces a pop-up dialogue with title (z) with a list of that allows you
to select a number between (and including) the high and low values

**Note:** This will only bring up the chooser if invoked from the
Temporary Bonus tab.

Example
-------

`CHOOSE:NUMBER|MIN=2|MAX=5|TITLE=Roll 1d4+1 and pick a number`

Will let you choose a number between 2 and 5. (Simulates rolling 1d4+1).

