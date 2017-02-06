+++
date = "2016-08-01"
title = "RACENAME (System: bio/biosettings.lst)"
original_url = "/list/system/biosettings.html#racename"
categories = [ "all-tag", "biosettings-tag" ]
[menu.main]
    name = "RACENAME (System: bio/biosettings.lst)"
    parent = "biosettings"
+++

## Status

None

## Syntax

`RACENAME:x`

## Parameters

-   x: Text (The name of the race)



What it does
------------

Defines the name of the race. Will appear under every AGESET tag. If the
name is followed by a "%" symbol then that BIOSET will apply to all
subsets of that race name. For example `RACENAME:Elf%` will apply to Elf
(Drow), Elf (Wood) and all other Elf races. Without the "%" symbol the
age set will apply only to the race that matches the name exactly, so
`RACENAME:Elf (House)` will only be used by the race "Elf (House)".
Using parenthesis in combination with the "%" symbol will not work at
all. BIOSET entries for specific subset races will override a general
BIOSET entry of the same race.

Example
-------

`RACENAME:Human%`

The race name is "Human" and the BIOSET will apply to all subsets of the
Human race.

`RACENAME:Elf (Drow)`

The race name is "Elf (Drow)" and the BIOSET will apply only to the race
"Elf (Drow)".

