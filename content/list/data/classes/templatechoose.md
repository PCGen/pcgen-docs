+++
date = "2016-08-01"
title = "TEMPLATECHOOSE (Data: classes.lst)"
original_url = "/list/data/classes.html#templatechoose"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "TEMPLATECHOOSE"
    parent = "data_classes"
    identifier = "data_classes_TEMPLATECHOOSE"
+++

## Status

None

## Syntax

`TEMPLATE:CHOOSE:x|x`

## Parameters

-   x: Text (Template Name)



What it does
------------

-   Will present a popup window of the choices provided in the
    pipe-delimited (|) list, allowing the user to pick ONE from
    the list.
-   Multiple `TEMPLATE:CHOOSE` tags can be used in the same LST object
    but PCGen's current Data Standard is to include no more that one in
    each LST object.
-   Though the `TEMPLATE:CHOOSE` tag is not a gobal tag it can be used
    in the [Ability](/list/data/ability/templatechoose.html) ,
    [Race](/list/data/races/templatechoose.html) , and
    [Template](/list/data/templates/templatechoose.html) files.

Example
-------

`TEMPLATE:CHOOSE:Celestial|Outsider`

The class can choose either the "Celestial" or "Outsider" template.

Where it is used
----------------

Class Level Line

