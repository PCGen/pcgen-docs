+++
date = "2016-08-01"
title = "WEIGHTPATTERN (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#weightpattern"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "WEIGHTPATTERN"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_WEIGHTPATTERN"
+++

## Status

New 5.9.5

## Syntax

`WEIGHTPATTERN:x`

## Parameters

-   x: Text (Weight unit pattern).



What it does
------------

Used in UNITSET lines to define the weight unit pattern. The 'pattern'
string is a pattern for formatting the output of the value, so you can
specify e.g. how many decimal digits are printed. The pattern follows
the definition of the Java class DecimaFormat and can be found
[here](http://java.sun.com/j2se/1.3/docs/api/java/text/DecimalFormat.html)
.

Example
-------

`WEIGHTPATTERN:#.##`

Defines the weight unit pattern as "ft.".

Where it is used
----------------

Used in [UNITSET](/list/system/gamemode-miscinfo/unitset.html) lines.

