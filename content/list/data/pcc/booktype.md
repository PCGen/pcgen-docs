+++
date = "2016-08-01"
title = "BOOKTYPE (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#booktype"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "BOOKTYPE"
    parent = "data_pcc"
+++

## Status

None

## Syntax

`BOOKTYPE:x|x`

## Parameters

-   x: Text (Book type)



<span id="booktype"></span> \*\*\* Updated 6.1.1

What it does
------------

-   This tells PCGen what the book types are.
-   The book types identified by this tag can be used as a prerequisite
    for loading data sets. See the
    [PRECAMPAIGN](/list/data/pcc/precampaign.html) tag docs for
    more information.

Example
-------

`BOOKTYPE:Supplement`

The source data set that this PCC file represents is a "Supplement".

`BOOKTYPE:Supplement|Traits`

The source data set that this PCC file represents is a "Supplement" and
also provides the basics for Traits rules.

