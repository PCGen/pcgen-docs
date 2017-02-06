+++
date = "2016-08-01"
title = "SCHOOL (Data: spells.lst)"
original_url = "/list/data/spells.html#school"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "SCHOOL (Data: spells.lst)"
    parent = "spells"
+++

## Status

Updated 5.13.6

## Syntax

`SCHOOL:x|x`

## Parameters

-   x: Text (Spell School Name)



What it does
------------

This is a pipe-delimited (|) list of Schools the spell belongs to and is
used for specialist wizards to determine their favored school's bonus
spells.

.CLEAR - this CAN be chained, e.g. SCHOOL:.CLEAR|x|x|.

Example
-------

`SCHOOL:Divination`

This spell belongs to the "Divination" school.

`SCHOOL:Enchantment|Illusion`

This spell belongs to the "Enchantment" and "Illusion" schools.

`Summon Monster VII.MOD <tab> CLASSES:Channeler=7 <tab> SCHOOL:.CLEAR <tab> SCHOOL:Greater Conjuration`

For the Class Channeler of level 7 the spell Summon Monster VII is
modified, moving it from whatever schools it was in to just "Greater
Conjuration".

`SCHOOL:.CLEAR <tab> SCHOOL:Illusion`

This clears the schools list and replaces it with the "Illusion" school.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> SCHOOL:Enchantment`

Modified By: `<spell name>.MOD <tab> SCHOOL:Illusion`

Is Equivalent To: `<spell name> <tab> SCHOOL:Enchantment|Illusion`

This spell belongs to the "Enchantment" and "Illusion" schools.

