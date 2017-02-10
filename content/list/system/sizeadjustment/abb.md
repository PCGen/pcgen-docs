+++
date = "2016-08-01"
title = "ABB (System: sizeAdjustment.lst)"
original_url = "/list/system/sizeadjustment.html#abb"
categories = [ "all-tag", "sizeadjustment-tag" ]
[menu.main]
    name = "ABB"
    parent = "system_sizeadjustment"
    identifier = "system_sizeadjustment_ABB"
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="abb"></span>

### ABB

**Optional:** A one letter abbreviation of the size name.

#### Syntax

`ABB:X` , where `X` is a single letter.

#### Example

`SIZENAME:Fine  →  ABB:F` sets the abbreviation for the `Fine` size to
the letter `F` .

#### Notes

The `ABB` tag is implemented in
[code/src/java/plugin/lsttokens/sizeadjustment/AbbToken.java](https://github.com/PCGen/pcgen/blob/master/code/src/java/plugin/lsttokens/sizeadjustment/AbbToken.java)
.

