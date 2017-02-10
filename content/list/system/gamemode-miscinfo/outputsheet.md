+++
date = "2016-08-01"
title = "OUTPUTSHEET (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#outputsheet"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "OUTPUTSHEET"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 6.01.06

## Syntax

`OUTPUTSHEET:x|y`

## Parameters

-   x: DIRECTORY
-   x: DEFAULT.HTM
-   x: DEFAULT.PDF
-   x: DEFAULT.TXT
-   y: Text (File path)



What it does
------------

Defines where outputsheets are stored and identifies the default html,
pdf, and txt OSes for the associated gamemode.

Example
-------

`OUTPUTSHHET:DIRECTORY|outputsheets/d20/fantasy`

Outputsheets for this gamemode will be stored in the
"outputsheets/d20/fantasy" folder.

`OUTPUTSHHET:DEFAULT.PDF|outputsheets/d20/fantasy/pdf/csheet_fantasy_std_blue.xslt`

The default pdf OS for this gamemode is
"outputsheets/d20/fantasy/pdf/csheet\_fantasy\_std\_blue.xslt" OS.

`OUTPUTSHHET:DEFAULT.HTM|outputsheets/d20/fantasy/htmlxml/csheet_fantasy_std.htm`

The default html OS for this gamemode is
"outputsheets/d20/fantasy/htmlxml/csheet\_fantasy\_std.htm" OS.

