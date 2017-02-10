+++
date = "2016-08-01"
title = "ICON (Game Mode: equipicons.lst)"
original_url = "/list/system/gamemode-equipicons.html#icon"
categories = [ "all-tag", "gamemode-equipicons-tag" ]
[menu.main]
    name = "ICON"
    parent = "system_gamemode-equipicons"
    identifier = "system_gamemode-equipicons_ICON"
+++

## Status

New 5.17.7 - Updated 5.17.14

## Syntax

`ICON:x|y|z`

## Parameters

-   x: Text (Equipment Type)
-   y: Number (File Path)
-   z: Number (Priority. Optional. Default is 10)



What it does
------------

This links an equipment type to an icon. It sets the path to the default
icon to be used for any item of equipment of the specified type. The
path is relative to the pcgen install folder. The priority allows icons
to be chosen where an equipment item has multiple types. The default is
10 and higher numbers mean higher priority.

Example
-------

`ICON:Eyegear|system/icons/eyegear.png`

The default icon for this type will be <span class="lstfile">
system/icons/eyegear.png </span> relative to the program install
directory. Priority will be 10.

`ICON:Container|system/icons/container.png|3`

The default icon for this type will be <span class="lstfile">
system/icons/container.png </span> relative to the program install
directory. Priority will be 3 (a low priority).

