+++
date = "2016-08-01"
title = "SELECT (Global: OTHER)"
original_url = "/list/global/other.html#select"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "SELECT (Global: OTHER)"
    parent = "other"
+++

## Status

New 5.13.9

## Syntax

`SELECT:x`

## Parameters

-   x: Number, Variable, or Formula (Number of choices)



What it does
------------

-   This tag is optional.
-   Defines the number of choices allowed every time the associated
    object is taken.
-   This tag is used in conjunction with a `CHOOSE` tag that does not
    already have an integrated number for "choices" to be made.
-   If this tag is not used the default number of selections made is
    one (1).
-   Tag is ignored when used in conjunction with `CHOOSE:NOCHOICE` .

Example
-------

`SELECT:3 <tab> CHOOSE:SKILLS`

Allows the selection of "3" skills selected from the list of skills
currently held by the character.

`SELECT:INT`

Allows a number of choices equal to the Intelligence ability bonus.

