+++
date = "2016-08-01"
title = "EXCLUDE (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#exclude"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "EXCLUDE"
    parent = "data_pcc"
+++

## Status

None

## Syntax

`(EXCLUDE:y|y)`

## Parameters

-   x: Text (Ability category)
-   y: Text (LST object name)



**Tag Name:** (EXCLUDE:CATEGORY=x,y,y|x,y,y) - Special syntax for feats
and abilities

What it does
------------

-   The EXCLUDE tag and its arguments are enclosed within a pair
    of parentheses.
-   The tag will prevent the pipe-delimited list of LST objects from
    being loaded from the LST file the tag is associated with.
-   The tag will not prevent other .pcc files from loading the same
    LST file.
-   The tag will not prevent other .pcc files from loading the excluded
    LST objects from another LST file.
-   LST objects can include any of the following types: CLASS,
    COMPANIONMODS, DEITY, DOMAIN, EQUIPMENT, EQUIPMOD, FEAT, KIT,
    LANGUAGE, RACE, SKILL, SPELL, TEMPLATE, WEAPONPROF

Example
-------

`RACE:fhbrace.lst|(EXCLUDE:Fooman|Foowarf)`

This loads all the races from the `fhbrace.lst` file except for the
"Fooman" and "Foowarf" races.

`ABILITY:fhbability.lst|(EXCLUDE:CATEGORY=Class Ability,Monkey See,Monkey Do)`

This loads all the abilities from the `fhbability.lst` file except for
the "Monkey See" and "Monkey Do" Class Abilities.

