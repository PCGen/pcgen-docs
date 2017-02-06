+++
date = "2016-08-01"
title = "DESCRIPTOR (Data: spells.lst)"
original_url = "/list/data/spells.html#descriptor"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "DESCRIPTOR (Data: spells.lst)"
    parent = "spells"
+++

## Status

Updated 5.11.13

## Syntax

`DESCRIPTOR:x|x`

## Parameters

-   x: Text (Spell type)
-   x: .CLEAR



What it does
------------

-   Reports what types the spell is and is used for specialist wizards
    to determine their favored school's bonus spells.
-   `.CLEAR` is used to clear all descriptors from a spell and can be
    followed by new descriptors to replace those cleared.

Example
-------

`DESCRIPTOR:Sonic|Acid|Evil`

This spell is of the "Sonic", "Acid" & "Evil" types.

`DESCRIPTOR:.CLEAR|Fire`

This clears the spell list and replaces it with the "Fire" type.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> DESCRIPTOR:Sonic|Acid`

Modified By: `<spell name>.MOD <tab> DESCRIPTOR:Evil`

Is Equivalent To: `<spell name> <tab> DESCRIPTOR:Sonic|Acid|Evil`

The associated spell has the descriptors "Acid", "Evil", and "Sonic".

