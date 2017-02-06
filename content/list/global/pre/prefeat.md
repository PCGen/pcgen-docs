+++
date = "2016-08-01"
title = "PREFEAT (Global: PRErequisite)"
original_url = "/list/global/pre.html#prefeat"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREFEAT (Global: PRErequisite)"
    parent = "pre"
+++

## Status

None

## Syntax

`PREFEAT:x,y,z`

## Parameters

-   x: Number (Number of required feats)
-   y: CHECKMULT (Used to make the program count each
    instance of a feat separately - optional)
-   z: Text (Feat name)
-   z: \[Text\] (Name of a feat a character must
    NOT have)
-   z: TYPE=Text (Feat type)
-   z: \[TYPE=Text\] (Type of feat the character must
    NOT have)



<span id="prefeat"></span>

### PREFEAT

**Status:**

-   6.05.04 (July 2015): JIRA
    [NEWTAG-477](http://jira.pcgen.org/browse/NEWTAG-477) / Github [PR
    \#380](https://github.com/PCGen/pcgen/pull/380)
-   -   `PREFEAT` is deprecated. Use
        [`PREABILITY`](/list/global/pre/preability.html) instead.
    -   All `FEAT` tags have been **deprecated** and replaced by the
        `ABILITY` system, which is more general. The `ABILITY` system
        can model feats, racial features, class features, traits, flaws,
        temporary bonuses, and so on, all using a common format.

What it does
------------

-   Sets character feat requirements.
-   Feats with multiple instances where the instance is expressed within
    parentheses, e.g. Skill Focus or Spell Focus, there is no space
    between the name of the feat and the parentheses.
-   Use of the `(TYPE=<text>)` syntax with feats with multiple
    instances, e.g. `Weapon Focus(TYPE=Bow)` , though allowed, is only
    supported for feats with internal choosers for `DOMAIN` , `SKILL` ,
    `SPELL` , and `WEAPONPROF` types.

Examples
--------

`PREFEAT:1,Dodge,Combat Reflexes`

Character must have either "Dodge" or "Combat Reflexes".

`PREFEAT:2,CHECKMULT,Spell Focus`

Character must have "Spell Focus" for two schools.

`PREFEAT:2,CHECKMULT,Spell Focus,[Spell Focus(Enchantment)]`

Character must have "Spell Focus" for two schools, but not the
"Enchantment" school.

`PREFEAT:2,Weapon Focus(TYPE=Bow),Weapon Focus(Longsword)`

Character must have both "Weapon Focus(Longsword)" and any one "Bow"
type "Weapon Focus".

`PREFEAT:2,CHECKMULT,Weapon Focus(TYPE=Sword)`

Character must have two "Sword" type "Weapon Focus" feats.

`PREFEAT:2,Skill Focus(Spot),Skill Focus(Listen),Skill Focus(Search)`

Character must have any two of "Skill Focus(Spot)", "Skill
Focus(Listen)", or "Skill Focus(Search)".

`PREFEAT:2,TYPE=ItemCreation`

Character must have any two "ItemCreation" type feats.

`PREFEAT:1,Skill Focus(Knowledge%)`

Character must have one "Skill Focus" feat for a "Knowledge" sub-type
skill.

`Magecraft (Charismatic).MOD <tab> !PREFEAT:1,Untapped Potential`

Character must not (!) have one feat called "Untapped Potential".

