+++
date = "2016-08-01"
title = "ROLE (Data: races.lst)"
original_url = "/list/data/races.html#role"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "ROLE (Data: races.lst)"
    parent = "races"
+++

## Status

New 6.1.2

## Syntax

`ROLE:x.x`

## Parameters

-   x: Text (a monster role as defined in the
    game mode).



What it does
------------

Specifies the monster role or roles of a creature. Used to determine CR
for creatures with both racial hit dice and class levels.

Example
-------

`ROLE:Combat`

Character levels in classes associated with the Combat role are key
levels for CR calculation purposes for this creature.

`ROLE:Combat.Skill`

Character levels in classes associated with either the Combat role or
the Skill role are key levels for CR calculation purposes for this
creature.

`ROLE:Cleric`

Cleric levels are key levels for CR calculation purposes for this
creature.

