+++
date = "2016-08-01"
title = "SPROP (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#sprop"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "SPROP"
    parent = "data_equipmentmodifiers"
+++

## Status

None

## Syntax

`SPROP:x`

## Parameters

-   x: Text (Special property)



<span id="sprop"></span> \*\*\* Updated 5.7.7

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
-   Support has been added for %CHOICE substitution so that the SPROP
    will pick up and display the selection from the CHOOSE.

Examples
--------

`SPROP:Shines with an inner light`

Output sheet reads "Shines with an inner light" under the item.

`SPROP:Squash code bugs % times per day|TL`

For a 5th level character the output sheet would read "Squash code bugs
5 times per day" under the item.

`SPROP:+2 against undead|PRECLASS:Paladin=1`

Outputs the text if the character has at least 1 level of Paladin.

`SPROP:+% vs. code bugs|ColaIntake|PRESKILL:1,Programming=10`

If the character has the Programming skill of at least 10 and the
variable "ColaIntake" is defined as equal to 4 then the output sheet
reads "+4 vs. code bugs".

`SPROP:+2 against %CHOICE`

If one of the choices offered by the EQMOD were "Dragons" the SPROP
might read "+2 against Dragons".

`SPROP:Unreliable (%CHOICE) <tab> CHOOSE:5%|10%|15%|20%|25%|30%|35%|40%|45%|50%|55%|60%|65%|70%|75%|80%|85%|90%|95%|100%`

Chooser to select the level of unreliablty.

