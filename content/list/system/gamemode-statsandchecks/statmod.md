+++
date = "2016-08-01"
title = "STATMOD (Game Mode: statsandchecks.lst)"
original_url = "/list/system/gamemode-statsandchecks.html#statmod"
categories = [ "all-tag", "gamemode-statsandchecks-tag" ]
[menu.main]
    name = "STATMOD (Game Mode: statsandchecks.lst)"
    parent = "gamemode-statsandchecks"
+++

## Status

None

## Syntax

`STATMOD:x or
if(x,y,z)`

## Parameters

-   x: Formula (Any valid formula).
-   y: Formula (Any valid formula).
-   z: Formula (Any valid formula).



<span id="statmod"></span> \*\*\* Updated 5.10.1

What it does
------------

Defines the formula used to determine a stats modifiers.

Example
-------

`STATMOD:floor(SCORE/2)-5`

Would calculate a stat modification as STAT divided by 2, round down,
minus 5 (SCORE is the variable name for the stat value). Note: the
formula can only contain 1 SCORE variable.

`STATMOD:if(CL<10,1,2)`

Would compare CL to 10 and return 1 or 2 as required.

`STATMOD:if((CL>5)||(TL>5),2,-4)`

Asks if Class Level or Total Level is greater than 5 then returns 2 or
else returns -4.

`STATMOD:if(STR>DEX,STR,DEX)`

Asks if STR is greater than DEX then returns STR or else returns DEX

Where it is used
----------------

STATNAME Line.

