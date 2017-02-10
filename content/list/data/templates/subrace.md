+++
date = "2016-08-01"
title = "SUBRACE (Data: templates.lst)"
original_url = "/list/data/templates.html#subrace"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "SUBRACE"
    parent = "data_templates"
+++

## Status

None

## Syntax

`SUBRACE:x`

## Parameters

-   x: Text (Subrace Name)
-   x: YES



What it does
------------

-   This sets the name of the sub race the character is, the default
    is none.
-   If "YES" is specified then it will place the name of the template in
    parenthesis after the race on character sheet output.
-   `SUBRACE` should only be used once in a template line.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `SUBRACE` tag, the data included in a new
    `SUBRACE` tag will overwrite the existing tag data.

Example
-------

`SUBRACE:Ooze Monkey`

The character is part of the "Monkey Ooze" sub race.

**.MOD Example:**

Initial Template: `Ooze Monkey <tab> SUBRACE:Ooze Monkey`

Modified By: `Ooze Monkey.MOD <tab> SUBRACE:Tropical`

Is Equivalent To: `Ooze Monkey <tab> SUBRACE:Tropical` .

The Ooze Monkey is granted the "Tropical" sub-race.

