+++
date = "2016-08-01"
title = "ALLOWDUPES (Data: campaign.pcc)"
original_url = "list/data/pcc.html#allowdupes"
categories = [ "all-tag", "pcc-tag" ]
+++

## Status

New 5.15.10

## Syntax

`ALLOWDUPES:x`

## Parameters

-   x: LANGUAGE
-   x: SPELL



What it does
------------

-   Suppresses the "Duplicate Object" error messages for the listed LST
    object type.
-   This tag will only work if the PCC file it is contained in is the
    exact PCC file selected by the user.

Examples
--------

`ALLOWDUPES:SPELL`

Duplicate spells loaded by the user selected PCC files will be allowed.

