+++
date = "2016-08-01"
title = "FEAT (Data: races.lst)"
original_url = "list/data/races.html#feat"
categories = [ "all-tag", "races-tag" ]
+++

## Status

Updated 5.17.4

## Syntax

`FEAT:x|x`

## Parameters

-   x: Text (Feat name)



<span id="feat"></span>

**Status:**

-   6.05.04 (July 2015): JIRA
    [NEWTAG-477](http://jira.pcgen.org/browse/NEWTAG-477) / Github [PR
    \#380](https://github.com/PCGen/pcgen/pull/380)
    -   The `FEAT` tag is deprecated. Use
        [`ABILITY`](/list/global/other/ability.html) instead.
    -   All `FEAT` tags have been **deprecated** and replaced by the
        `ABILITY` system, which is more general. The `ABILITY` system
        can model feats, racial features, class features, traits, flaws,
        temporary bonuses, and so on, all using a common format.

What it does
------------

-   This is a pipe-delimited (|) list of feats granted to a Race (also
    known as "bonus feats").
-   The hyphen (-) is used only in the `OUTPUTNAME` of feats and should
    NOT be used in the feat list for this tag. (See example below.)
-   When including a feat with an internal chooser, subchoices can be
    handled one of two ways.
-   -   Subchoices must be specified within the tag. (e.g. Weapon Focus
        (Longsword)).\
         or
    -   Used in conjunction with the `CHOOSE` tag, `%LIST` can be used
        with this tag to provide the required choice.
-   When modifying a race, with the `.MOD` tag, given an existing `FEAT`
    tag, the data included in a new `FEAT` tag will overwrite the
    existing tag data.

Example
-------

`FEAT:Blind Fight|Alertness`

Race gets "Blind-Fight" and "Alertness" as bonus feats.

`CHOOSE:WEAPONPROFS|LIST <tab> FEAT:Weapon Focus (%LIST)`

The feat "Weapon Focus" is granted as an automatic feat with the weapon
chosen with the `CHOOSE` tag.

**.MOD Example:**

Initial Race: `Darkling <tab> FEAT:Blind Fight|Alertness`

Modified By: `Darkling.MOD <tab> FEAT:Blind Fight|Combat Reflexes`

Is Equivalent To: `Darkling <tab> FEAT:Blind Fight|Combat Reflexes`

Race gets the "Blind-Fight" and "Combat Reflexes" feats as bonus feats.

