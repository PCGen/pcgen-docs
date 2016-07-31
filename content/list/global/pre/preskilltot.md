+++
date = "2016-08-01"
title = "PRESKILLTOT (Global: PRErequisite)"
original_url = "list/global/pre.html#preskilltot"
categories = [ "all-tag", "pre-tag" ]
+++

## Status

None

## Syntax

`PRESKILLTOT:x,x=y`

## Parameters

-   x: Text (skill name).
-   x: TYPE=Text (skill type).
-   y: Number (total non-bonus skill ranks required).



What it does
------------

-   A comma-delimited list of skills whose total non-bonus ranks must
    equal y.
-   Skills may be identified by TYPE.

Example
-------

`PRESKILLTOT:Spot,Listen,Search=30`

Character must have a total of 30 non-bonus ranks between Spot, Search,
and Listen skills.

