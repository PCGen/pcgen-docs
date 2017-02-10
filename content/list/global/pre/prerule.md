+++
date = "2016-08-01"
title = "PRERULE (Global: PRErequisite)"
original_url = "/list/global/pre.html#prerule"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRERULE"
    parent = "global_pre"
+++

## Status

None

## Syntax

`PRERULE:x,y`

## Parameters

-   x: Number (Number of rules required)
-   y: Text (Rule name)



What it does
------------

-   Checks for the state of a rule.
-   The rule name must have been defined and match the variable (
    `VAR` ) entry in the *system/gameModes/rules.lst* file.
-   Rules can be turned on and off by the user in the **House Rules**
    section of the preferences.

Example
-------

`PRERULE:1,SYS_WTPSK`

The rule WeightPenaltyToSkill must be checked for this to apply.

