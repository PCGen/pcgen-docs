+++
date = "2016-08-01"
title = "MODIFYFEATCHOICE (Data: feats.lst)"
original_url = "/list/data/feats.html#modifyfeatchoice"
categories = [ "all-tag", "feats-tag" ]
[menu.main]
    name = "MODIFYFEATCHOICE"
    parent = "data_feats"
+++

## Status

New 5.11.x

## Syntax

`MODIFYFEATCHOICE:x`

## Parameters

-   x: Text (feat name)
-   x: TYPE=Text (feat type)



What it does
------------

-   This tag allows for a previous feat choice to be replaced by a
    new one.
-   The feat called must allow choices to be a valid ability.
-   **.MOD Behavior:** When modifying an feat with the `.MOD` tag, given
    an existing `MODIFYFEATCHOICE` tag, the data included in a new
    `MODIFYFEATCHOICE` tag will overwrite the existing tag data.

Example
-------

`MODIFYFEATCHOICE:TYPE=NinjaMonkeySchool`

Allows the selection of a new school from a list of schools of type
'NinjaMonkeySchool' to replace a previously selected one.

`MODIFYFEATCHOICE:Ninja Monkey Primary Weapon Reselection`

Allows a ninja monkey to select a new primary weapon, replacing an
earlier selected primary weapon.

**.MOD Example:**

Initial Feat:
`<feat name> <tab> MODIFYFEATCHOICE:TYPE=NinjaMonkeyChimpSchool`

Modified By:
`<feat name> <tab> MODIFYFEATCHOICE:TYPE=NinjaMonkeySilverbackSchool`

Is Equivalent To:
`<feat name> <tab> MODIFYFEATCHOICE:TYPE=NinjaMonkeySilverbackSchool`

Modified feat allows the selection of a new school from a list of
schools of type 'NinjaMonkeySilverbackSchool' to replace a previously
selected one.

