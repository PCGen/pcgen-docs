+++
date = "2016-08-01"
title = "FAVCLASSCHOOSE (Data: races.lst)"
original_url = "/list/data/races.html#favclasschoose"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "FAVCLASSCHOOSE"
    parent = "data_races"
+++

## Status

Updated 5.15.8

## Syntax

`FAVCLASS:CHOOSE:x|x.y`

## Parameters

-   x: Text (Base class name)
-   x: ANY
-   y: Text (Base class or sub-class name)



What it does
------------

-   Determines the Race's favored class.
-   More than one class may be included, as a pipe-delimited (|) list,
    with all listws classes identified as "Favored".
-   Special type 'ANY' will grant the character's highest level class
    as Favored.
-   When 'ANY' is used no other class is allowed.

Example
-------

`FAVCLASS:CHOOSE:Wizard`

Race may select any sub-class of "Wizard" as the favored class.

`FAVCLASS:CHOOSE:Rogue|Wizard.Illusionist`

Race may select either "Rogue" or "Wizard" sub-class, "Illusionist", as
the favored class.

`FAVCLASS:CHOOSE:Wizard`

Race may select the "Wizard" base class or any of its sub-classes as the
favored class.

