+++
date = "2016-08-01"
title = "PRETEMPLATE (Global: PRErequisite)"
original_url = "/list/global/pre.html#pretemplate"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRETEMPLATE"
    parent = "global_pre"
    identifier = "global_pre_PRETEMPLATE"
+++

## Status

None

## Syntax

`PRETEMPLATE:x,y,y`

## Parameters

-   x: Number (Number of templates required)
-   y: Text (Template name)



What it does
------------

-   Sets template requirements. If one of the template names in the list
    matches, the prerequisite is met.
-   The wildcard character (%) can be used within this tag.

Example
-------

`PRETEMPLATE:1,Celestial,Fiendish`

Character must be either "Celestial" or "Fiendish".

`PRETEMPLATE:1,Feral%`

Character must be any subrace of Feral.

