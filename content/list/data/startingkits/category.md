+++
date = "2016-08-01"
title = "CATEGORY (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#category"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "CATEGORY"
    parent = "data_startingkits"
+++

## Status

New 5.11.11

## Syntax

`ABILITY:CATEGORY=x|y|y`

## Parameters

-   x: Text (Ability Category Pool)
-   y: Text (Ability name)
-   y: TYPE=Text (Ability TYPE)



What it does
------------

-   Presents a pipe (|) delimited list of abilities from which the user
    selects one to be granted.
-   The ability granted will be assigned to the ability category
    pool specified.

NOTE: While multiple categories can be defined currently, this syntax is
strongly discouraged as the results may be unpredictable.

Example
-------

`ABILITY:CATEGORY=FEAT|Weapon Focus (Greataxe)`

Would grant the "Greataxe Weapon Focus" feat.

`ABILITY:CATEGORY=Fighter Feat|Dodge PRESTAT:1,DEX=13`

Would grant "Dodge" if the character has a Dexterity of at least 13.

`ABILITY:CATEGORY=Fighter Feat|Dodge|Improved Initiative`

Would grant the choice of Dodge or Improved Initiative.

`ABILITY:CATEGORY=Wizard Feat|TYPE=ItemCreation`

Would grant the choice of an ItemCreation type feat.

`ABILITY:CATEGORY=Salient Divine Ability|Alter Size`

Would grant the Alter Size salient divine ability.

`ABILITY:CATEGORY=Salient Divine Ability|Alter Size|Divine Blessing`

Would grant a choice of the Alter Size and Divine Blessing salient
divine abilities.

`ABILITY:CATEGORY=Salient Divine Ability|Alter Form<tab>FREE:YES`

Would grant the Alter Form salient divine ability without charging the
salient divine ability pool.

