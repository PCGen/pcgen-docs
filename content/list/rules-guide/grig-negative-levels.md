+++
date = "2016-08-01"
title = "Equipment Granting Negative Levels"
original_url = "/list/rules-guide/grig-negative-levels.html"

[menu.main]
    identifier = "rules-guide_grig-negative-levels"
    name = "Equipment Granting Negative Levels"
    parent = "rules-guide"
    
+++
**Rule Description:** The granting of "Negative Levels" to characters by
equipment.

**PCGen Version:** 5.8.x to current.

**Gamemode/Dataset:** 35e/RSRD Complete

**File(s) Covered:** equipment.lst and feat.lst

**Tags Used:**

[TYPE](/list/data/feats.html#type) ,
[VISIBLE](/list/data/feats/visible.html) ,
[SA](/list/global/other/sab.html) , [DEFINE](/list/global/define.html) ,
[BONUS:CHECKS](/list/global/bonus/checks.html) ,
[BONUS:COMBAT](/list/global/bonus/combat.html) ,
[BONUS:SKILL](/list/global/bonus/skill.html)[VFEAT](/list/global/other/vfeat.html)
,
[BONUS:VAR](/list/global/bonus/var.html)[PREALIGN](/list/global/pre/prealign.html)

NOTE: In this section we will discuss only those LST tags specific to
this implementation, and how they are used to implement the subject
rule. For more general information on the associated tags, please visit
the [LST File Tag Index](/navlistindex.html) section of the PCGen
Documentation.

------------------------------------------------------------------------

Implementation Discussion
-------------------------

Implementing "Negative Levels" for equipment that is "equiped" requires
two specific LST entries. These are a <span class="lstfile"> feat.lst
</span> entry titled "Negative Levels" and a specifc application of this
feat in the appropriate item entry in the <span class="lstfile">
equipment.lst </span> file. Fortunately, this ability has already been
implemented in the RSRD, SRD, and the MSRD, as well as several other
distributed datasets, so incorporating the rule into a Homebrew dataset
is fairly simple, as long as the homebrew rules are based upon one of
the datasets that have the rule already implemented. The steps to follow
in this case are as follows:

1.  Make sure the hidden feat "Negative Levels" is loaded when you load
    your datasets on the "Source Materials" tab.
2.  When creating the <span class="lstfile"> equipment.lst </span> entry
    for the piece of equipment in question, include the appropriate tag
    to grant the "Negative Levels" feat. This is usually done with the
    `VFEAT:Negative Levels` tag. See the
    [VFEAT](/list/rules-guide/grig-negative-levels.html#vfeat) tag below
    for more information on how it works.
3.  Add a `BONUS:VAR|NegLevels|#|PRExxx` tag in the <span
    class="lstfile"> equipment.lst </span> file, replacing the "\#" with
    the number of negative levels being lost. See the
    [BONUS:VAR](/list/rules-guide/grig-negative-levels.html#bonusvar)
    tag below for more information on how it works.
4.  The PRExxx tag used in the `BONUS:VAR` tag above is used to define
    what prerequirements must be met before applying the
    negative levels. The most common prerequirement is the alignment of
    the character, in which case the `PREALIGN|x,x` tag would be used.
    See the
    [PREALIGN](/list/rules-guide/grig-negative-levels.html#prealign) tag
    description below for more information on how it works.

If you are not using a dataset that already implements the "Negative
Levels" rule you will follow the same steps above except that you will
need to create the feat of the same name in the <span class="lstfile">
feat.lst </span> file. We discuss tags used in this feat entry, as well
as the tags used to apply the rule within an <span class="lstfile">
equipment.lst </span> entry, in more detail below. To help you better
understand these entries, we will be using the <span class="lstobj">
Demon Armor </span> entry from the RSRD.

Finally, for assistance in understanding how to read this page you may
review the [Rules Style
Guide](/list/rules-guide/reading-instructions.html) .

------------------------------------------------------------------------

### Feat File

The specific feat entry in the <span class="lstfile"> feat.lst </span>
file is called <span class="lstobj"> Negative Levels </span> and will
provide all of the penalties, or enhancments, required when a negative
level is applied. The penalties, in this case, include a reduction to
"Fortitude", "Reflex", and "Will" checks, the reduction of the
characters "To Hit" bonus, and a reduction in skill bonuses across the
board. The tags used are explained below:

> > **Tag Used:**
> > `SA:% negative level(s) (-% effective level(s) and loses access to % spell(s) from the highest spell level castable)|NegLevels|NegLevels|NegLevels`
>
> **What it does:**
>
> -   This grants the character negative levels as a <span
>     class="lstobj"> Special Ability (SA) </span> that will get listed
>     together with all other special abilities the character has
>     been granted.
> -   The "%" tag will fill in a number from a variable listed after the
>     pipe (|) with each successive "%" being replaced by the next
>     variable listed after subsequent pipes.
> -   The variable <span class="lstvar"> NegLevels </span> is defined by
>     the `DEFINE` tag within this feat.
> -   The <span class="lstobj"> SA </span> will NOT be displayed if the
>     last variable or formula equals "0".

> **Tag Used:** `DEFINE:NegLevels|0`
>
> **What it does:** Creates the <span class="lstvar"> NegLevels </span>
> variable and initializes it to a value of zero.

> **Tag Used:** `BONUS:CHECKS|Fortitude,Reflex,Will|-1*(NegLevels)`
>
> **What it does:** Subracts the number of negative levels granted from
> the "Fortitude". "Reflex", and "Will" saving throws.

> **Tag Used:** `BONUS:COMBAT|TOHIT|-1*(NegLevels)`
>
> **What it does:** Subtracts the number of negative leves granted from
> the primary attack bonus.

> > **Tag Used:**
> > `BONUS:SKILL|TYPE=Strength,TYPE=Dexterity,TYPE=Constitution, TYPE=Intelligence,TYPE=Wisdom,TYPE=Charisma|-1*(NegLevels)`
>
> **What it does:** Subtracts the number of negative levels granted from
> all skills.

------------------------------------------------------------------------

### Equipment File

In the <span class="lstfile"> equip.lst </span> file we must first apply
the new feat <span class="lstobj"> Negative Levels </span> by using the
`VFEAT` tag in the specific equipment entry and then we must apply the
specific number of negative levels through the `BONUS:VAR` tag.

> <span id="vfeat"></span> **Tag Used:** `VFEAT:Negative Levels`
>
> **What it does:** Grants the <span class="lstobj"> Negative Levels
> </span> feat and initializes the <span class="lstvar"> NegLevels
> </span> variable. (see Feat File Entry above.)

> <span id="bonusvar"></span> **Tag Used:**
> `BONUS:VAR|NegLevels|x|PREALIGN:LG,LN,NG,TN,CG,CN`
>
> **Variables Used (x):** Number (number of negative levels applied.)
>
> **What it does:**
>
> -   <span class="lstvar"> NegLevels </span> is a variable defined in
>     the <span class="lstobj"> Negative Levels </span> feat
>     specifically for this purpose.
> -   Use "2", not "-2", to bestow two negative levels.
> -   If the <span class="lstvar"> NegLevels </span> variable is "0" (no
>     negative levels applied), then nothing will show, and it will be
>     as if the Negative Levels feat was not granted.
> -   PRExxx tags can be used to set requirements for the applicaton of
>     the <span class="lstvar"> NegLevels </span> bonus. The most common
>     PRExxx tag used is the PREALIGN tag, which sets an "Alignment"
>     restriction on the associated bonus.
>
> **Example:** - <span class="lstobj"> Demon Armor </span> (RSRD)
>
> `BONUS:VAR|NegLevels|1|PREALIGN:LG,LN,NG,TN,CG,CN`
>
> Demon Armor bestows one negative level to all non-evil characters.

> <span id="prealign"></span> **Tag Used:** `PREALIGN:LG,LN,NG,TN,CG,CN`
>
> **What it does:** Sets an "Alignment" based restriction upon when the
> associated bonus will be applied.

------------------------------------------------------------------------

### Known Issues

None

------------------------------------------------------------------------

### LST File Entry Examples

These examples come from the RSRD.

Feat File: <span class="lstobj"> Negative Levels </span> feat

> `Negative Levels`
>
> `TYPE:Special`
>
> `VISIBLE:NO`
>
> `SA:% negative level(s) (-% effective level(s) and loses access to % spell(s) from the highest spell level castable)|NegLevels|NegLevels|NegLevels`
>
> `DEFINE:NegLevels|0`
>
> `BONUS:CHECKS|Fortitude,Reflex,Will|-1*(NegLevels)`
>
> `BONUS:COMBAT|TOHIT|-1*(NegLevels)`
>
> `BONUS:SKILL|TYPE=Strength,TYPE=Dexterity,TYPE=Constitution, TYPE=Intelligence,TYPE=Wisdom,TYPE=Charisma|-1*(NegLevels)`

Equipment File: <span class="lstobj"> Demon Armor </span>

> `Demon Armor`
>
> .
>
> . (See the RSRD for full detail on this item.)
>
> .
>
> `VFEAT:Negative Levels`
>
> `BONUS:VAR|NegLevels|1|PREALIGN:LG,LN,NG,TN,CG,CN`

------------------------------------------------------------------------



