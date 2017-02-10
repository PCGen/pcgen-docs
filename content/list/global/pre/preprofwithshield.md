+++
date = "2016-08-01"
title = "PREPROFWITHSHIELD (Global: PRErequisite)"
original_url = "/list/global/pre.html#preprofwithshield"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREPROFWITHSHIELD"
    parent = "global_pre"
    identifier = "global_pre_PREPROFWITHSHIELD"
+++

## Status

NEW 5.15.8

## Syntax

`PREPROFWITHSHIELD:x,y,y`

## Parameters

-   x: Number (The number of shield
    proficiencies needed).
-   y: Text (The name of a shield proficiency).
-   y: TYPE.Text (The type of shield proficiency).



What it does
------------

Checks for shield proficiency requirements.

Examples
--------

`PREPROFWITHSHIELD:1,Buckler,Large Shield`

Character must be proficient with either "Buckler" or "Large Shield".

`PREPROFWITHSHIELD:1,TYPE.Tower`

Character must be proficient with Tower shields.

