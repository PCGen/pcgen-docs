+++
date = "2016-08-01"
title = "STARTPACK (Data: starting_kits.lst)"
original_url = "list/data/startingkits.html#startpack"
categories = [ "all-tag", "startingkits-tag" ]
+++

## Status

None

## Syntax

`STARTPACK:x`

## Parameters

-   x: Text (Kit name)



What it does
------------

-   This MUST be the FIRST line of a new kit definition.
-   Starts creation of a new kit.
-   All lines following this one are considered part of this kit until a
    new STARTPACK tag, or the end of the file, is encountered.

Example
-------

`STARTPACK:Bar1`

Would create a new available kit called "Bar1".

