+++
date = "2016-08-01"
title = "EXCHANGELEVEL (Data: classes.lst)"
original_url = "/list/data/classes.html#exchangelevel"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "EXCHANGELEVEL"
    parent = "data_classes"
    identifier = "data_classes_EXCHANGELEVEL"
+++

## Status

None

## Syntax

`EXCHANGELEVEL:w|x|y|z`

## Parameters

-   w: Text (Class Name)
-   x: Number (Class level, minimum level required in
    donating class)
-   y: Number (Class level, maximum levels donated
    from class)
-   z: Number (Class level, lowest that donation can
    lower donating class level to)



What it does
------------

Allows the exchange of levels from the current class to the specified
class.

Example
-------

`EXCHANGELEVEL:Ex Paladin|11|10|1`

Up to 10 levels of Ex Paladin can be exchanged as long as there were at
least 11 levels of Ex Paladin available.

Where it is used
----------------

Class Line.

