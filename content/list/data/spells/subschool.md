+++
date = "2016-08-01"
title = "SUBSCHOOL (Data: spells.lst)"
original_url = "list/data/spells.html#subschool"
categories = [ "all-tag", "spells-tag" ]
+++

## Status

Updated 5.11.13

## Syntax

`SUBSCHOOL:x|x`

## Parameters

-   x: Text (Spell Sub-School Name)



What it does
------------

This is a | (pipe) delimited list of Sub-Schools the spell belongs to
and is used for specialist wizards to determine their favored school's
bonus spells.

.CLEAR - this CAN be chained, e.g. SUBSCHOOL:.CLEAR|x|x|.

Example
-------

`SUBSCHOOL:Charm`

This spell belongs to the "Charm" sub-school.

`SUBSCHOOL:Creation|Calling`

This spell belongs to the "Creation" and "Calling" subschools.

`Wall of Force.MOD <tab> SUBSCHOOL:Force`

This spell belongs to the "Force" sub-school.

`SUBSCHOOL:.CLEAR|Charm`

This clears the subschools list and replaces with "Charm" sub-school.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> SUBSCHOOL:Creation`

Modified By: `<spell name>.MOD <tab> SUBSCHOOL:Calling`

Is Equivalent To: `<spell name> <tab> SUBSCHOOL:Creation|Calling`

This spell belongs to the "Creation" and "Calling" subschools.

