+++
date = "2016-08-01"
title = "PRECHECKBASE (Global: PRErequisite)"
original_url = "/list/global/pre.html#precheckbase"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRECHECKBASE"
    parent = "global_pre"
    identifier = "global_pre_PRECHECKBASE"
+++

## Status

None

## Syntax

`PRECHECKBASE:x,y=z`

## Parameters

-   x: Number (The number of base checks that must be
    equal to or greater than the numbers specified for the check
    to succeed).
-   y: Text (A defined check from statsandchecks.lst -
    e.g. Fortitude or Willpower).
-   z: Number (The number the associated base check
    must be greater than or equal to).



What it does
------------

Sets the minimum Base Check requirements. Base Checks are usually only
those from class advancement (no stat modifiers, magic, etc.), but
follow anything defined with " `BONUS:CHECKS|BASE.Name|` ".

Examples
--------

`PRECHECKBASE:2,Fortitude=3,Reflex=3`

Would succeed if both Fortitude meets or exceeds 3 and Reflex meets or
exceeds 3.

`PRECHECKBASE:1,Fortitude=5,Reflex=3`

Would succeed if Fortitude meets or exceeds 5 or Reflex meets or exceeds
3.

