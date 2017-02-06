+++
date = "2016-08-01"
title = "SKILLLIST (Data: classes.lst)"
original_url = "/list/data/classes.html#skilllist"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "SKILLLIST (Data: classes.lst)"
    parent = "classes"
+++

## Status

None

## Syntax

`SKILLLIST:x|y|y`

## Parameters

-   x: Number (Number of choices)
-   y: Text (Class Name)



What it does
------------

This is a | (pipe) delimited list of class names that the class can
choose from to duplicate class skills.

Examples
--------

`SKILLLIST:1|Ranger`

The class can choose from Ranger class skills.

`SKILLLIST:1|Ranger|Druid`

The class can choose either from Ranger or Druid class skills.

`SKILLLIST:2|Ranger|Druid|Barabarian`

The class can choose from 2 of Ranger, Druid or Barbarian class skills.

Where it is used
----------------

Class Line.

