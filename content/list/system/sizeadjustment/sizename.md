+++
date = "2016-08-01"
title = "SIZENAME (System: sizeAdjustment.lst)"
original_url = "list/system/sizeadjustment.html#sizename"
categories = [ "all-tag", "sizeadjustment-tag" ]
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="sizename"></span>

### SIZENAME

Identifies a creature size category.

Each line of the `sizeAdjustment.lst` file **MUST** begin with a
`SIZENAME` tag. Features are added to the category by adding sub-tags
after the `SIZENAME` , such as `BONUS` tags.

The same `SIZENAME` may appear on multiple lines. The tokens following
the `SIZENAME` are appended to any tokens for the same `SIZENAME` on
preceding lines.

#### Status

New in 5.10.1.

#### Syntax {#syntax-2}

`SIZENAME:size_name` , where `size_name` is a single letter, i.e. `S` ,
`M` , `L` . This is the current standard for all game modes included in
PCGen.

Alternately, `size_name` may be a single word such as `Small` , `Medium`
, `Large` , etc.

**Example:**

`SIZENAME:F` defines a creature size named `F` . (This form is
preferred.)

`SIZENAME:Fine` defines a creature size `Fine` .

