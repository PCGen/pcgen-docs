+++
date = "2016-08-01"
title = "MINVER (Data: install.lst)"
original_url = "/list/data/install.html#minver"
categories = [ "all-tag", "install-tag" ]
[menu.main]
    name = "MINVER (Data: install.lst)"
    parent = "install"
+++

## Status

None

## Syntax

`MINVER:x`

## Parameters

-   x: Text (Version number)



<span id="minver"></span>

What it does
------------

-   Mandatory tag specifying the minimum version of PCGen that will
    support his dataset.
-   Normally this will be based on tags supported in the version
    of PCGen.
-   For the source to be installed by PCGen, the version of PCGen in use
    must be equal to or greater than this version.
-   e.g. a MINVER:5.14.1 value would mean that the source could not be
    installed by 5.14.0, but could be installed by 5.14.1 or 5.16.0

Example
-------

`MINVER:5.14.1`

This dataset requires PCGen prodiction version 5.14.1 or later.

