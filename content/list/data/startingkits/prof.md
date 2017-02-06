+++
date = "2016-08-01"
title = "PROF (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#prof"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "PROF (Data: starting_kits.lst)"
    parent = "startingkits"
+++

## Status

None

## Syntax

`PROF:x`

## Parameters

-   x: Text (Proficiency name)



What it does
------------

-   Presents a pipe-delimited (|) list of weapon proficiencies for the
    character to choose from.
-   If the `RACIAL:YES` tag is included on the line, PCGen will fill any
    racial bonus proficiency choices first, otherwise it will try to
    fill any class bonus proficiency choices. If there are any choices
    left they will be granted as bonus proficiencies.

Example
-------

`PROF:Greataxe`

Would give a proficiency in the use of "Greataxe" if the PC can afford
it.

`PROF:Longsword <tab> RACIAL:YES`

Would select Longsword as the bonus proficiency choice if the character
can legally select that choice.

`PROF:Longbow|Shortbow`

Would grant the choice of Longbow or Shortbow as a bonus proficiency.

