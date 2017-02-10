+++
date = "2016-08-01"
title = "VISIBLE (Data: abilities.lst)"
original_url = "/list/data/ability.html#visible"
categories = [ "all-tag", "ability-tag" ]
[menu.main]
    name = "VISIBLE"
    parent = "data_ability"
    identifier = "data_ability_VISIBLE"
+++

## Status

None

## Syntax

`VISIBLE:x`

## Parameters

-   x: YES (Default)
-   x: NO
-   x: DISPLAY
-   x: EXPORT



<span id="visible"></span> \*\*\* Added 5.11.x

What it does
------------

-   `YES` - Shows the ability name in PCGen and on export to a
    character sheet.
-   `NO` - Hides the ability name in PCGen and on export to a
    character sheet.
-   `DISPLAY` - Displays the ability name in PCGen but not on the
    character sheet.
-   `EXPORT` - Hides the ability name from PCGen but displays it on the
    character sheet.
-   **.MOD Behavior:** When modifying an ability with the `.MOD` tag,
    given an existing `VISIBLE` tag, the data included in a new
    `VISIBLE` tag will overwrite the existing tag data.

Example
-------

`VISIBLE:YES`

Shows the ability name in PCGen and on the Output sheet.

**.MOD Example:**

Initial Ability:
`CATEGORY=<category name>|<ability name> <tab> VISIBLEE:YES`

Modified By:
`CATEGORY=<category name>|<ability name> <tab> VISIBLE:DISPLAY`

Is Equivalent To:
`CATEGORY=<category name>|<ability name> <tab> VISIBLE:DISPLAY`

Modified ability will appear in the GUI but will not appear on the
output sheet.

