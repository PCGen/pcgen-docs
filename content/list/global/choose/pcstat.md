+++
date = "2016-08-01"
title = "PCSTAT (Global: CHOOSE)"
original_url = "/list/global/choose.html#pcstat"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "PCSTAT (Global: CHOOSE)"
    parent = "choose"
+++

## Status

New 5.16.x

## Syntax

`CHOOSE:PCSTAT|x|x`

## Parameters

-   x: Text (Stat abbreviation)
-   x: TYPE=Text (Stat type)
-   x: !TYPE=Text (Stat type)
-   x: ALL



What it does
------------

-   This will produce a list of all stats listed or that otherwise meet
    the criteria included.
-   The stats listed, including the type, must be defined in the Game
    Mode file.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

**NOTE:** Most, if not all, game modes distributed with PCGen do not use
stat types.

Example
-------

`CHOOSE:STAT|DEX|CON`

Un-intuitively, this produces a list of all stats *except* `DEX` and
`CON` . Due to the potential for confusion, the `CHOOSE:STAT` syntax has
been replaced by the `CHOOSE:PCSTAT` syntax below.

Example Conversion to New Syntax
--------------------------------

`CHOOSE:STAT|STR|CON` becomes `CHOOSE:PCSTAT|DEX|INT|WIS|CHA`

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

