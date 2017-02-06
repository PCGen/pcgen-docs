+++
date = "2016-08-01"
title = "DOMAINS (Data: spells.lst)"
original_url = "/list/data/spells.html#domains"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "DOMAINS (Data: spells.lst)"
    parent = "spells"
+++

## Status

Updated 5.11.11

## Syntax

`DOMAINS:x,x=y|x,x=y`

## Parameters

-   x: Text (Domain name)
-   x: .CLEARALL
-   y: Number (Spell level)



What it does
------------

-   This indicates that this spell is the indicated level for the
    named domain.
-   `.CLEARALL` will clear all classes or class/level pairs from the
    `CLASSES` tag.
-   This tag can now be qualified with `PRExxx` statements. Please note
    that you must enclose the `PRExxx` statement with \[ \] instead of
    the usual Pipe delineation.

Examples
--------

`DOMAINS:Charm=2|Beauty=3`

Indicates that this is a 2nd level spell for the Charm domain, and 3rd
level for the Beauty domain.

`DOMAINS:Fire=3|Magic=4[PREALIGN:2,5,8]`

Indicates that this is a 3rd level spell for the Fire domain, and 4th
level for the Magic domain, but is only available to evil characters.

`DOMAINS:Charm=2|Beauty=3[PRECLASS:Supermodel=1]`

Indicates that this is a 2nd level spell for the Charm domain, and 3rd
level for the Beauty domain, but will only be added to the spell list of
a character with a level of the Supermodel prestige class.

`Binding.MOD <tab> DOMAINS:Fate=8`

Indicates that this is an 8th level spell for the Fate domain.

**Deprecated Syntax:**

`DOMAINS:.CLEAR` replaced by `DOMAINS:.CLEARALL.`

This is done due to the past side-effects between the `CLASSES` and
`DOMAINS` tags. Note that any single `.CLEAR` is equivalent to both
`.CLEARALL` tags due to this old interaction.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> DOMAINS:Charm=2`

Modified By: `<spell name>.MOD <tab> DOMAINS:Beauty=3`

Is Equivalent To: `<spell name> <tab> DOMAINS:Charm=2|Beauty=3`

The associated spell is a 2nd level spell for the Charm domain and 3rd
level for the Beauty domain.

