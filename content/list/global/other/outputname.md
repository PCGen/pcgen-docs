+++
date = "2016-08-01"
title = "OUTPUTNAME (Global: OTHER)"
original_url = "list/global/other.html#outputname"
categories = [ "all-tag", "other-tag" ]
+++

## Status

Updated 5.9.5

## Syntax

`OUTPUTNAME:x`

## Parameters

-   x: Text (Name to appear on the output sheet)
-   x: \[NAME\] (This is replaced by anything in
    parenthesis on output)



What it does
------------

-   Alters the name of the object when output.
-   The `[NAME]` tag, when used, will be replaced by the parenthetical
    text in the object's name.
-   If the `[NAME]` tag is used where there is no parenthetical text the
    object name itself is output.

This tag is used when the name you wish to appear on the output sheet
contains symbols that might interfere with the program. It also helps to
keep the list orderly as you can group a series of objects like scrolls
and potions together without sacrificing the preferred name of the
object.

Example
-------

`OUTPUTNAME:Jason's [NAME]`

LST entry "Magic Spell" will output as "Jason's Magic Spell"

`OUTPUTNAME:[NAME] Elf`

LST entry "Elf (Gray)" will output as "Gray Elf".

`OUTPUTNAME:Huge Water Elemental`

LST entry "Elemental (Water/Huge)" will output as "Huge Water
Elemental".

`OUTPUTNAME:Formian [NAME]`

LST entry "Formian (Queen)" will output as "Formian Queen".

`OUTPUTNAME:Potion of [NAME]`

LST entry "Potion (Glibness)" will output as "Potion of Glibness".

`Clenched Fist.MOD <tab> OUTPUTNAME:Big [NAME]`

This spell will output as "Big Clenched Fist".

