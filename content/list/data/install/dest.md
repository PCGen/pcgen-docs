+++
date = "2016-08-01"
title = "DEST (Data: install.lst)"
original_url = "/list/data/install.html#dest"
categories = [ "all-tag", "install-tag" ]
[menu.main]
    name = "DEST"
    parent = "data_install"
    identifier = "data_install_DEST"
+++

## Status

None

## Syntax

`DEST:x`

## Parameters

-   x: Text (DATA or VENDORDATA)



<span id="dest"></span>

What it does
------------

-   The recommended install path for the source.
-   Sources installed in the Data folder will be replaced in the next
    release of PCGen.
-   Sources installed in Vendor Data will be retained through an
    upgrade process.

Example
-------

`DEST:DATA`

The dataset will be installed within the DATA folder in PCGen.

