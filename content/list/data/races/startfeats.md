+++
date = "2016-08-01"
title = "STARTFEATS (Data: races.lst)"
original_url = "/list/data/races.html#startfeats"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "STARTFEATS (Data: races.lst)"
    parent = "races"
+++

## Status

None

## Syntax

`STARTFEATS:x`

## Parameters

-   x: Number (Number of Starting Feats)



<span id="startfeats"></span> \*\*\* Updated before 5.12.0

What it does
------------

-   Grants a number of free feats to the race at first level. These are
    unrestricted feats. To restrict choice (such as "only
    Fighter feats") use the global ADD:FEAT() tag.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `STARTFEATS` tag, the data included in a new
    `STARTFEATS` tag will be included as if it were a separate tag.

Example
-------

`STARTFEATS:2`

The race starts with 2 free feats.

**.MOD Example:**

Initial Race: `Werewolf <tab> STARTFEATS:2`

Modified By: `Werewolf.MOD <tab> STARTFEATS:2`

Is Equivalent To: `Werewolf <tab> STARTFEATS:2 <tab> STARTFEATS:2`

The Werewolf now starts with 4 free feats.

