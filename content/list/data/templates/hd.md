+++
date = "2016-08-01"
title = "HD (Data: templates.lst)"
original_url = "/list/data/templates.html#hd"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "HD"
    parent = "data_templates"
+++

## Status

Updated 5.11.11

## Syntax

` HD:x:y:z`

## Parameters

-   x: Calculation (range or minimum natural Hit Dice)
-   y: ANY valid Template or Global Token which can
    accept trailing PRE tags can be used
-   z: Number or Text (Must be valid for the tag used)



What it does
------------

-   The numeric values supplied are a range (1-3) or minimum (4+) hit
    dice the character must have before an ability is granted to
    the character.
-   This is Natural Hit Dice, not character level.
-   The ability of these tags have been enhanced so that they can call
    any global tag.
-   The text may contain the following tags:
    -   CR - [Challenge Rating](/list/data/templates/cr.html)
    -   DR - [Damage Reduction](/list/global/other/dr.html)
    -   FEAT - [Feat](/list/data/templates.html#feat)
    -   SA - [Special Ability](/list/global/other/sab.html)
    -   SR - [Spell Resistance](/list/global/other/sr.html)
    -   Any valid Template or Global Token which can accept trailing PRE
        tags can also be used
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `HD` tag, the data included in a new `HD` tag will
    be included as if it were a separate tag.

Examples
--------

`HD:1-3:DR:5/1`

Grants Damage Reduction of 5/+1 if natural hit dice is between one and
three.

`HD:1+:SR:15`

Grants Spell Resistance of 15 if natural hit dice is greater than one.

`HD:2-7:CR:2`

Grants an increase in Challenge Rating of two if natural hit dice is
between two and seven.

`HD:15+:SA:Uncanny Dodge`

Grants the "Uncanny Dodge" special ability if natural hit dice is
greater than fifteen.

`HD:10+:FEAT:Alertness`

Grants the "Alertness" feat if natural hit dice is greater than ten.

**.MOD Example:**

Initial Template: `Werewolf <tab> HD:1-3:DR:5/1`

Modified By: `Werewolf.MOD <tab> HD:2-7:CR:2`

Is Equivalent To: `Werewolf <tab> HD:1-3:DR:5/1 <tab> HD:2-7:CR:2` .

The werewolf gains Damage Reduction of "5/1" if natural hit dice is
between one and three, and is granted an increase in Challenge Rating of
two if natural hit dice is between two and seven.

