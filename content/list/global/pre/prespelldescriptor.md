+++
date = "2016-08-01"
title = "PRESPELLDESCRIPTOR (Global: PRErequisite)"
original_url = "/list/global/pre.html#prespelldescriptor"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRESPELLDESCRIPTOR"
    parent = "global_pre"
    identifier = "global_pre_PRESPELLDESCRIPTOR"
+++

## Status

None

## Syntax

`PRESPELLDESCRIPTOR:x,y=z`

## Parameters

-   x: Number (Number of spells known)
-   y: Text (Spell descriptor)
-   z: Number (Minimum spell level)



What it does
------------

Sets spell descriptor requirements. (i.e. Fire, Acid, Sonic, Evil, Good,
Mind-Affecting, etc.)

Example
-------

`PRESPELLDESCRIPTOR:4,Mind-Affecting=3`

Character must have at least four 3rd level or higher Mind-Affecting
spells to meet the requirement.

**Deprecated Syntax:**

`PRESPELLDESCRIPTOR:y,x,z`

