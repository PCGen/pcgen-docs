+++
date = "2016-08-01"
title = "COPYRIGHT (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#copyright"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "COPYRIGHT"
    parent = "data_pcc"
    identifier = "data_pcc_COPYRIGHT"
+++

## Status

None

## Syntax

`COPYRIGHT:x`

## Parameters

-   x: Text (Copyright information)



What it does
------------

-   Used to display copyright information when a source is selected in
    the source selection page.
-   Sources included with PCGen should have the copyright information
    from section 15 of the Open Game License included in the source
    reproduced verbatim.
-   An additional entry should be made listing all who worked on the
    PCGen conversion in the format shown below.

Example
-------

`COPYRIGHT:PCGen dataset conversion for "X Book" Copyright XXXX-YYYY, PCgen Data Team including, but not limited to, "Original Author", "Any secondary authors".`

This is the Sec. 15 that should be added to all sources going into
PCGen. X Book should be the name of the source, XXXX should be the year
the dataset was created and YYYY is the current year. Please list all
contributors to the dataset.

`COPYRIGHT:Foo Reference Document &copy 2003 Foo Games, Inc.`

**Note(s):** `&copy` - This code coverts to a copyright symbol (©) when
put in the text of a COPYRIGHT tag.

