+++
date = "2016-08-01"
title = "PREVIEWSHEET (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#previewsheet"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "PREVIEWSHEET (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

New 5.13.2

## Syntax

`PREVIEWSHEET:x`

## Parameters

-   x: Text (Path to specified directory)



What it does
------------

Sets the default sheet used by the [Character Sheet
Tab](/tab/character-sheet.html) for this gameMode. The sheet specified
must exist in the directory set by the gameModes
[PREVIEWDIR](/list/system/gamemode-miscinfo/previewdir.html) tag.

Example
-------

`PREVIEWSHEET:preview.html`

Sets the "preview.html" file as the default sheet displayed when the
Character Sheet Tab is selected.

