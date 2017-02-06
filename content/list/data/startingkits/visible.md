+++
date = "2016-08-01"
title = "VISIBLE (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#visible"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "VISIBLE (Data: starting_kits.lst)"
    parent = "startingkits"
+++

## Status

Updated 5.9.2

## Syntax

`VISIBLE:x`

## Parameters

-   x: YES (Default)
-   x: NO
-   x: QUALIFY



What it does
------------

-   This is an optional tag that determins whether the KIT appears in
    the KIT Selection window.
-   `YES` - Displays the name of the KIT in the KIT selection window.
-   `NO` - Hides the name of the KIT in the KIT selection window.
-   `QUALIFY` - Displays the name of the KIT only if the character
    passes the prerequisites.

Example
-------

`VISIBLE:YES`

Shows the KIT name in PCGen.

`VISIBLE:NO`

Hides the KIT name in PCGen.

`VISIBLE:QUALIFY`

The KIT name will be displayed in PCGen if the character meets all
prerequisites.

Where it is used
----------------

STARTPACK lines

