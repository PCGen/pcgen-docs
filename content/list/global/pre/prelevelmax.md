+++
date = "2016-08-01"
title = "PRELEVELMAX (Global: PRErequisite)"
original_url = "/list/global/pre.html#prelevelmax"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRELEVELMAX"
    parent = "global_pre"
    identifier = "global_pre_PRELEVELMAX"
+++

## Status

None

## Syntax

`PRELEVELMAX:x`

## Parameters

-   x: Number (The maximum level).



What it does
------------

Requires that a character have a maximum number of character
(non-monster) levels.

-- Do NOT mix PRELEVELMAX and BONUS:SKILLPOINTS|NUMBER, since it results
in double negative and some very bad exceptions in the code.

Example
-------

`PRELEVELMAX:10`

Character cannot be over level 10.

