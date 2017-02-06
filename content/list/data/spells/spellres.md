+++
date = "2016-08-01"
title = "SPELLRES (Data: spells.lst)"
original_url = "/list/data/spells.html#spellres"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "SPELLRES (Data: spells.lst)"
    parent = "spells"
+++

## Status

Updated 5.11.13

## Syntax

`SPELLRES:x`

## Parameters

-   x: Text (Yes, No or free-form text)



What it does
------------

-   Indicates whether the character can try to resist the spell based on
    their Spell Resistance (SR).
-   There is NO JOINING IN THIS TOKEN... the following are NOT LEGAL (or
    you won't get what you expect): SPELLRES:For Good Creatures|Limited
    or SPELLRES:.CLEAR|No

Example
-------

`SPELLRES:Yes`

This spell is susceptible to spell resistance.

`SPELLRES:For Good Creatures`

This spell is susceptible to Good Creatures.

`SPELLRES:.CLEAR`

This clears the Spell resistance setting.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> SPELLRES:YES`

Modified By: `<spell name>.MOD <tab> SPELLRES:`

Is Equivalent To: `<spell name> <tab> SPELLRES:`



