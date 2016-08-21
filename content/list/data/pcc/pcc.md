+++
date = "2016-08-01"
title = "PCC (Data: campaign.pcc)"
original_url = "list/data/pcc.html#pcc"
categories = [ "all-tag", "pcc-tag" ]
+++

## Status

None

## Syntax

`PCC:x`

## Parameters

-   x: Text (File path)



What it does
------------

-   Tells PCGen to load additional pcc files along with the current
    pcc file.
-   If the campaign file to be loaded by this tag isn't located in the
    same folder as the current campaign file then file path must
    be included.
    -   The `@` symbol used at the beginning of the file path will set
        the **data** folder as the top folder in the path.
    -   The `&` symbol used at the beginning of the file path will set
        the **vendor** folder as the top folder in the path.
    -   The `$` symbol used at the beginning of the file path will set
        the **homebrew** folder as the top folder in the path.
-   It is recommended that this tag be placed before any tags that load
    LST files.

Example
-------

`PCC:@/d20ogl/paizo/pathfinder_rpg/pathfinder_rpg_for_players_advanced.pcc`

Loads the campaign file <span class="lstfile">
pathfinder\_rpg\_for\_players\_advanced.pcc </span> found in the <span
class="lstfile"> data/d20ogl/paizo/pathfinder\_rpg/ </span> folder.

`PCC:&/foodir/foobook.pcc`

Loads the campaign file <span class="lstfile"> foobook.pcc </span> found
in the <span class="lstfile"> vendor/foodir/ </span> folder.

