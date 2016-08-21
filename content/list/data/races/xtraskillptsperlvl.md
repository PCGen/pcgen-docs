+++
date = "2016-08-01"
title = "XTRASKILLPTSPERLVL (Data: races.lst)"
original_url = "list/data/races.html#xtraskillptsperlvl"
categories = [ "all-tag", "races-tag" ]
+++

## Status

Updated Syntax 6.03.02

## Syntax

`XTRASKILLPTSPERLVL:x`

## Parameters

-   x: Number, Variable, or Formula



What it does
------------

Grants a number of skill points to the race for free at every character
level. This happens before multiplication of the first class level's
skill points.

<span class="lstwarning"> Warning: </span> Use of this tag on levels
greater than first level will lead to unexpected behavior.

Example
-------

`XTRASKILLPTSPERLVL:1`

Adds one to the skill points per level (before multiplication for the
1st level).

`XTRASKILLPTSPERLVL:HumanSkillBase`

Adds a number of skill points per level (before multiplication for the
1st level) equal to the value of the variable "HumanSkillBase"".

**.MOD Example:**

Initial Race: `<race name> <tab> XTRASKILLPTSPERLVL:1`

Modified By: `<race name>.MOD <tab> XTRASKILLPTSPERLVL:2`

Is Equivalent To: `<race name> <tab> XTRASKILLPTSPERLVL:2`

The final extra skill points per level are "2".

