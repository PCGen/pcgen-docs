+++
date = "2016-08-01"
title = "COMPS (Data: spells.lst)"
original_url = "/list/data/spells.html#comps"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "COMPS (Data: spells.lst)"
    parent = "spells"
+++

## Status

Updated 5.11.12

## Syntax

`COMPS:x`

## Parameters

-   x: Text (V, S, M, DF)



What it does
------------

Lists the types of spell components required for this spells (Verbal,
Somatic, etc).

Example
-------

`COMPS:V S`

This spell has "Verbal" and "Somatic" components.

`SpellFoo <tab> COMPS:.CLEAR <tab> COMPS:V <tab> COMPS:S`

The spell SpellFoo has its COMPS cleared and "Verbal" and "Somatic"
components added.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> COMPS:V S`

Modified By: `<spell name>.MOD <tab> COMPS:M`

Is Equivalent To: `<spell name> <tab> COMPS:V S|M`

The associated spell's spell components include "Verbal", "Somatic", and
"Material" components.

