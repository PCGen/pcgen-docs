+++
date = "2016-08-01"
title = "LSTEXCLUDE (Data: campaign.pcc)"
original_url = "list/data/pcc.html#lstexclude"
categories = [ "all-tag", "pcc-tag" ]
+++

## Status

None

## Syntax

`LSTEXCLUDE:x|x`

## Parameters

-   x: Text (File names)



What it does
------------

This is a | (pipe) delimited tag which allows you to customize which LST
files are loaded. This must be before PCC/LST file INCLUDE statements if
used. All of the files listed will NOT be loaded, even if referenced
later by other included PCC files. The LST file list can be a single LST
filename per entry, or can be separated by the "|" (pipe) character. The
full path to the file is needed unless the .pcc file containing the
LSTEXCLUDE tag is in the same directory as the files to be excluded.

Examples
--------

`LSTEXCLUDE:fooraces.lst`

`LSTEXCLUDE:fooraces.lst|foogods.lst`

`LSTEXCLUDE:@d20ogl/foogames/foohandbook/fooclasses.lst`

