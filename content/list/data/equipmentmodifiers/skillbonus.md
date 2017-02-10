+++
date = "2016-08-01"
title = "SKILLBONUS (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#skillbonus"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "SKILLBONUS"
    parent = "data_equipmentmodifiers"
+++

## Status

None

## Syntax

`CHOOSE:SKILLBONUS|w|x|y|z`

## Parameters

-   w: Text (Skill name)
-   w: TYPE=Text (Skill type)
-   x: MIN=Number (Lowest value to choose from)
-   y: MAX=Number (Highest value to choose from)
-   z: TITLE=Text (Chooser dialog title)



<span id="skillbonus"></span> \*\*\* Updated 5.13.8

What it does
------------

You get a pop-up dialogue that allows you to select a number between
(and including) the high and low values

**Note:** This will only bring up the chooser if invoked from the
Temporary Bonus tab.

Example
-------

`CHOOSE:SKILLBONUS|Climb|MIN=2|MAX=5|TITLE=Enhancement Bonus`

Will let you choose a number between 2 and 5 as an enhancement bonus to
the "Climb" skill.

