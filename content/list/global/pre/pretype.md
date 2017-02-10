+++
date = "2016-08-01"
title = "PRETYPE (Global: PRErequisite)"
original_url = "/list/global/pre.html#pretype"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRETYPE"
    parent = "global_pre"
    identifier = "global_pre_PRETYPE"
+++

## Status

None

## Syntax

`PRETYPE:x,y,y`

## Parameters

-   x: Number (Number of types required)
-   y: Text (Type)



What it does
------------

-   Sets specific "type" requirements appropriate to the object being
    applied to, i.e. Racial, Equipment, EqMod, Template, etc.
-   See the `PRETYPE` entry in
    [Equipment](/list/data/equipment/pretype.html) or [Equipment
    Modifier](/list/data/equipmentmodifiers/pretype.html) files
    for usage.
-   If you need to prerequisite race type from equipment you can use
    [PRETEMPLATE](/list/global/pre/pretemplate.html) to check for the
    racial type template.

Examples
--------

`PRETYPE:1,Elemental,Fey,Outsider`

Type must either "Elemental", "Fey" or "Outsider".

`PRETYPE:2,Humanoid,Undead`

Character must be an "Undead Humanoid".

`PRETYPE:1,Heavy`

Object must have the type "Heavy".

