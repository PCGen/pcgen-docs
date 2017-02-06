+++
date = "2016-08-01"
title = "OPTION (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#option"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "OPTION (Data: campaign.pcc)"
    parent = "pcc"
+++

## Status

None

## Syntax

`OPTION:x`

## Parameters

-   x: Text (Option)



What it does
------------

Specifies an option which should be set when the campaign is loaded. The
format is the same as in the `options.ini` or `legacy.ini` files. For
options from `legacy.ini` only the *pcgen.options* lines may be used and
they need to have the *pcgen.options.* part removed from their key when
provided here.

The user can stop these options from being set by unselecting the *PCGen
-&gt; Sources -&gt; Allow options to be set by sources* setting in the
Preferences dialog.

Examples
--------

`OPTION:hpMaxAtFirstLevel=true`

Set the pcgen.options.hpMaxAtFirstLevel preference stored in legacy.ini
to true.

`OPTION:gameMode.Pathfinder_RPG.purchaseMethodName=Epic Fantasy`

Set the selected stats purchase mode (stored in options.ini) for the
Pathfinder\_RPG game mode to "Epic Fantasy".

`OPTION:pcgen.options.autoResizeEquip=true`

Set the auto resize equipment for PC option (stored in options.ini) to
true.

