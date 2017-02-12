+++
date = "2016-08-01"
title = "Game Mode: sizeAdjustment.lst"
original_url = "/list/system/sizeadjustment.html"

[menu.main]
    identifier = "system_sizeadjustment"
    name = "sizeAdjustment.lst"
    parent = "gamemode"
    
+++
The `sizeAdjustment.lst` is a part of the "game mode".

`sizeAdjustment.lst` defines:

-   what size categories exist in the game mode, such as 'Small',
    'Medium', and 'Large'.
-   what bonuses apply to each size category; i.e. small creatures
    having better Hide checks, or big creatures being able to carry
    more weight.
-   what penalties apply to each size category; i.e. small creatures
    having a reduced carrying capacity, or big creatures having to pay
    more for weapons and armour.

The `sizeAdjustment.lst` files can be found in the
`system/gameModes/<game_mode_name>/` directory for each game mode.

Structure of the `sizeAdjustment.lst` file
------------------------------------------

Each creature size is identified by a `SIZENAME` .

Tokens are added to the `SIZENAME` to indicate the in-game effects of
the creature's size. The `SIZENUM` token is mandatory; all others are
optional.

A typical size definition, from
`system/gameModes/35e/sizeAdjustment.lst` , looks like:

    SIZENAME:S
      →  ABB:S
      →  DISPLAYNAME:Small
      →  BONUS:ITEMCOST|TYPE=Ammunition,TYPE=Armor,TYPE=Shield,TYPE=Weapon|1
    SIZENAME:S
      →  BONUS:ITEMWEIGHT|TYPE=Ammunition,TYPE=Armor,TYPE=Shield,TYPE=Weapon|0.5
      →  BONUS:ITEMWEIGHT|TYPE=Goods|0.25
    SIZENAME:S
      →  BONUS:ACVALUE|TYPE.Armor,TYPE.Shield|1
      →  BONUS:COMBAT|AC|1|TYPE=Size
      →  BONUS:COMBAT|TOHIT|1|TYPE=SIZE
      →  BONUS:COMBAT|TOHIT.GRAPPLE|-5|TYPE=Size
    SIZENAME:S
      →  BONUS:ITEMCAPACITY|TYPE=Goods|0.25
    SIZENAME:S
      →  BONUS:SKILL|Hide|4|TYPE=SIZE
    SIZENAME:S
      →  BONUS:LOADMULT|TYPE=SIZE|0.25|PRELEGSGTEQ:4
    SIZENAME:S
      →  BONUS:STAT|STR|2|PREBASESIZELT:Tiny|PREVAREQ:BypassSizeMods,0
      →  BONUS:STAT|STR|4|PREBASESIZELT:Small|PREVAREQ:BypassSizeMods,0
    SIZENAME:S
      →  BONUS:STAT|DEX|-2|PREBASESIZEEQ:Fine|PREVAREQ:BypassSizeMods,0
      →  BONUS:STAT|DEX|-2|PREBASESIZELT:Tiny|PREVAREQ:BypassSizeMods,0
      →  BONUS:STAT|DEX|-2|PREBASESIZELT:Small|PREVAREQ:BypassSizeMods,0
    SIZENAME:S
      →  SIZENUM:040

Tags
----

SIZENAME lines

-   [ABB](#abb) (abbreviation) - optional
-   [ISDEFAULTSIZE](#isdefaultsize) - optional
-   [SIZENAME](#sizename) - mandatory - each line must begin
    with SIZENAME.
-   [SIZENUM](#sizenum) - mandatory

BONUS tags specific to `sizeAdjustment.lst`

-   [BONUSACVALUE](#bonusacvalue)
-   [BONUSITEMCAPACITY](#bonusitemcapacity)
-   [BONUSITEMCOST](#bonusitemcost)
-   [BONUSITEMWEIGHT](#bonusitemweight)
-   [BONUSLOADMULT](#bonusloadmult)

All global `BONUS` tags may be used in `sizeAdjustment.lst`. Some useful
tags include:

-   `BONUS:COMBAT|AC|1|TYPE=Size`- grant a +1 size AC bonus due to size.
-   `BONUS:COMBAT|TOHIT|1|Type=Size` - grant a +1 attack bonus due
    to size.
-   `BONUS:COMBAT|TOHIT.GRAPPLE|5|Type=Size` - grant a bonus on Grapple
    checks due to large size.
-   `BONUS:SKILL|Hide|4|TYPE=Size` - grant a bonus on Hide checks due to
    small size.

------------------------------------------------------------------------

