+++
date = "2016-08-01"
title = "SERVESAS (Global: OTHER)"
original_url = "list/global/other.html#servesas"
categories = [ "all-tag", "other-tag" ]
+++

## Status

New 5.13.15

## Syntax

`SERVESAS:x|y|y`

## Parameters

-   x: ABILITY=Text (Ability category including FEATS)
-   x: CLASS
-   x: RACE
-   x: SKILL
-   y: Text (Object name)



What it does
------------

Allows one object to imitate one or more objects, of the same type, to
satisfy the requirements established by PRExxx tags.

Example
-------

`Super Foo<tab>SERVESAS:ABILITY=FEAT|Endurance|Diehard`

Allows a character with the feat "Super Foo" to pass a prerequisite of
"Endurance" or "Diehard".

`Super Warrior <tab> SERVESAS:CLASS|Warrior|Barbarian`

Allows a character with class levels of "Super Warrior" to pass a
prerequisite of class "Warrior" or "Barbarian".

**Where is it Used:**

Ability, Class, Feat, Race, and Skill files.

