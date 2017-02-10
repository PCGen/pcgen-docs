+++
date = "2016-08-01"
title = "PREVISION (Global: PRErequisite)"
original_url = "/list/global/pre.html#prevision"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREVISION"
    parent = "global_pre"
+++

## Status

None

## Syntax

`PREVISION:x,y=z,y=z`

## Parameters

-   x: Number (Number of matching vision types)
-   y: Text (Vision type)
-   z: Number (Distance for related vision type)
-   z: ANY



What it does
------------

-   Sets the vision requirements by type and distance.
-   The variable (z) is required for each vision type (y) provided and
    determines the minimum distance required for the related
    vision type.

Examples
--------

`PREVISION:2,Normal=ANY,Darkvision=ANY`

Character must have both Normal and Darkvision.

`PREVISION:1,Blindsight=30,Darkvision=30`

Character must have either Blindsight or Darkvision at at least 30.

`PREVISION:1,Low-Light=ANY`

Character must have low-light vision to any distance.

