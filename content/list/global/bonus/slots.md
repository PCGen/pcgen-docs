+++
date = "2016-08-01"
title = "SLOTS (Global: BONUS)"
original_url = "/list/global/bonus.html#slots"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "SLOTS"
    parent = "global_bonus"
    identifier = "global_bonus_SLOTS"
+++

## Status

Updated 5.7.3

## Syntax

`BONUS:SLOTS|x|y`

## Parameters

-   x: Text (Slot type)
-   x: LIST (When used in conjunction with CHOOSE)
-   y: Number, variable or formula (Number of
    item slots)



What it Does
------------

-   Adds to the number of items usable in the defined slot.
-   These slots are defined in the equipmentslots.lst file for
    each gameMode.
-   Slot Types defined in most gameModes are:
    -   AMULET
    -   ARMOR
    -   BELT
    -   BOOT
    -   BRACER
    -   CAPE
    -   CLOTHING
    -   EYEGEAR
    -   GLOVE
    -   HEADGEAR
    -   LEGWEAR
    -   PSIONICTATTOO (in the 3.0 and 3.5 gameModes)
    -   RING
    -   ROBE
    -   SHIELD
    -   SHIRT
    -   TATTOO (in the Modern gameMode)
    -   TRANSPORTATION (in the Modern gameMode)
    -   VEHICLE (in the Spycraft gameMode)
    -   WEAPON

Example
-------

`BONUS:SLOTS|RING|1`

Adds one ring slot to character.

`BONUS:SLOTS|LIST|1 <tab> CHOOSE:STRING|Armor|Shield|Bracer`

Adds one slot chosen from Armor, Shield or Bracer to the character.

