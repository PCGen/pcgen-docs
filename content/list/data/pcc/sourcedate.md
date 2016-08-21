+++
date = "2016-08-01"
title = "SOURCEDATE (Data: campaign.pcc)"
original_url = "list/data/pcc.html#sourcedate"
categories = [ "all-tag", "pcc-tag" ]
+++

## Status

None

## Syntax

`SOURCEDATE:x`

## Parameters

-   x: Date (Release date of source in format YYYY-MM)



<span id="sourcedate"></span> \*\*\* New 5.9.5

What it does
------------

Allows PCGen to determine which of two sources is newer. A source
without this tag will be considered older than a source with a set date.
There is a preference which must be checked to activate this feature. In
Preferences/PCGen/Sources check the box for "Allow newer sources to
override duplicate object from older sources".

Example
-------

`SOURCEDATE:2005-12`

This source was published in December 2005.

