+++
date = "2016-08-01"
title = "HTDIEROLL (System: bio/biosettings.lst)"
original_url = "/list/system/biosettings.html#htdieroll"
categories = [ "all-tag", "biosettings-tag" ]
[menu.main]
    name = "HTDIEROLL"
    parent = "system_biosettings"
    identifier = "system_biosettings_HTDIEROLL"
+++

## Status

None

## Syntax

`HTDIEROLL:xdy`

## Parameters

-   x: Number (Number of dice)
-   y: Number (number of sides on the dice)



What it does
------------

The HTDIEROLL tag is used inside of the SEX tag to define the spread for
randomization in the number that is added to your base height for the
race/sex it is paired with. It also acts as a variable name that
contains the result of this randomization.

Example
-------

`HTDIEROLL:2d10`

This race added 2d10 to its base height.

