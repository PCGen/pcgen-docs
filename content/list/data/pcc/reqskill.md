+++
date = "2016-08-01"
title = "REQSKILL (Data: campaign.pcc)"
original_url = "list/data/pcc.html#reqskill"
categories = [ "all-tag", "pcc-tag" ]
+++

## Status

None

## Syntax

`REQSKILL:x`

## Parameters

-   x: ALL or REQSKILL:ALL or UNTRAINED or
    REQSKILL:UNTRAINED or Text



What it does
------------

A "|" (pipe) delimited list can include:

-   `UNTRAINED` - all untrained skills will be automatically included on
    any character as if the skill had the REQ tag (see `skill.lst` for
    details);
-   `ALL` - all skills will have the REQ tag, or;
-   a list of specified skill names.

If this tag is included it should be after the `SKILL:` tag.

Example
-------

`REQSKILL:Alchemy|Bluff|Diplomacy|etc`

