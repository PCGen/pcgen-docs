+++
date = "2016-08-01"
title = "SPROP (Data: equipment.lst)"
original_url = "list/data/equipment.html#sprop"
categories = [ "all-tag", "equipment-tag" ]
+++

## Status

None

## Syntax

`SPROP:x`

## Parameters

-   x: Text (Special property)



<span id="sprop"></span> \*\*\* Updated 5.7.1

What it does
------------

-   The special property is text that will appear on output sheets under
    the equipment it is assigned to.
-   Variable substitution can be used in the same manner as the
    [SA](/list/global/other/sab.html) tag
-   The "%" symbol will fill in a number from a variable listed after a
    "|" (pipe).
-   This can be done numerous times, with each successive "%" relating
    to the next variable listed after another "|" (pipe).
-   Each variable needs to be defined (via the global
    [DEFINE](/list/global/define.html) tag.)
-   SPROP tags can be qualified with
    [PRExxx](/list/global/pre.html) tags. SPROP tags qualified with
    PRExxx tags will not display unless the character meets
    the prerequisites.
-   Variable substitution and PRExxx qualifying can be combined in one
    SPROP tag.

Examples
--------

`SPROP:Shines with an inner light`

Output sheet reads "Shines with an inner light" under the item.

`SPROP:Squash code bugs % times per day|TL`

For a 5th level character the output sheet would read "Squash code bugs
5 times per day" under the item.

`SPROP:+2 against undead|PRECLASS:1,Paladin=1`

Outputs the text if the character has at least 1 level of Paladin.

`SPROP:+% vs. code bugs|ColaIntake|PRESKILL:1,Programming=10`

If the character has the Programming skill of at least 10 and the
variable "ColaIntake" is defined as equal to 4 then the output sheet
reads "+4 vs. code bugs".

`SPROP:+1 luck bonus to saves vs. %|%CHOICE <tab> CHOOSE:Abjuration|Conjuration|          Divination|Evocation|Necromancy|Enchantment|Transmutation|Universal`

Allows for the selection of the type of luck bonus and inserts it in the
%CHOICE.

