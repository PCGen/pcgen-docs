+++
date = "2016-08-01"
title = "SAVEINFO (Data: spells.lst)"
original_url = "list/data/spells.html#saveinfo"
categories = [ "all-tag", "spells-tag" ]
+++

## Status

None

## Syntax

`SAVEINFO:x`

## Parameters

-   x: Text (Spell save)



What it does
------------

Reports whether or not there is a save for the spell, and if so what it
is.

Example
-------

`SAVEINFO:Will Negates`

A successful Will save will negate the spell effects.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> SAVEINFO:Will negates`

Modified By: `<spell name>.MOD <tab> SAVEINFO:Reflex for half`

Is Equivalent To:
`<spell name> <tab> SAVEINFO:Will negates|Reflex for half`

A successful Reflex save will half the spell effect and a successful
Will save negates.

