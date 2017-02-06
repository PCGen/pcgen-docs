+++
date = "2016-08-01"
title = "DEFAULTDATASET (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#defaultdataset"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "DEFAULTDATASET (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

Updated 5.15.13

## Syntax

`DEFAULTDATASET:x,x|y`

## Parameters

-   x: Text (Default Data Set Name)
-   y: Text (Displayed Data Set Name, Optional)



What it does
------------

-   Sets the Default data Set used by the game mode.
-   If the display name is set then the game mode will be displayed in
    the Load Sources dialog with that name.
-   If no display name is provided then the default sources will not
    appear on the Load Sources dialog.
-   The display name has no effect on the Advanced sources page.

Example
-------

`DEFAULTDATASET:3.5 RSRD`

The "3.5 RSRD" data set will appear in the right panel on the sources
tab when this gamemode is loaded.

`DEFAULTDATASET:MSRD - Basics,MSRD - Arcana,MSRD - Future,MSRD - Menaces|MSRD`

The default data sets for the game mode are the four sources named and
they will have a button on the "Load Sources" dialog titled "MSRD"".
When the button is selected all four sources are loaded.

