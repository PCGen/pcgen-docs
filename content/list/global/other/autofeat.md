+++
date = "2016-08-01"
title = "AUTOFEAT (Global: OTHER)"
original_url = "list/global/other.html#autofeat"
categories = [ "all-tag", "other-tag" ]
+++

## Status

Updated 5.17.4

## Syntax

`AUTO:FEAT|x|x`

## Parameters

-   x: Text (Feat name)



<span id="autofeat"></span>

**Status:**

-   6.05.04 (July 2015): JIRA
    [NEWTAG-477](http://jira.pcgen.org/browse/NEWTAG-477) / Github [PR
    \#380](https://github.com/PCGen/pcgen/pull/380)
-   -   `AUTO:FEAT` is deprecated. Use
        [`ABILITY:FEAT|AUTOMATIC|`](/list/global/other/ability.html) instead.
    -   All `FEAT` tags have been **deprecated** and replaced by the
        `ABILITY` system, which is more general. The `ABILITY` system
        can model feats, racial features, class features, traits, flaws,
        temporary bonuses, and so on, all using a common format.

What it does
------------

-   This is a pipe-delimited (|) list of feats that are granted to the
    character as automatic feats.
-   When including a feat with an internal chooser, subchoices can be
    handled one of two ways.
-   -   Subchoices must be specified within the tag. (e.g. Weapon Focus
        (Longsword)).\
         or
    -   Used in conjunction with the `CHOOSE` tag, `%LIST` can be used
        with this tag to provide the required choice.
-   PRExxx tags must be appended to the tag using the pipe-delimited (|)
    syntax.
-   .CLEAR may be used with this tag as part of a .MOD operation and may
    not be used during class progression. (i.e. There is no
    cross-level interaction.)

**Note:** This tag **WILL NOT** activate a CHOOSER inside of a feat. You
must use [ADD:FEAT](/list/global/add/feat.html) to activate a chooser
inside of a feat being granted.

Examples
--------

`AUTO:FEAT|Dodge|PRESTAT:1,DEX=13`

The feat "Dodge" is granted as an automatic feat if the character's
dexterity is 13 or higher.

`CHOOSE:WEAPONPROFICIENCY|LIST <tab> AUTO:FEAT|Weapon Focus (%LIST)`

The feat "Weapon Focus" is granted as an automatic feat with the weapon
chosen with the `CHOOSE` tag.

`AUTO:FEAT|.CLEAR.Dodge <tab> AUTO:FEAT|Alertness`

The feat "Dodge" is cleared and the feat "Alertness" is granted as an
automatic feat.

