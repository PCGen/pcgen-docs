+++
date = "2016-08-01"
title = "LANGUAGE (Global: ADD)"
original_url = "list/global/add.html#language"
categories = [ "all-tag", "add-tag" ]
+++

## Status

New 5.11.11

## Syntax

`ADD:LANGUAGE|x|y,y`

## Parameters

-   x: Number, Variable or Formula (Number of
    choices granted. Optional)
-   y: Text (Language name)
-   y: TYPE=Text (Language type)
-   y: ALL



What it does
------------

-   Will add a number (x) of languages from the presented list of
    feats (y) to the characters list of known languages.
-   This is a comma-delimited (",") list of languages that the character
    can choose from.
-   Valid language types are "Spoken", "Written", or "Read".

Example
-------

`ADD:LANGUAGE|Draconic,Elven,Undercommon`

Add "Draconic", "Elven" or "Undercommon" to the list of languages known.

`ADD:LANGUAGE|2|TYPE=Spoken`

Adds two of any spoken type languages to the list of languages known.

`ADD:LANGUAGE|2|TYPE=Imperial,TYPE=Infernal`

Adds two of any Imperial or Infernal type languages to the list of
languages known.

`ADD:LANGUAGE|2|ALL`

Adds two of any language to the list of languages known.

