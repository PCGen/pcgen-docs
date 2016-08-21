+++
date = "2016-08-01"
title = "STAT (Global: BONUS)"
original_url = "list/global/bonus.html#stat"
categories = [ "all-tag", "bonus-tag" ]
+++

## Status

None

## Syntax

`BONUS:STAT|x,x|y`

## Parameters

-   x: Text (Stat name)
-   y: Number, variable or formula (Number to adjust
    stat by)



What it Does
------------

Adds to character stats (stat can be any stat that has been defined in
the statsandchecks.lst system file).

Examples
--------

`BONUS:STAT|STR|2`

Adds two to character's STR stat.

`BONUS:STAT|DEX,CON,INT|1`

Adds 1 to character's DEX, CON, & INT stats.

`CHOOSE:PCSTAT|STR|DEX|CON <tab> STACK:NO <tab> MULT:YES <tab> BONUS:STAT|%LIST|1|TYPE=Inherent`

Adds 1 to character's STR, DEX, & CON stats, can be chosen multiple
times, does not stack.

`#Dwarf Racial Progression.MOD <tab> BONUS:STAT|CON|2|PRELEVEL:3 <tab> BONUS:STAT|STR|2|PRELEVEL:5 <tab> BONUS:STAT|CON|2|PRELEVEL:7 <tab> BONUS:STAT|WIS|2|PRELEVEL:9`

Modifies the character based on what level they are, i.e. +2 to CON at
3, +2 to STR at 5, +2 to CON at 7, +2 to WIS at 9.

`STACK:NO <tab> MULT:YES <tab> CHOOSE:PCSTAT|STR|DEX|CON <tab> BONUS:STAT|%LIST|2|TYPE=Inherent`

Adds two to character's Chosen stat from Inherent ability, doesn't
stack, but can be selected multiple times.

