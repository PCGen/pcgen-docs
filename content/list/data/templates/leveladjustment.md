+++
date = "2016-08-01"
title = "LEVELADJUSTMENT (Data: templates.lst)"
original_url = "/list/data/templates.html#leveladjustment"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "LEVELADJUSTMENT"
    parent = "data_templates"
    identifier = "data_templates_LEVELADJUSTMENT"
+++

## Status

Updated 5.4

## Syntax

`LEVELADJUSTMENT:x`

## Parameters

-   x: Number or Formula (Level Adjustment)



What it does
------------

-   Raises the Effective Character Level (ECL) of the creature by the
    number specified by adding the Level Adjustment to the Monster Hit
    Dice and/or Character Levels.
-   The ECL is factored in when determining how much experience is
    needed to raise a character's level. For example, a 1st level
    character with a Level adjustment of 3 would need the same amount of
    experience to reach 2nd level as a 4th level character with no level
    adjustments would need to reach 5th level.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `LEVELADJUSTMENT` tag, the data included in a new
    `LEVELADJUSTMENT` tag will overwrite the existing tag data.

Example
-------

`LEVELADJUSTMENT:1`

Effective Character Level is raised by one.

`<template name>.MOD <tab> LEVELADJUSTMENT:3`

The character's ECL is raised by three.

**.MOD Example:**

Initial Template: `Darkling <tab> LEVELADJUSTMENT:2`

Modified By: `Darkling.MOD <tab> LEVELADJUSTMENT:4`

Is Equivalent To: `Darkling <tab> LEVELADJUSTMENT:4`

The Darkling's Effective Character Level (ECL) is raised by "4".

