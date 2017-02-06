+++
date = "2016-08-01"
title = "REMOVE (Global: OTHER)"
original_url = "/list/global/other.html#remove"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "REMOVE (Global: OTHER)"
    parent = "other"
+++

## Status

New 5.11.13

## Syntax

`REMOVE:FEAT|x|y,y`

## Parameters

-   x: Number (Number of feats, Optional)
-   x: ALL
-   y: Text (Name of feat)
-   y: TYPE.Text (Feat type)
-   y: CLASS.Text (Feat class type)
-   y: CHOICE (Presents a chooser dialog box)



<span id="remove"></span>

**Status:**

-   6.05.04 (July 2015): JIRA
    [NEWTAG-477](http://jira.pcgen.org/browse/NEWTAG-477) / Github [PR
    \#380](https://github.com/PCGen/pcgen/pull/380)
-   -   All `FEAT` tags have been **deprecated** and replaced by the
        `ABILITY` system, which is more general. The `ABILITY` system
        can model feats, racial features, class features, traits, flaws,
        temporary bonuses, and so on, all using a common format.

What it does
------------

-   Provides options for removing hidden and standard feats, but not
    those applied with the VFEAT tag.
-   The number of feats to be removed (x) is optional. If not present
    the tag simply removes whatever feats are specified in variable (y).
-   When `ALL` is used for (x), all indicated feats are removed
    without prompting.

Example
-------

`REMOVE:FEAT|Alertness`

Removes the Alertness feat, no choice is presented, the feat is simply
removed.

`REMOVE:FEAT|TYPE.Fighter`

Presents a list of Fighter type feats and allows the removal of up to 3.

`REMOVE:FEAT|2|CHOICE`

Presents a list of all feats the character has and allows the removal of
2 of them. If a feat has a cost associated with it, it returns that cost
to the feat pool.

`REMOVE:FEAT|ALL|CLASS.Paladin`

Removes all feats that have been granted/taken by the Paladin Class.

**Where it can be used:**

Works in Ability, Class and Template files.

