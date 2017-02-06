+++
date = "2016-08-01"
title = "DEITYWEAP (Data: deities.lst)"
original_url = "/list/data/deities.html#deityweap"
categories = [ "all-tag", "deities-tag" ]
[menu.main]
    name = "DEITYWEAP (Data: deities.lst)"
    parent = "deities"
+++

## Status

Updated 6.3.0

## Syntax

`DEITYWEAP:x|x`

## Parameters

-   x: Text (Weapon Name)
-   x: ANY
-   x: .CLEAR



What it does
------------

-   This is a | (pipe) delimited list of the deity's favored weapon(s).
    (or a choice of one of the weapons if more than one is listed).
-   ANY will produce a list of all loaded proficiencies for the
    War domain.
-   The Weapon name MUST match exactly what is listed in the weapon
    proficiencies list file.
-   Using `.CLEAR` will clear all deity weapons from the
    associated deity.

Examples
--------

`DEITYWEAP:Sword (Long)`

The deity's favored weapon is a "Long Sword".

`DEITYWEAP:Longspear|Shortspear|Halfspear`

The deity's favored weapon is either a "Longspear", "Shortspear" or
"Halfspear".

`DEITYWEAP:ANY`

The deity's favored weapon can be any weapon.

**.MOD Example (Appending):**

Initial Deity: `<deity name> <tab> DEITYWEAP:Longsword`

Modified By: `<deity name>.MOD <tab> DEITYWEAP:Scimitar`

Is Equivalent To: `<deity name> <tab> DEITYWEAP:Longsword|Scimitar`

