+++
date = "2016-08-01"
title = "TEMPLATEADDCHOICE (Data: templates.lst)"
original_url = "/list/data/templates.html#templateaddchoice"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "TEMPLATEADDCHOICE (Data: templates.lst)"
    parent = "templates"
+++

## Status

Updated 6.03.04

## Syntax

`TEMPLATE:ADDCHOICE:x|x`

## Parameters

-   x: Text (Template Name)
-   x: TYPE=Text (Valid Template Type)



What it does
------------

-   This is a pipe-delimited list of template choices that are added to
    the list presented by the original `TEMPLATE:CHOOSE` tag.
-   **.MOD Behavior:** When using the `TEMPLATE:ADDCOICE` tag as part of
    a `.MOD` of a Template object that containes multiple
    `TEMPLATE:CHOOSE` tags, all instances of the `TEMPLATE:CHOOSE` tag
    will be modified.

Example
-------

`TEMPLATE:ADDCHOICE:Demihuman|Beast`

The character has "Demihuman" and "Beast" added to the choice list.

