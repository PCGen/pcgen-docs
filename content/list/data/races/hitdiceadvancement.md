+++
date = "2016-08-01"
title = "HITDICEADVANCEMENT (Data: races.lst)"
original_url = "/list/data/races.html#hitdiceadvancement"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "HITDICEADVANCEMENT"
    parent = "data_races"
+++

## Status

None

## Syntax

`HITDICEADVANCEMENT:x,x`

## Parameters

-   x: Number (Hit Dice)



What it does
------------

-   The last number in the comma delimited list is the highest HD the
    creature can advance to, through HD advancement. Unlimited HD
    advancement is indicated by using an asterisk (\*) in place of the
    final number.
-   All the numbers preceding the last number each indicate the highest
    number of HD the creature can have before before its size increases
    by one category.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `HITDICEADVANCMENT` tag, the data included in a new
    `HITDICEADVACEMENT` tag will overwrite the existing tag data.

Examples
--------

`HITDICEADVANCEMENT:4,6,8`

Race starts out as Tiny, with 4 Hit Dice. 5-6 it is Small, 7+ it is
Medium. 8 Hit Dice is the maximum it can ever raise to.

`HITDICEADVANCEMENT:4,16,32,*`

Assassin Vine: starts out as Large, with 4 HD. 5-16 it is Huge, 17-32 it
is Gargantuan, 33+ it is Colossal. There is no limit to the creature's
hit dice.

`HITDICEADVANCEMENT:4,6,*`

Race starts out as Tiny, with 4 Hit Dice. 5-6 it is Small, 7+ it is
Medium. There is no limit to the creature's hit dice.

**.MOD Example:**

Initial Race: `<race name> <tab> HITDICEADVANCEMENT:4,6,8`

Modified By: `<race name>.MOD <tab> HITDICEADVANCEMENT:4,6,*`

Is Equivalent To: `<race name> <tab> HITDICEADVANCEMENT:4,6,*`

Race starts out as Tiny, with 4 Hit Dice. 5-6 it is Small, 7+ it is
Medium. The race no longer has a limit to the creature's hit dice.

