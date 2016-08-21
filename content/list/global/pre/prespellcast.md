+++
date = "2016-08-01"
title = "PRESPELLCAST (Global: PRErequisite)"
original_url = "list/global/pre.html#prespellcast"
categories = [ "all-tag", "pre-tag" ]
+++

## Status

None

## Syntax

`PRESPELLCAST:x=y`

## Parameters

-   x: MEMORIZE (Set requirements based
    on memorization).
-   x: TYPE (Set requirements based on spelltype).
-   y: Y (Yes - used with MEMORIZE).
-   y: N (No - used with MEMORIZE).
-   y: Text (A spelltype - used with TYPE).



What it does
------------

Basically each label=value pair is processed, and as the character's
classes fail to meet that pair, the class is removed from the list.
After all the label=value pairs have been processed, if the character
has any classes remaining (meaning they meet all the requirements), then
this prerequisite is met.

Examples
--------

`PRESPELLCAST:MEMORIZE=Y`

Character's class must have to memorize spells.

`PRESPELLCAST:MEMORIZE=N`

Character's class must NOT have to memorize spells.

`PRESPELLCAST:TYPE=Arcane`

Character must be able to cast arcane spells.

`PRESPELLCAST:TYPE=Divine`

Character must be able to cast divine spells.

`PRESPELLCAST:TYPE=Arcane,TYPE=Divine`

Character must be able to cast arcane/divine spells.

