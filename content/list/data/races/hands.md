+++
date = "2016-08-01"
title = "HANDS (Data: races.lst)"
original_url = "list/data/races.html#hands"
categories = [ "all-tag", "races-tag" ]
+++

## Status

None

## Syntax

`HANDS:x`

## Parameters

-   x: Number (Number of Hands)



What it does
------------

-   Determines the Number of Hands the creature has for purposes of
    Multiattack and Multidexterity.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `HANDS` tag, the data included in a new `HANDS` tag will
    overwrite the existing tag data.

Example
-------

`HANDS:4`

Race has four hands.

**.MOD Example:**

Initial Race: `<race name> <tab> HANDS:2`

Modified By: `<race name>.MOD <tab> HANDS:4`

Is Equivalent To: `<race name> <tab> HANDS:4`

Race now has four hands.

