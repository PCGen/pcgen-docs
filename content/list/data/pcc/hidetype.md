+++
date = "2016-08-01"
title = "HIDETYPE (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#hidetype"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "HIDETYPE"
    parent = "data_pcc"
+++

## Status

None

## Syntax

`HIDETYPE:x|y|y`

## Parameters

-   x: EQUIP (Equipment Types will be hidden)
-   x: FEAT (Feat Types will be hidden)
-   x: SKILL (Skill Types will be hidden)
-   y: Text (Type to be hidden)



<span id="hidetype"></span> \*\*\* New 5.9.1

What it does
------------

This tag will prevent the listed Types from appearing within the user
interface while allowing it to be used internally by PCGen. This is
useful when types need to be added for internal purposes but it is not
desirable to have the type show in the GUI. HIDETYPE will effect all
sources loaded but only when the .pcc file it is in is loaded.

Example
-------

`HIDETYPE:EQUIP|Starting|SpecialTools`

The Types Starting and SpecialTools will not be visible in the user
interface. The equipment type "Starting" is hardcoded into the feature
which provides free clothing at first level.

