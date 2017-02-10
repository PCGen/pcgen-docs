+++
date = "2016-08-01"
title = "DESC (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#desc"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "DESC"
    parent = "data_pcc"
    identifier = "data_pcc_DESC"
+++

## Status

None

## Syntax

`DESC:x`

## Parameters

-   x: Text (Information)



<span id="desc"></span> \*\*\* New 5.13.9

What it does
------------

-   Provides text information that is displayed in the Source
    Information Panel, on the Source Tab, when the source material
    is selected.
-   This tag shall be used only once per pcc.
-   This text will appear just below the cover image (if there is one)
    or the CAMPAIGN header (if there is no cover image).
-   The text is a short description of the selected source such as one
    might find at amazon.com or other book/pdf seller.
-   Functionally this is the same as INFOTEXT except where it appears in
    the Source Info panel.

Example
-------

`DESC:This pcc loads all the Foo source materials minus the FooWorld races`

