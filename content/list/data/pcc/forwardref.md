+++
date = "2016-08-01"
title = "FORWARDREF (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#forwardref"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "FORWARDREF (Data: campaign.pcc)"
    parent = "pcc"
+++

## Status

New 5.15.10

## Syntax

`FORWARDREF:x|y,y`

## Parameters

-   x: ABILITY=Text (Ability category)
-   x: ARMORPROF
-   x: CLASS
-   x: DEITY
-   x: DOMAIN
-   x: EQMOD
-   x: EQUIPMENT
-   x: FEAT
-   x: LANGUAGE
-   x: RACE
-   x: SHIELDPROF
-   x: SKILL
-   x: SPELL
-   x: TEMPLATE
-   x: WEAPONPROF
-   x: CLASSSKILLLIST
-   x: CLASSSPELLLIST
-   x: DOMAINSPELLLIST
-   y: Text (Object name)



What it does
------------

-   This tag will suppress the "Unconstructed Object" error reports for
    the listed LST objects from appearing within the user interface.
-   This is useful during source loading when objects are referenced
    that will not be loaded with the given source.
-   The FORWARDREF only applies if the PCC is directly loaded. Since the
    FORWARDREF tag's purpose is to hide intentional omissions it always
    needs to be intentionally placed.

Example
-------

`FORWARDREF:CLASSSPELLLIST|Assassin,Black Guard`

"Unconstructed Object" errors for the "'Assassin" and "Black Guard"
spell lists will be suppressed during source loading.

