+++
date = "2016-08-01"
title = "MAXLEVEL (Data: classes.lst)"
original_url = "/list/data/classes.html#maxlevel"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "MAXLEVEL"
    parent = "data_classes"
    identifier = "data_classes_MAXLEVEL"
+++

## Status

None

## Syntax

`MAXLEVEL:x`

## Parameters

-   x: Number (Maximum allowed level of this class)
-   x: NOLIMIT (No upper limit to the number of levels
    in this class)



What it does
------------

-   This is maximum number of levels a character can take in this class.
-   If no MAXLEVEL tag is supplied for a class, no limit is imposed.
-   There is a checkbox in the Preferences|Character section of the menu
    to allow this to be overridden.

Example
-------

`MAXLEVEL:10`

The maximum class level is 10.

`CLASS:Barbarian.MOD <tab> MAXLEVEL:100`

The maximum class level is modified to 100.

`CLASS:Barbarian.MOD <tab> MAXLEVEL:NOLIMIT`

Remove the previously specified maximum class level for barbarian.

Where it is used
----------------

Class Line.

