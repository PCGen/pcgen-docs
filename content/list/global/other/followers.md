+++
date = "2016-08-01"
title = "FOLLOWERS (Global: OTHER)"
original_url = "/list/global/other.html#followers"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "FOLLOWERS (Global: OTHER)"
    parent = "other"
+++

## Status

New 5.11.0

## Syntax

`FOLLOWERS:x|y`

## Parameters

-   x: Text (The type of companion the limit will
    apply to).
-   x: Number, variable or formula (Number of this type
    of companion the master can have)



What it does
------------

Limits the number of the specified type of companion the master can
have.

Optional, if this tag is not present no limits are placed on the number
of companions the character can have.

If more than one tag is encountered the highest value is used.

The value can be adjusted with the BONUS:FOLLOWERS tag.

Where it is used
----------------

Global tag, would most often be used in class and feat (ability) files,
should also be enabled for templates and Domains.

Examples
--------

`FOLLOWERS:Familiar|1`

A character is allowed only 1 companion of type Familiar.

