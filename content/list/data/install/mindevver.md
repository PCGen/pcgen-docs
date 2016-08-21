+++
date = "2016-08-01"
title = "MINDEVVER (Data: install.lst)"
original_url = "list/data/install.html#mindevver"
categories = [ "all-tag", "install-tag" ]
+++

## Status

None

## Syntax

`MINDEVVER:x`

## Parameters

-   x: Text (Version number)



<span id="mindevver"></span>

What it does
------------

-   Optional tag specifying the minimum development version of PCGen
    that will support this dataset, where this is later than the
    production version.
-   This would be used where a tag was added partway through a dev cycle
    and then retrofitted to the next patch release of PCGen.
-   For the source to be installed by PCGen, the version of PCGen must
    either:
    -   Have an even minor version (as in 5.x.y, where x is even
        indicating a production release) and be greater than or equal to
        the MINVER value; or
    -   Have an odd minor version (as in 5.x.y, where x is odd
        indicating a development release) and be greater than or equal
        to the MINDEVVER value.
    -   e.g. Given `MINVER:5.14.1` and `MINDEVVER:5.15.3` , the source
        could not be installed by 5.15.2, but could be installed by
        5.14.1 or 5.15.3

Example
-------

`MINDEVVER:5.15.2`

This dataset requires PCGen developer version 5.15.2 or later.

