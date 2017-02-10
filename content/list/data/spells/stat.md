+++
date = "2016-08-01"
title = "STAT (Data: spells.lst)"
original_url = "/list/data/spells.html#stat"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "STAT"
    parent = "data_spells"
+++

## Status

None

## Syntax

`STAT:x`

## Parameters

-   x: Text (stat abbreviation)



What it does
------------

-   Used to tell PCGen what attribute/stat to use for determining bonus
    spells and maximum level the character can cast.
-   Used in conjunction with the `SPELLSTAT:SPELL` tag in the
    *\*\_class.lst* file.

Example
-------

`STAT:CHA`

When used in conjunction with the `SPELLSTAT:SPELL` tag in a class file,
a spell with this tag will use the charisma modifier to determine bonus
spells and maximum level the character can cast.

**.MOD Example (Overwriting):**

Initial Spell: `<spell name> <tab> STAT:CHA`

Modified By: `<spell name>.MOD <tab> STAT:INT`

Is Equivalent To: `<spell name> <tab> STAT:INT`

This spell will now use the intelligence modifier to determine bonus
spells and maximum level the character can cast

