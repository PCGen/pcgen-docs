+++
date = "2016-08-01"
title = "NUMBER (Global: CHOOSE)"
original_url = "/list/global/choose.html#number"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "NUMBER (Global: CHOOSE)"
    parent = "choose"
+++

## Status

None

## Syntax

`CHOOSE:NUMBER|x|y|z`

## Parameters

-   x: MIN=Number (Lowest value to choose from)
-   y: MAX=Number (Highest value to choose from)
-   z: TITLE=Text (Description to output to
    the chooser)



<span id="number"></span>

What it does
------------

-   Allows the selections of a number between the high and low values,
    inclusive
-   Unlike other `CHOOSE` tags, `MULT:YES` is not to be used with
    `CHOOSE:NUMBER` .
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

**Note:** This will only bring up the chooser if invoked from the
Temporary Bonus tab.

Example
-------

`CHOOSE:NUMBER|MIN=2|MAX=5|TITLE=Roll 1d4+1 and pick a number`

Will let you choose a number between 2 and 5. (Simulates rolling 1d4+1).

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

