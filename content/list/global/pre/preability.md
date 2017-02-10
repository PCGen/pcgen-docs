+++
date = "2016-08-01"
title = "PREABILITY (Global: PRErequisite)"
original_url = "/list/global/pre.html#preability"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREABILITY"
    parent = "global_pre"
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="preability"></span>

### PREABILITY

*Require that the character has at least `N` abilities from a given
`ability_category` . A type of ability can be specified, or individual
abilities can be specified by name.*

#### Status

-   Updated 6.03.00.
    -   The syntax `PREABILITY:N,CATEGORY=ability_category,ALL`
        was deleted. (Formerly used to require `N` abilities from
        `ability_category` . Removed because it was too broad.)
    -   Refer [JIRA issue
        NEWTAG-423](http://jira.pcgen.org/browse/NEWTAG-423) - Eliminate
        use of ANY for a Category in PREABILITY.

#### Syntax

1.  `PREABILITY:N,CATEGORY=ability_category,TYPE.ability_type_1,TYPE.ability_type_2,...`

    Requires the character to have at least `N` abilities from
    `ability_category` , of the specific type(s) `ability_type_1` ,
    `ability_type_2` , and so on.

2.  `PREABILITY:N,CATEGORY=ability_category,ability_name_1,ability_name_2,...`

    Requires the character to have at least `N` abilities from a
    specific list of abilities: `ability_name_1` , `ability_name_2` ,
    and so on.

It is possible to combine the `TYPE.ability_type1` and the
`ability_name_1` syntax:

    PREABILITY:N,CATEGORY=ability_category,TYPE.ability_type_1,specific_ability_2,...  

#### Notes

-   The `CATEGORY` tag will only accept "parent" categories.

-   Square brackets around an ability name, `[ability_name_1]` , means
    that the character must **not** have `ability_name_1` .

-   Square brackets around an ability type, `[TYPE.ability_type_1]` ,
    means that the character must **not** have any ability of the type
    `ability_type_1` .

#### Examples

-   Examples using specifically named abilities

    -   `PREABILITY:1,CATEGORY=Feat,Dodge`

        Requires the `Dodge` feat. (Prerequisite for [d20 SRD
        Mobility](http://www.d20srd.org/srd/feats.htm#mobility) .)

    -   `PREABILITY:2,CATEGORY=Feat,Dodge,Mobility`

        Requires two of the `Dodge` and `Mobility` feats, i.e. both
        are required. (Prerequisite for [d20 SRD Spring
        Attack](http://www.d20srd.org/srd/feats.htm#springAttack) .)

    -   `PREABILITY:2,CATEGORY=Feat,Improved Disarm,Improved Feint,Improved Trip`

        Requires any two of the three feats specified.

-   Examples using ability types

    -   `PREABILITY:1,Category=Feat,TYPE.SpellFocus`

        Requires at least one `SpellFocus` type feat.

    -   `PREABILITY:3,Category=Feat,TYPE.Metamagic`

        Requires at least three `Metamagic` type feats.

-   Examples of excluding abilities

    -   `PREABILITY:1,Category=SpecialQuality,[Night Vision]`

        Requires that the creature does **not** have the `Night Vision`
        special quality.

        Note that the `!` syntax could also be used, i.e.

        `!PREABILITY:1,Category=SpecialQuality,Night Vision` .

    -   `PREABILITY:1,CATEGORY=Feat,Power Attack,[Weapon Finesse]`

        Requires that the creature has the `Power Attack` feat, and does
        **not** have the `Weapon Finesse` feat.



