+++
date = "2016-08-01"
title = "CSKILL (Global: OTHER)"
original_url = "/list/global/other.html#cskill"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "CSKILL"
    parent = "global_other"
+++

## Status

Updated 5.13.6

## Syntax

`CSKILL:x|x`

## Parameters

-   x: Text (&lt;Skill Name&gt;)
-   x: Text (Type=&lt;Skill Type&gt;)
-   x: ALL
-   x: LIST
-   x: .CLEAR
-   x: .CLEAR.Text



What it does
------------

-   Grants the listed skills as class skills.
-   When used in a Class LST object it grants the class skills only to
    the class it is actually in.
-   When used in a Domain LST object it grants the class skills only to
    the classes that grant the domain.
-   When used anywhere else it grants the class skills to all classes
    the character possesses.

Examples
--------

`CSKILL:Listen|Spot`

The "Listen" and "Spot" skills are made class skills.

`CSKILL:Search|TYPE.Knowledge`

The "Search" and "Knowledge" type skills are made class skills.

`CSKILL:ALL`

All skills are made class skills.

`CSKILL:LIST`

Skills selected in the associated choice are made class skills. (In
Abilities and Feats)

`CLASS:Sorcerer.MOD <tab> CSKILL:.CLEAR.Scry <tab> CSKILL:Drive|TYPE.Knowledge|Perform`

Modifies the Class Sorcerer, droping the class skill "Scry" and adding
"Drive, Perform and all TYPE.Knowledge" skills.

`CLASS:Blackguard.MOD <tab> CSKILL:.CLEAR <tab> CSKILL:Concentration|TYPE.Craft|Diplomacy|Heal|Intimidate|Knowledge (Religion)|TYPE.Profession|Climb|Jump|Listen|Spot|Swim|Pilot`

Modified Class that removes all class skills in the object previously,
then adds in the specific list.

`CLASS:Blackguard.MOD <tab> CSKILL:.CLEAR.Handle Animal|.CLEAR.Ride|Heal <tab> CSKILL:Pilot`

Modified Class that removes only Handle Animal and Ride from the
original class skill list, and then adds Heal and Pilot.

