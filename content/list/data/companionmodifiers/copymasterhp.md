+++
date = "2016-08-01"
title = "COPYMASTERHP (Data: companion_mods.lst)"
original_url = "/list/data/companionmodifiers.html#copymasterhp"
categories = [ "all-tag", "companionmodifiers-tag" ]
[menu.main]
    name = "COPYMASTERHP"
    parent = "data_companionmodifiers"
    identifier = "data_companionmodifiers_COPYMASTERHP"
+++

## Status

None

## Syntax

`COPYMASTERHP:x`

## Parameters




**Variables used (x):** Number, Variable or Formula (Hit Points granted)

**Variables used (x):** MASTER

What it does
------------

-   Substitutes the follower's normal Hit Points (HP) with the
    value specified.
-   `MASTER` is a special sub-tag which passes the value of the
    Master's HP.

Example
-------

`COPYMASTERHP:MASTER/2`

Gives the creature half the master's hit points

`COPYMASTERHP:max(1,MASTER/2)`

Gives the creature half the master's hit points or 1, whichever is
higher.

Where it is Used
----------------

FOLLOWER Line

