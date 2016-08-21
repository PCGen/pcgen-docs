+++
date = "2016-08-01"
title = "WEAPONFOCUS (Global: CHOOSE)"
original_url = "list/global/choose.html#weaponfocus"
categories = [ "all-tag", "choose-tag" ]
+++

## Status

None

## Syntax

`CHOOSE:WEAPONFOCUS|x`

## Parameters

-   x: TYPE.Text (Equipment type)



<span id="weaponfocus"></span>

What it does
------------

-   This will produce a list of weaponprofs associated with the Weapon
    Focus Feat.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

Example
-------

`CHOOSE:WEAPONFOCUS|TYPE.Sword`

Present a list of weaponprofs associated with a character's Weapon Focus
feats that match a given equipment type.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

