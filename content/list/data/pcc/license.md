+++
date = "2016-08-01"
title = "LICENSE (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#license"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "LICENSE"
    parent = "data_pcc"
+++

## Status

None

## Syntax

`LICENSE:x`

## Parameters

-   x: Text (License information)
-   x: FILE=Text (HTML file)



<span id="license"></span> \*\*\* New 5.3.3

What it does
------------

Displays special license information in a pop-up at time of source load.
Requires a `ISLICENSED:YES` tag to be active.

Examples
--------

`LICENSE:This set included with special permission from Foo Games`

Would display the text in a nice box with other licenses.

`LICENSE:FILE=foolicense.html`

Doing a `FILE=` allows PCC to point to an HTML formatted file, which
will display in a box of its own.

