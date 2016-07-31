+++
date = "2016-08-01"
title = "Game Mode: equipmentslots.lst"
original_url = "/list/system/gamemode-equipmentslots.html"

[menu.main]
    identifier = "system_gamemode-equipmentslots"
    name = "Game Mode: equipmentslots.lst"
    parent = "system"
    
+++
The equipmentslots.lst sets the name of locations on the character to
which specific equipment types can be equipped as well as the number of
such items which can be equipped. Equipment which do not have one of the
types specified in this file can be equipped to the character without
taking up a slot an unlimited number of times.

------------------------------------------------------------------------

------------------------------------------------------------------------

**Examples:**

`EQSLOT:Hand CONTAINS:Glove=1 NUMBER:HANDS`

This defines a Hand slot, of which there are 2 each of which can hold 1
Glove.

`EQSLOT:Fingers CONTAINS:Ring=2 NUMBER:TORSO`

This defines a Fingers slot which can hold 2 Rings. The number of slots
is defined using the TORSO type because a character can only wear 2
rings at any one time regardless of the number of hands the character
might have. The TORSO type is useful if you need the slot number to
remain static, many creatures have non standard numbers of arms, legs,
heads etc. but all creatures have only one TORSO.

`EQSLOT:Skin CONTAINS:PsionicTattoo=20 NUMBER:TORSO`

This defines a Skin slot which can hold 20 items of TYPE:PsionicTattoo.

`EQSLOT:Body CONTAINS:Armor,Robe=1 NUMBER:TORSO`

This defines a Body slot which can hold 1 item of type Armor or Robe.

