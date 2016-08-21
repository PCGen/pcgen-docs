+++
date = "2016-08-01"
title = "SPELLS (Data: starting_kits.lst)"
original_url = "list/data/startingkits.html#spells"
categories = [ "all-tag", "startingkits-tag" ]
+++

## Status

None

## Syntax

`SPELLS:x|x`

## Parameters

-   x: Text (Spell name)



What it does
------------

-   Grants the character the indicated spells if they are
    legally available.
-   You can specify spells by using a pipe-delimited (|) list.

Examples
--------

`SPELLS:Detect Magic|Ghost Sound|Light|Read Magic`

Would give the <span class="lstobj">Detect Magic</span> , <span
class="lstobj">Ghost Sound</span> , <span class="lstobj">Light</span>
and <span class="lstobj">Read Magic</span> spells if the PC has free
spells.

`SPELLS:LEVEL=0`

Grants ALL 0-level spells.

