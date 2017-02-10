+++
date = "2016-08-01"
title = "SOURCEWEB (Global: OTHER)"
original_url = "/list/global/other.html#sourceweb"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "SOURCEWEB"
    parent = "global_other"
    identifier = "global_other_SOURCEWEB"
+++

## Status

Updated 5.10

## Syntax

`SOURCEWEB:x`

## Parameters

-   x: Text (Source Web Site)



What it does
------------

-   Specifies the URL that points directly to this product/book.
-   This tag is used on its own line, with other `SOURCExxx` tags, or on
    individual object lines.
-   When used on its own line the `SOURCEWEB` tag will be used by all
    objects which follow it.
-   When used on individual object lines it applies to that object and
    overrides any stand alone `SOURCEWEB` tag on lines which
    preceeded it.

Example
-------

`SOURCEWEB:http://www.foogames.com/product.php?products=654321`

The web site for this source is
"SOURCEWEB:http://www.foogames.com/product.php?products=654321".

