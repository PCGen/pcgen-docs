+++
date = "2016-08-01"
title = "VARIANTS (Data: spells.lst)"
original_url = "/list/data/spells.html#variants"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "VARIANTS"
    parent = "data_spells"
+++

## Status

Updated 5.11.13

## Syntax

`VARIANTS:x|x`

## Parameters

-   x: Text (Spell Variant)



What it does
------------

-   This is a | (pipe) delimited list of the names of variations of
    the spell.
-   Optional Tag. Not all spells have variants.
-   Used when creating custom magic items (such as scrolls and wands).
    User must select one of the variants when creating such an item.

.CLEAR - this CAN be chained, e.g. TAG:.CLEAR|x|x|.

Example
-------

`VARIANTS:Blast|Spell`

Names the two variations of the spell.

`VARIANTS:Acorn Grenades|Holly Berry Bombs`

Names the two variants of the spell Fire seeds.

`VARIANTS:.CLEAR`

Removes all variants of the spell.

`VARIANTS:.CLEAR|Acorn Grenades|Holly Berry Bombs`

Removes all variants of the spell Fire seeds.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> VARIANTS:Acorn Grenades`

Modified By: `<spell name>.MOD <tab> VARIANTS:Holly Berry Bombs`

Is Equivalent To:
`<spell name> <tab> VARIANTS:Acorn Grenades|Holly Berry Bombs`

Names the two variants of the spell Fire seeds.

