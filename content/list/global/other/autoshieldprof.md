+++
date = "2016-08-01"
title = "AUTOSHIELDPROF (Global: OTHER)"
original_url = "/list/global/other.html#autoshieldprof"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "AUTOSHIELDPROF"
    parent = "global_other"
+++

## Status

Updated 5.17.11

## Syntax

`AUTO:SHIELDPROF|x|x`

## Parameters

-   x: Text (Shield name)
-   x: SHIELDTYPE=Text (Shield type)



What it does
------------

-   This is a pipe-delimited (|) list of shields, by name or shield
    type, that are granted as free shield proficiencies.
-   When including the `SHIELDTYPE=` sub-tag you may use a
    period-delimted (.) list of shield types. This will grant the
    character proficiency with shields that meet all of the listed
    shield types.
-   PRExxx tags are allowed with this tag and use the pipe-delimited (|)
    syntax.

Examples
--------

`AUTO:SHIELDPROF|SHIELDTYPE=Buckler`

Buckler shield is given as a free shield proficiency.

`AUTO:SHIELDPROF|SHIELDTYPE=Buckler|SHIELDTYPE=Light|SHIELDTYPE=Heavy`

Buckler, Light, and Heavy Shields are given as free shield
proficiencies.

