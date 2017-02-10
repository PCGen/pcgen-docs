+++
date = "2016-08-01"
title = "VISIBLE (Data: templates.lst)"
original_url = "/list/data/templates.html#visible"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "VISIBLE"
    parent = "data_templates"
    identifier = "data_templates_VISIBLE"
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

-   `YES` - Shows the Template name in PCGen and on export to a
    character sheet
-   `NO` - Hides the Template name in PCGen and on export to a
    character sheet.
-   `DISPLAY` - Displays the Template name in PCGen but not on the
    character sheet.
-   `EXPORT` - Hides the Template name from PCGen but displays it on the
    character sheet.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `VISIBLE` tag, the data included in a new
    `VISIBLE` tag will overwrite the existing tag data.

Example
-------

`VISIBLE:YES`

Shows the Template name in PCGen and on export to a character sheet.

`<template name>.MOD <tab> VISIBLE:NO`

The template will not be visible either in the GUI or on the character
sheet..

**.MOD Example:**

Initial Template: `South Philly <tab> VISIBLE:YES`

Modified By: `South Philly.MOD <tab> VISIBLE:NO`

Is Equivalent To: `South Philly <tab> VISIBLE:NO` .

The template is not visible.

