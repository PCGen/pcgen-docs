+++
date = "2016-08-01"
title = "TEMPLATECHOOSE (Data: templates.lst)"
original_url = "/list/data/templates.html#templatechoose"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "TEMPLATECHOOSE"
    parent = "data_templates"
+++

## Status

Updated 6.03.04

## Syntax

`TEMPLATE:CHOOSE:x|x`

## Parameters

-   x: Text (Template Name)
-   x: TYPE=Text (Valid Template Type)



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
    [Class](/list/data/classes/templatechoose.html) , and
    [Race](/list/data/races/templatechoose.html) files.

Example
-------

`TEMPLATE:CHOOSE:Celestial|Outsider`

The character is given the choice between "Celestial" or "Outsider".

