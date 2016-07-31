+++
date = "2016-08-01"
title = "EQMOD (Data: starting_kits.lst)"
original_url = "list/data/startingkits.html#eqmod"
categories = [ "all-tag", "startingkits-tag" ]
+++

## Status

New 5.9.2

## Syntax

`EQMOD:x|y|y.x|y|y`

## Parameters

-   x: Text, period delimited (Equipment modifier name)
-   y: Text, pipe delimited (Modifiers applied to the
    equipment modifier name)



What it does
------------

-   A period (.) delimited list of equipment modifiers.
-   Each element is a pipe (|) delimited list of strings.
-   It calls an equipment mod to be applied to the base item.
-   It will take the base item, and automatically apply the equipmod.

Example
-------

`EQMOD:Bane.Holy.Keen`

The equipment modifiers "Bane", "Holy" and "Keen" (as seen in the item
customizer in PCGen) are added to the granted equipment item.

`EQMOD:KEEN.BANE|Undead` or `EQMOD:BANE|Undead.KEEN`

Bane Undead is added to the item.

`EQMOD:ABILITYPLUS|STR+2`

Applies a +2 STR bonus to the character when using the item.

Where it is used
----------------

GEAR line

