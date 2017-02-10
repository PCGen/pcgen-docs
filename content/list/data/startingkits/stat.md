+++
date = "2016-08-01"
title = "STAT (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#stat"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "STAT"
    parent = "data_startingkits"
    identifier = "data_startingkits_STAT"
+++

## Status

New 5.9.3

## Syntax

`STAT:x=y|x=y`

## Parameters

-   x: Text (Stat abbreviation)
-   y: Number, Variable or Formula (Stat value)



What it does
------------

This sets the ability scores for the character. This is done as if the
user had set them in the GUI, setting the editable scores before racial
and other bonuses are added in. Specifying all the Stats is not
required, a single Stat or more can be set and any which are not
specified are left alone.

Example
-------

`STAT:STR=15|DEX=14|WIS=10|CON=10|INT=10|CHA=18`

Sets the editable scores to those specified.

