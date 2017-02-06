+++
date = "2016-08-01"
title = "QUALIFY (Global: OTHER)"
original_url = "/list/global/other.html#qualify"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "QUALIFY (Global: OTHER)"
    parent = "other"
+++

## Status

Updated 5.11.7

## Syntax

`QUALIFY:x|y|y`

## Parameters

-   x: ABILITY=Text (Ability category)
-   x: CLASS
-   x: DEITY
-   x: DOMAIN
-   x: EQUIPMENT
-   x: EQMOD
-   x: FEAT
-   x: RACE
-   x: SPELL
-   x: SKILL
-   x: TEMPLATE
-   x: WEAPONPROF
-   y: Text (Object KEY)



What it does
------------

Counters PRExxx tags checking for the listed objects. Any objects listed
will ignore all PRE tags and be a valid selection for the character.

Example
-------

`QUALIFY:ABILITY=FEAT|Mounted Combat|Ride-By Attack`

The character would be able to take the above feats whether they meet
the prereqs or not.

`QUALIFY:FEAT|Mounted Combat|Ride-By Attack`

The character would be able to take the above feats whether they meet
the prereqs or not.

`QUALIFY:CLASS|Monk`

The character would be able to take the Monk class whether they meet the
prereqs or not.

`QUALIFY:CLASS|Battle Mind|Telepath`

The character would be able to take either the Battle Mind or Telepath
class whether they meet the prereqs or not.

Where it is used
----------------

Valid in most objects except .pcc files and class level lines.

