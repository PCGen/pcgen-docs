+++
date = "2016-08-01"
title = "SOURCESHORT (Global: OTHER)"
original_url = "/list/global/other.html#sourceshort"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "SOURCESHORT (Global: OTHER)"
    parent = "other"
+++

## Status

Updated 5.10

## Syntax

`SOURCESHORT:x`

## Parameters

-   x: Text (Short Source Name)



What it does
------------

-   Specifies the short product/book name.
-   This tag is used on its own line, with other `SOURCExxx` tags, or on
    individual object lines.
-   When used on its own line the `SOURCESHORT` tag will be used by all
    objects which follow it.
-   When used on individual object lines it applies to that object and
    overrides any stand alone `SOURCESHORT` tag on lines which
    preceeded it.

Example
-------

`SOURCESHORT:FHB`

The short source name for this file is "FHB".

