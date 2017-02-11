+++
date = "2016-08-01"
title = "RACETYPE (Data: templates.lst)"
original_url = "/list/data/templates.html#racetype"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "RACETYPE"
    parent = "data_templates"
    identifier = "data_templates_RACETYPE"
+++

## Status

New 5.9.4

## Syntax

`RACETYPE:x`

## Parameters

-   x: Text (Creature Type)



What it does
------------

-   Changes the Type of creature the race is from the initial Type
    defined by [RACETYPE](/list/data/races/racetype.html) in the
    race line.
-   A Creature may only have one RACETYPE at any given time.
-   Currently existing selections from the Monster List include:\
     Aberration, Animal, Beast, Construct, Dragon, Elemental, Fey,
    Giant, Humanoid, Magical Beast, Monstrous Humanoid, Ooze, Outsider,
    Plant, Shapechanger, Undead, and Vermin
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `RACETYPE` tag, the data included in a new
    `RACETYPE` tag will overwrite the existing tag data.

Example
-------

`RACETYPE:Undead`

The creature is now of the "Undead" type.

**.MOD Example:**

Initial Template: `<template name> <tab> RACETYPE:Undead`

Modified By: `<template name>.MOD <tab> RACETYPE:Outsider`

Is Equivalent To: `<template name> <tab> RACETYPE:Outsider` .

The character is now the race type "Outsider".

