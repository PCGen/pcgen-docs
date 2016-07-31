+++
date = "2016-08-01"
title = "TOTALWT (System: bio/biosettings.lst)"
original_url = "list/system/biosettings.html#totalwt"
categories = [ "all-tag", "biosettings-tag" ]
+++

## Status

None

## Syntax

`TOTALWT:x`

## Parameters

-   x: Number or Formula (Total weight of
    the character)



What it does
------------

The TOTALWT tag is used inside of the SEX tag to define the total weight
of your character. It can use standard numbers, as well as the BASEWT,
WTDIEROLL and HTDIEROLL variables.

Example
-------

`TOTALWT:BASEWT+(HTDIEROLL*WTDIEROLL)`

Defines the total weight of the character.

