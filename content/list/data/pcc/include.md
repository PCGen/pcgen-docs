+++
date = "2016-08-01"
title = "INCLUDE (Data: campaign.pcc)"
original_url = "list/data/pcc.html#include"
categories = [ "all-tag", "pcc-tag" ]
+++

## Status

None

## Syntax

`(INCLUDE:y|y)`

## Parameters

-   x: Text (Ability category)
-   y: Text (LST object name)



**Tag Name:** (INCLUDE:CATEGORY=x,y,y|x,y,y) - Special syntax for feats
and abilities

What it does
------------

-   The INCLUDE tag and its arguments are enclosed within a pair
    of parentheses.
-   The tag will add the pipe-delimited list of LST objects from the LST
    file the tag is associated with.
-   The tag will not prevent other .pcc files from loading the same
    LST file.
-   LST objects can include any of the following types: ABILITY, CLASS,
    COMPANIONMODS, DEITY, DOMAIN, EQUIPMENT, EQUIPMOD, FEAT, KIT,
    LANGUAGE, RACE, SKILL, SPELL, TEMPLATE, WEAPONPROF

<span class="new"> IMPORTANT NOTE: </span> Using INCLUDE for the same
file on multiple lines will cause only the first line with INCLUDE to be
processed.

Example
-------

`RACE:myrace.lst|(INCLUDE:Happy Elf|Dower Dwarf)`

This loads only the "Happy Elf" and the "Dower Dward" from `myrace.lst`
.

`ABILITY:myability.lst|(INCLUDE:CATEGORY=Class Ability,Monkey See,Monkey Do)`

This loads only the "Monkey See" and "Monkey Do" Class Abilities from
`myability.lst` .

