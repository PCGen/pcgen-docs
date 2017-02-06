+++
date = "2016-08-01"
title = "TEMPLATEADDCHOICE (Data: feats.lst)"
original_url = "/list/data/feats.html#templateaddchoice"
categories = [ "all-tag", "feats-tag" ]
[menu.main]
    name = "TEMPLATEADDCHOICE (Data: feats.lst)"
    parent = "feats"
+++

## Status

None

## Syntax

`TEMPLATE:ADDCHOICE:x|x`

## Parameters

-   x: Text (Template Name)



What it does
------------

-   This is a pipe-delimited list of template choices that are added to
    the list presented by the original `TEMPLATE:CHOOSE` tag.
-   When using the `TEMPLATE:ADDCOICE` tag as part of a `.MOD` of a Feat
    that containes multiple `TEMPLATE:CHOOSE` tags, all instances of the
    `TEMPLATE:CHOOSE` tag will be modified.

Example
-------

`TEMPLATE:ADDCHOICE:Demihuman|Beast`

The feat allows the selection of previously defined templates plus the
"Demihuman" or "Beast" templates.

