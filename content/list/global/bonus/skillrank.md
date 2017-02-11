+++
date = "2016-08-01"
title = "SKILLRANK (Global: BONUS)"
original_url = "/list/global/bonus.html#skillrank"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "SKILLRANK"
    parent = "global_bonus"
    identifier = "global_bonus_SKILLRANK"
+++

## Status

Updated 5.7.14

## Syntax

`BONUS:SKILLRANK|x|y`

## Parameters

-   x: Text (Skill Name)
-   x: TYPE=Text (Skill type)
-   y: Number, variable or formula (Number to add to
    skill level)



What it Does
------------

Adds to skill ranks (Maximum ranks still apply).

Example
-------

`BONUS:SKILLRANK|Bluff,Listen|2`

Adds two to "Bluff" & "Listen" skills.

`BONUS:SKILLRANK|TYPE=Strength|2`

Adds two to Strength type skills.

`BONUS:SKILLRANK|Speak Language,Decipher Script,Innuendo|2|TYPE=Insight`

Adds two to three skills for insight purposes.

