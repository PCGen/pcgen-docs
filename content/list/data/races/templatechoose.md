+++
date = "2016-08-01"
title = "TEMPLATECHOOSE (Data: races.lst)"
original_url = "/list/data/races.html#templatechoose"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "TEMPLATECHOOSE"
    parent = "data_races"
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
-   Although the `TEMPLATE:CHOOSE` tag is not a gobal tag it can be used
    in the [Ability](/list/data/ability/templatechoose.html) ,
    [Class](/list/data/classes/templatechoose.html) , and
    [Template](/list/data/templates/templatechoose.html) files.

Example
-------

`TEMPLATE:CHOOSE:Celestial|Outsider`

The race can choose either the "Celestial" or "Outsider" template.

