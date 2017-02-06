+++
date = "2016-08-01"
title = "AUTOLANG (Global: OTHER)"
original_url = "/list/global/other.html#autolang"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "AUTOLANG (Global: OTHER)"
    parent = "other"
+++

## Status

New 5.17.14

## Syntax

`AUTO:LANG|x|x`

## Parameters

-   x: Text (Language)
-   x: TYPE=Text (Language type)
-   x: !TYPE=Text (Language type)
-   x: ALL
-   x: %LIST
-   x: .CLEAR



What it does
------------

-   This is a pipe-delimited (|) list of languages, by name or type,
    that are granted as free language.
-   When including the `TYPE=` sub-tag you may use a
    period-delimited (.) list of language types. This will grant the
    character any Language with the listed types.
-   Use of `%LIST` will insert the result of a `CHOOSE` tag.
-   `.CLEAR` will clear all languages granted by previous
    `AUTO:LANG` tags.
-   PRExxx tags are allowed with this tag and use the pipe-delimited (|)
    syntax.

Examples
--------

`AUTO:LANG|Common`

Common is granted as a free language to the character.

`AUTO:LANG|TYPE=Latin`

Latin-type Languages are given as free languages .

`AUTO:LANG|Draconic|PREFEAT:1,Dodge`

The Draconic language is granted as a free language if the character has
the Dodge feat.

