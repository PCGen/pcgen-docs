+++
date = "2016-08-01"
title = "AUTOEQUIP (Global: OTHER)"
original_url = "/list/global/other.html#autoequip"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "AUTOEQUIP"
    parent = "global_other"
    identifier = "global_other_AUTOEQUIP"
+++

## Status

New 5.17.11

## Syntax

`AUTO:EQUIP|x|x`

## Parameters

-   x: Text (&lt;Equipment Name&gt;)



What it does
------------

-   This is a pipe-delimited (|) list of equipment that is granted to
    the character for free.
-   PRExxx tags are allowed with this tag and use the pipe-delimited (|)
    syntax.
-   `AUTO:EQUIP` won't take (%)LIST or (%)CHOICE for substitution.

**NOTE:** The equipment added is marked on the GUI just as feats added
by the `AUTO:FEAT` tag, i.e. are yellow, and can't be removed.
Additionally, the equipment must be added to the Equipment Set just as
any other Equipment the PC has to come out on the OS.

**CAUTION:** Some trouble has been found when attempting to add two of
the same item. Additionally, you should not use items which have math
operators (such as + and -) in their names.

Where it is used
----------------

Global, however AUTO:EQUIP is not supported in class level lines. It can
be used on a class line.

Examples
--------

`AUTO:EQUIP|Flurry of Blows|PRECLASS:1,Monk=1|`

The item "Flurry of Blows" is granted as a free equipment item if the
character has a level of Monk.

`AUTO:EQUIP|Flurry of Blows|PREMULT:2,[PRESTAT:1,DEX=15],[PRECLASS:1,Monk=1]`

The item "Flurry of Blows" is granted as a free equipment item if the
character has a level of Monk and a DEX score of 15 or better.

