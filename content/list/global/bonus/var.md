+++
date = "2016-08-01"
title = "VAR (Global: BONUS)"
original_url = "/list/global/bonus.html#var"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "VAR"
    parent = "global_bonus"
+++

## Status

Updated 5.7.3

## Syntax

`BONUS:VAR|x,x|y`

## Parameters

-   x: Text (Variable name)
-   y: Number, variable or formula (Number to adjust
    variable by)



What it Does
------------

-   Adds to a user-defined variable within the loaded data sets.
-   A [DEFINE](/list/global/define.html) tag for the listed variable
    must be included within the loaded data sets and must be attached to
    the character for a BONUS to have any effect.

Examples
--------

`BONUS:VAR|SneakAttack|2`

Adds 2 to character's SneakAttack variable.

`BONUS:VAR|SneakAttack,TrapSense|1`

Adds 1 to character's SneakAttack and TrapSense variables.

`BONUS:VAR|TurnTimesBase|3+CHA|TYPE=Base`

Sets the character's base TurnTimesBase variable to three plus the
Charisma Modifier.

`TEMPBONUS:ANYPC|VAR|LegacyPoints|%CHOICE|PRERACE:1,Titan <tab> CHOOSE:NUMBER|MIN=1|MAX=10|TITLE=Legacy Points`

A chooser to let you select the number of points to add, from 1 to 10,
if you're a Titan and a PC.

