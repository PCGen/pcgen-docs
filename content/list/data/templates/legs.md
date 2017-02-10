+++
date = "2016-08-01"
title = "LEGS (Data: templates.lst)"
original_url = "/list/data/templates.html#legs"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "LEGS"
    parent = "data_templates"
    identifier = "data_templates_LEGS"
+++

## Status

None

## Syntax

`LEGS:x`

## Parameters

-   x: Number (Number of Legs &gt;=0)



What it does
------------

-   Used to determine encumbrance and carrying capacity for
    creatures/characters with a nonstandard number of legs. (i.e. more
    than/less than 2).
-   .MOD Behavior: When modifying a template, with the `.MOD` tag, given
    an existing `LEGS` tag, the data included in a new `LEGS` tag will
    overwrite the existing tag data.

Examples
--------

`LEGS:4`

A horse has four legs.

`LEGS:0`

Slime and ooze creatures/characters would have no legs!

`<template name>.MOD <tab> LEGS:8`

The creature has eight legs.

**.MOD Example:**

Initial Template: `Odin's Blessing <tab> LEGS:8`

Modified By: `Odin's Blessing.MOD <tab> LEGS:6`

Is Equivalent To: `Odin's Blessing <tab> LEGS:6`

The recipient of this template now has "6" legs.

