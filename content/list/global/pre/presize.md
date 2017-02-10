+++
date = "2016-08-01"
title = "PRESIZE (Global: PRErequisite)"
original_url = "/list/global/pre.html#presize"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRESIZE"
    parent = "global_pre"
    identifier = "global_pre_PRESIZE"
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="presize"></span>

### PRESIZE

Require the character is a particular size category, or in a particular
range of size categories.

#### Status

#### Syntax

`PRESIZEoperator:size`

`operator` is a comparison operator from the list `EQ` , `LT` , `LTEQ` ,
`GT` , `GTEQ` , or `NEQ` . The comparison operator is written as part of
the tag name, i.e. `PRESIZELTEQ` . See [comparison
operators](/list/global/pre.html#comparison-operators)\
 for more details.

The `operator` is written as part of the tag name, i.e. `PRESIZENEQ` or
`PRESIZEGTEQ` .

`size` is one of the `SIZENAME` s defined in the "game mode", i.e.
`/system/gameModes/35e/sizeAdjustment.lst` . For the `35e` game mode the
`SIZENAMES` are:

-   `F` - fine
-   `D` - diminutive
-   `T` - tiny
-   `S` - small
-   `M` - medium
-   `L` - large
-   `H` - huge
-   `G` - gargantuan
-   `C` - colossal
-   `P` - larger than colossal

#### Examples

1.  `PRESIZEGTEQ:S`

    Require the character is at least small-sized.

2.  `PRESIZELT:S`

    Require that the character is fine, diminutive, or tiny.

3.  `PREMULT:2,[PRESIZEGTEQ:S],[PRESIZELTEQ:L]`

    Require the character to be small, medium, or large.

    Alternately, `PREMULT:1,[PRESIZEEQ:S],[PRESIZEEQ:M],[PRESIZEEQ:L]`
    would do the same thing.



