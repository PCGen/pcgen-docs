+++
date = "2016-08-01"
title = "RANK (Data: campaign.pcc)"
original_url = "list/data/pcc.html#rank"
categories = [ "all-tag", "pcc-tag" ]
+++

## Status

None

## Syntax

`RANK:x`

## Parameters

-   x: Number (Rank)



<span id="rank"></span> \*\*\* Updated 5.12 RC3

What it does
------------

Sets the priority in loading .pcc files. 1 is the highest priority and 9
is the lowest priority for loading .pcc files.

When PCGen encounters certain objects with duplicate names from
different sources (such as Classes) the object in the source with the
highest priority rank will be loaded while the duplicate will generate
an error message (and will not be loaded).

It is recommended that all RANK numbers should be expressed a positive
numbers as negative numbers will load before the positive.

Defaults to 9 if no RANK is set in the PCC file.

Example
-------

`RANK:1`

This pcc file is given first priority when loading.

**Officially sanctioned use of ranks:**

RANK:0 - Whatever has to be loaded before the Core

RANK:1 - Core rules

RANK:2 - Campaign settings

RANK:3 - Supplements

RANK:4 - Web enhancements

RANK:5 - 3rd party campaign books

RANK:6 - 3rd party supplements

RANK:7 - 3rd party web enhancements

RANK:8 and 9 - Homebrew

