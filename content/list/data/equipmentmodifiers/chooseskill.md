+++
date = "2016-08-01"
title = "CHOOSESKILL (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#chooseskill"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "CHOOSESKILL (Data: equipment_modifiers.lst)"
    parent = "equipmentmodifiers"
+++

## Status

None

## Syntax

`CHOOSE:SKILL|x|x|y`

## Parameters

-   x: Text (Skill name)
-   x: TYPE=Text (Skill type)
-   y: TITLE=Text (Chooser dialog title)



<span id="chooseskill"></span> \*\*\* Updated 5.13.8

What it does
------------

You get a pop-up dialogue that allows you to select a "Skill" from the
presented list.

**Note:** This will only bring up the chooser if invoked from the
Temporary Bonus tab.

Example
-------

`CHOOSE:SKILL|Climb|Jump|Balance|Tumble|TITLE=Acrobatics Skill Bonus`

Will let you select "Climb", "Jump", "Balance", or "Tumble" as an
"Acrobatic Skill Bonus".

