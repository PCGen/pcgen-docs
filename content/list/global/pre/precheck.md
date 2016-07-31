+++
date = "2016-08-01"
title = "PRECHECK (Global: PRErequisite)"
original_url = "list/global/pre.html#precheck"
categories = [ "all-tag", "pre-tag" ]
+++

## Status

None

## Syntax

`PRECHECK:x,y=z`

## Parameters

-   x: Number (The number of checks that must be equal
    to or greater than the numbers specified for the check to succeed).
-   y: Text (A defined check from statsandchecks.lst -
    e.g. Fortitude or Willpower).
-   z: Number (The number the associated check must be
    greater than or equal to).



What it does
------------

Sets the minimum CHECK requirements.

Examples
--------

`PRECHECK:1,Fortitude=5,Reflex=3`

Would succeed if Fortitude meets or exceeds 5 or Reflex meets or exceeds
3.

`PRECHECK:2,Fortitude=5,Reflex=3,Willpower=4`

Would succeed if any 2 of the 3 three listed conditions were met.

