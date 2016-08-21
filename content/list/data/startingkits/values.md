+++
date = "2016-08-01"
title = "VALUES (Data: starting_kits.lst)"
original_url = "list/data/startingkits.html#values"
categories = [ "all-tag", "startingkits-tag" ]
+++

## Status

None

## Syntax

`VALUES:x|y,z|x|y.z`

## Parameters

-   x: EQMOD:Text (Eqmod key)
-   x: LOOKUP Tag (See [LOOKUP
    Tag](/list/data/startingkits/lookup.html) docs)
-   y: Number (Lower selection range)
-   z: Number (Upper selection range)



What it does
------------

Defines the {"value",selection range} pairs for the associated
[TABLE](/list/data/startingkits/table.html) .

Example
-------

> `VALUES:EQMOD:BANE_M|1,10|EQMOD:DEFEND|11,17|EQMOD:FLM_M|18,27|EQMOD:FROST_M|28,37| EQMOD:SHOCK_M|38,47|EQMOD:GHOST_M|48,67|EQMOD:KIFOC|68,71|EQMOD:MERC_M|72,75| EQMOD:MI_CLE|76,82|EQMOD:SPL_STR|83,87|EQMOD:THROW|88,91|EQMOD:THNDR_M|92,95| EQMOD:VICIOU|96,100`

This table consists of the following eqmods, granted by random
determination of 1d100, <span class="lstobj">BANE\_M</span> on a 1-10,
<span class="lstobj">DEFEND</span> on an 11-17, <span
class="lstobj">FLM\_M</span> on a 18-27, <span
class="lstobj">FROST\_M</span> on a 28-37, <span
class="lstobj">SHOCK\_M</span> on a 38-47, <span
class="lstobj">GHOST\_M</span> on a 48-67, <span
class="lstobj">KIFOC</span> on a 68-71, <span
class="lstobj">MERC\_M</span> on a 72-75, <span
class="lstobj">MI\_CLE</span> on a76-82 <span
class="lstobj">SPL\_STR</span> on a 83-87, <span
class="lstobj">THROW</span> on a 88-91, <span
class="lstobj">THNDR\_M</span> on a 92-95, or <span
class="lstobj">VICIOU</span> on a 96-100.

Where it is Used
----------------

TABLE lines

