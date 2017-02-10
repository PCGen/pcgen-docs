+++
date = "2016-08-01"
title = "VISIBLE (Data: feats.lst)"
original_url = "/list/data/feats.html#visible"
categories = [ "all-tag", "feats-tag" ]
[menu.main]
    name = "VISIBLE"
    parent = "data_feats"
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



What it does
------------

-   `YES` - Shows the feat name in PCGen and on export to a
    character sheet.
-   `NO` - Hides the feat name in PCGen and on export to a
    character sheet.
-   `DISPLAY` - Displays the feat name in PCGen but not on the
    character sheet.
-   `EXPORT` - Hides the feat name from PCGen but displays it on the
    character sheet.
-   **.MOD Behavior:** When modifying a feat with the `.MOD` tag, given
    an existing `VISIBLE` tag, the data included in a new `VISIBLE` tag
    will overwrite the existing tag data.

Example
-------

`VISIBLE:YES`

Shows the feat name in PCGen and on the Output sheet.

**.MOD Example:**

Initial Feat: `<feat name> <tab> VISIBLEE:YES`

Modified By: `<feat name> <tab> VISIBLE:DISPLAY`

Is Equivalent To: `<feat name> <tab> VISIBLE:DISPLAY`

Modified feat will appear in the GUI but will not appear on the output
sheet.

