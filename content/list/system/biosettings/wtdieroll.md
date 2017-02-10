+++
date = "2016-08-01"
title = "WTDIEROLL (System: bio/biosettings.lst)"
original_url = "/list/system/biosettings.html#wtdieroll"
categories = [ "all-tag", "biosettings-tag" ]
[menu.main]
    name = "WTDIEROLL"
    parent = "system_biosettings"
+++

## Status

None

## Syntax

`WTDIEROLL:xdy`

## Parameters

-   x: Number (Number of dice)
-   y: Number (number of sides on the dice)



What it does
------------

The WTDIEROLL tag is used inside of the SEX tag to define the spread for
randomization in the number that is added to your base weight for the
race/sex it is paired with. It also acts as a variable name that
contains the result of this randomization.

Example
-------

`WTDIEROLL:2d4`

This race added 2d10 to its base weight.

