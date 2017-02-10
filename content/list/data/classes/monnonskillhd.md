+++
date = "2016-08-01"
title = "MONNONSKILLHD (Data: classes.lst)"
original_url = "/list/data/classes.html#monnonskillhd"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "MONNONSKILLHD"
    parent = "data_classes"
+++

## Status

None

## Syntax

`MONNONSKILLHD:x`

## Parameters

-   x: Number (Number of hit dice)



<span id="monnonskillhd"></span> \*\*\* Added 5.7.9

What it does
------------

Defines the number of hit dice the monster does not get skill points
for. This is normally defined by size, so the tag is normally seen with
a PRESIZE requirement.

Example
-------

`MONNONSKILLHD:32|PRESIZEEQ:C`

A colossal monster would not get skill points for the first 32
levels/hit dice of this class.

Where it is used
----------------

Class Line.

