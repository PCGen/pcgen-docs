+++
date = "2016-08-01"
title = "TEMPLATE (Data: abilities.lst)"
original_url = "/list/data/ability.html#template"
categories = [ "all-tag", "ability-tag" ]
[menu.main]
    name = "TEMPLATE"
    parent = "data_ability"
+++

## Status

Updated 5.17.x

## Syntax

`TEMPLATE:x|x`

## Parameters

-   x: Text (Template Name)



What it does
------------

-   This is a pipe-delimited (|) list of templates that are granted by
    the ability.
-   Supports `%LIST` in conjunction with a `CHOOSE` tag.

Example
-------

`TEMPLATE:Incorporeal|Undead|Celestial`

The ability applies the "Incorporeal", "Undead" and "Celestial"
templates.

