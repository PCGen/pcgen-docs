+++
date = "2016-08-01"
title = "FEAT (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#feat"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "FEAT (Data: campaign.pcc)"
    parent = "pcc"
+++

## Status

None

## Syntax

`FEAT:x`

## Parameters

-   x: Text (File path)



<span id="feat"></span>

**Status:**

-   6.05.04 (July 2015): JIRA
    [NEWTAG-477](http://jira.pcgen.org/browse/NEWTAG-477) / Github [PR
    \#380](https://github.com/PCGen/pcgen/pull/380)
    -   The `FEAT` file is deprecated. Use
        [`ABILITY`](/list/data/pcc/abilitypcc.html) instead.
    -   All `FEAT` tags have been **deprecated** and replaced by the
        `ABILITY` system, which is more general. The `ABILITY` system
        can model feats, racial features, class features, traits, flaws,
        temporary bonuses, and so on, all using a common format.

What it does
------------

Tells PCGen to load the feats list file specified.

Example
-------

`FEAT:foofeats.lst`

