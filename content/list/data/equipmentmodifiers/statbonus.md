+++
date = "2016-08-01"
title = "STATBONUS (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#statbonus"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "STATBONUS"
    parent = "data_equipmentmodifiers"
+++

## Status

None

## Syntax

`CHOOSE:STATBONUS|w|x|y|z`

## Parameters

-   w: Text (Stat abbreviation. Optional)
-   x: MIN=Number (Lowest value to choose from)
-   y: MAX=Number (Highest value to choose from)
-   z: TITLE=Text (Chooser dialog title)



<span id="statbonus"></span> \*\*\* Updated 5.13.8

What it does
------------

You get a pop-up dialogue that allows you to select a number between
(and including) the high and low values

**Note:** This will only bring up the chooser if invoked from the
Temporary Bonus tab.

Example
-------

`CHOOSE:STATBONUS|INT|MIN=2|MAX=5|TITLE=Enhancement Bonus`

Will let you choose a number between 2 and 5 as an enhancment bonus to
the "Intelligence" bonus.

