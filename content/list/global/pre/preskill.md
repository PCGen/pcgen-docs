+++
date = "2016-08-01"
title = "PRESKILL (Global: PRErequisite)"
original_url = "/list/global/pre.html#preskill"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRESKILL"
    parent = "global_pre"
+++

## Status

None

## Syntax

`PRESKILL:x,y=z,y=z`

## Parameters

-   x: Number (Number of skills)
-   y: Text (Skill name)
-   y: TYPE.Text (Skill type)
-   z: Number (Skill ranks)



What it does
------------

-   Sets skill requirements.
-   If you require multiples of a particular type of skill, you need to
    include a `TYPE.Text` sub-tag for each instance in the comma
    delimited list.
-   Skills types with multiple versions like "Craft (Pottery)" or
    "Knowledge (Local)" there must be a space between the name and the
    parentheses because the text must match the entry exactly.

Examples
--------

`PRESKILL:1,Spot=10,Listen=10`

Character must have at least 10 ranks in either "Spot" or "Listen".

`PRESKILL:2,TYPE.Spy=2,TYPE.Spy=2`

Character must have two "Spy" skills with at least two ranks in each of
them.

`PRESKILL:3,Appraise=3,Decipher Script=3,Knowledge (TYPE=Other)=3`

Character must have three skills with at least three ranks in each of
them.

