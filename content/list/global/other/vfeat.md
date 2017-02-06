+++
date = "2016-08-01"
title = "VFEAT (Global: OTHER)"
original_url = "/list/global/other.html#vfeat"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "VFEAT (Global: OTHER)"
    parent = "other"
+++

## Status

Updated 5.17.4

## Syntax

`VFEAT:x|x`

## Parameters

-   x: Text (Name of feat)



<span id="vfeat"></span>

**Status:**

-   6.05.04 (July 2015): JIRA
    [NEWTAG-477](http://jira.pcgen.org/browse/NEWTAG-477) / Github [PR
    \#380](https://github.com/PCGen/pcgen/pull/380)
-   -   `VFEAT` is deprecated. Use
        [`ABILITY:FEAT|VIRTUAL|`](/list/global/other/ability.html) instead.
    -   All `FEAT` tags have been **deprecated** and replaced by the
        `ABILITY` system, which is more general. The `ABILITY` system
        can model feats, racial features, class features, traits, flaws,
        temporary bonuses, and so on, all using a common format.

What it does
------------

-   Grants any number of feats to the character as "Virtual" feats.
-   The list of feats granted are a pipe-delimited ("|") list of feats.
-   The feats are granted regardless of the prerequisites for
    those feats.
-   When including a feat with an internal chooser, subchoices can be
    handled one of two ways.
-   -   Subchoices must be specified within the tag. (e.g. Weapon Focus
        (Longsword)).\
         or
    -   Used in conjunction with the `CHOOSE` tag, `%LIST` can be used
        with this tag to provide the required choice.
-   Feats such as "Armor Proficiency (yyy)" that do not have a built-in
    chooser are a set of individual feats and therfore **WILL** have a
    space between the feat name and the opening parenthesis.
-   Feats such as "Weapon Focus" are single feats with built-in choosers
    and will **NOT** have a space between the feat name and the opening
    parenthesis, i.e. "Weapon Focus(xxx)".
-   PRExxx tags can be used to assign new prerequisites to the
    virtual feats.

**Note:** This tag **WILL NOT** activate a CHOOSER inside of a feat. You
must use [ADD:FEAT](/list/global/add/feat.html) to activate a chooser
inside of a feat being granted.

Examples
--------

`VFEAT:Simple Weapon Proficiency`

The character gains "Simple Weapon Proficiency" as a virtual feat.

`VFEAT:Alertness|Blind Fight`

The character gains "Alertness" and "Blind Fight" as virtual feats.

`VFEAT:Weapon Focus(Greatsword)`

The character gains "Weapon Focus(Greatsword)" as a virtual feat.

`CHOOSE:WEAPONPROFS|LIST <tab> VFEAT:Weapon Focus (%LIST)`

The feat "Weapon Focus" is granted as a virtual feat with the weapon
chosen with the `CHOOSE` tag.

`VFEAT:Banana Barrage|PRECLASS:1,Ninja Monkey=1`

The character gains "Banana Barrage" as a virtual feat only if they have
at least one level of "Ninja Monkey".

