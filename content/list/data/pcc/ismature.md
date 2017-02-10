+++
date = "2016-08-01"
title = "ISMATURE (Data: campaign.pcc)"
original_url = "/list/data/pcc.html#ismature"
categories = [ "all-tag", "pcc-tag" ]
[menu.main]
    name = "ISMATURE"
    parent = "data_pcc"
    identifier = "data_pcc_ISMATURE"
+++

## Status

None

## Syntax

`ISMATURE:x`

## Parameters

-   x: Boolean (YES or NO)



What it does
------------

This tag is so that we have the ability to include datasets based upon
sources of a more mature nature. If `ISMATURE:YES` then the following
info gets inserted into a pop-up window "This dataset contains content
of a mature nature. User discretion is advised." This tag is optional.

Examples
--------

`ISMATURE:YES`

Causes a pop-up to fire saying "This dataset contains content of a
mature nature. User discretion is advised."

`ISMATURE:NO`

Does not cause a pop-up to fire saying "This dataset contains content of
a mature nature. User discretion is advised."

**Default Value:**

`NO`

