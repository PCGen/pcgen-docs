+++
date = "2016-08-01"
title = "PREMOVE (Global: PRErequisite)"
original_url = "/list/global/pre.html#premove"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREMOVE"
    parent = "global_pre"
    identifier = "global_pre_PREMOVE"
+++

## Status

Updated 5.9.4

## Syntax

`PREMOVE:x,y=z,y=z`

## Parameters

-   x: Number (The minimum number movement types which
    must pass).
-   y: Text (The name of a type of movement).
-   z: Number (The minimum movement rate for the
    associated movement type).



What it does
------------

Makes movement rate a prerequisite.

Examples
--------

`PREMOVE:1,Walk=30,Fly=20`

Character must be able to either walk at speed 30 OR fly at speed 20

`PREMOVE:1,Swim=10`

Character must be able to swim at speed 10

`PREMOVE:2,Walk=30,Climb=15`

Character must be able to walk at speed 30 AND climb at speed 15

