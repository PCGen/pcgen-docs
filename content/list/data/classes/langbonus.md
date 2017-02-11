+++
date = "2016-08-01"
title = "LANGBONUS (Data: classes.lst)"
original_url = "/list/data/classes.html#langbonus"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "LANGBONUS"
    parent = "data_classes"
    identifier = "data_classes_LANGBONUS"
+++

## Status

None

## Syntax

`LANGBONUS:x,x`

## Parameters

-   x: Text (Languages)
-   x: TYPE=Text (Language Type)
-   x: Text ('Any')
-   x: .CLEAR



What it does
------------

This is a comma (,) delimited list of the languages a character can
choose from based upon their Intelligence stat.

When using 'Any', no other language designation is necessary.

Examples
--------

`LANGBONUS:Draconic`

The class can choose "Draconic" as one of their languages.

`LANGBONUS:Draconic,Elven`

The class can choose "Draconic" or "Elven" as one of their languages.

`LANGBONUS:ALL`

The class can choose any language loaded from sources as one of their
languages.

`LANGBONUS:TYPE=Written`

The class can choose any written language as one of their languages.

`LANGBONUS:TYPE=Spoken,Draconic`

The class can choose any written language or "Draconic" as one of their
languages.

`LANGBONUS:.CLEAR,Dwarven,Gnomish,Orcish`

The class has all bonus languages cleared then can choose "Dwarvish",
"Gnomish" or "Orcish" as one of their languages.

Where it is used
----------------

Class Level Line.

