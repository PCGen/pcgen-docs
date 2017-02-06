+++
date = "2016-08-01"
title = "ROLE (Data: classes.lst)"
original_url = "/list/data/classes.html#role"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "ROLE (Data: classes.lst)"
    parent = "classes"
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

Specifies the monster role or roles associated with a character class.
Used to determine CR for creatures with both racial hit dice and class
levels.

Example
-------

`ROLE:Skill`

Character levels in this class are key levels for CR calculation
purposes for creatures with the Skill role.

`ROLE:Combat.Skill`

Character levels in this class are key levels for CR calculation
purposes for creatures with either the Combat role or the Skill role.

