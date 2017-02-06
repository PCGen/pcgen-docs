+++
date = "2016-08-01"
title = "TEMPLATEADDCHOICE (Data: classes.lst)"
original_url = "/list/data/classes.html#templateaddchoice"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "TEMPLATEADDCHOICE (Data: classes.lst)"
    parent = "classes"
+++

## Status

None

## Syntax

`TEMPLATE:ADDCHOICE:x|x`

## Parameters

-   x: Text (Template Name)



What it does
------------

-   This is a pipe-delimited list of template choices that are added to
    the list presented by the original TEMPLATE:CHOOSE tag.
-   When using the `TEMPLATE:ADDCOICE` tag as part of a `.MOD` of a
    class that containes multiple `TEMPLATE:CHOOSE` tags, all instances
    of the `TEMPLATE:CHOOSE` tag will be modified.

Example
-------

`TEMPLATE:ADDCHOICE:Demihuman|Beast`

The class can choose previously defined templates plus the "Demihuman"
or "Beast" templates.

Where it is used
----------------

Class Level Line

