+++
date = "2016-08-01"
title = "CR (Data: templates.lst)"
original_url = "/list/data/templates.html#cr"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "CR"
    parent = "data_templates"
+++

## Status

None

## Syntax

`CR:x`

## Parameters

-   x: Number (Challenge rating adjustment &gt;0)



What it does
------------

-   This is the amount the character's challenge rating is increased by
    this template.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `CR` tag, the data included in a new `CR` tag will
    overwrite the existing tag data.

Example
-------

`CR:2`

The character's challenge rating is increased by two.

`<template name>.MOD <tab> CR:3`

The character's challenge rating is increased by three.

**.MOD Example:**

Initial Template: `Darkling <tab> CR:2`

Modified By: `Darkling.MOD <tab> CR:3`

Is Equivalent To: `Darkling <tab> CR:3`

Darklings have a "challenge rating" of "3".

