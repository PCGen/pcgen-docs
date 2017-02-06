+++
date = "2016-08-01"
title = "PRECHARACTERTYPE (Global: PRErequisite)"
original_url = "/list/global/pre.html#precharactertype"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRECHARACTERTYPE (Global: PRErequisite)"
    parent = "pre"
+++

## Status

New 5.17.12

## Syntax

`PRECHARACTERTYPE:x,y,y`

## Parameters

-   x: Number (Number of character types required)
-   y: Text (Character type.)



What it does
------------

Sets requisites for character type.

Examples
--------

PRECHARACTERTYPE:1,PC

Character must be designated as a **PC** .

PRECHARACTERTYPE:1,NPC,Monster

Character must be a designated either as an **NPC** or as a **Monster**
.

