+++
date = "2016-08-01"
title = "NOCHOICE (Global: CHOOSE)"
original_url = "list/global/choose.html#nochoice"
categories = [ "all-tag", "choose-tag" ]
+++

## Status

New 5.9.4

## Syntax

`CHOOSE:NOCHOICE`

## Parameters




What it does
------------

-   Suppresses the pop-up window for this CHOOSE tag.
-   `MULT:YES` must be used when using this tag.
-   When used in a feat, this tag will simply add the feat to the
    character without a chooser window. After the first time it is
    added, a "(x2)", "(x3)" etc. will be displayed, indicating the
    number of times the feat was chosen.
-   When used for a "nested" choice, the "outer" choice isn't displayed.
    Example: Given feats "X" and "Y" where feat "X" includes the
    `ADD:FEAT|Y` tag and feat "X" also includes a `CHOOSE` tag, the feat
    "X(Y)" is displayed in the chooser. With this option it will show up
    as "Y".

Example
-------

`CHOOSE:NOCHOICE`

The feat is added without a chooser window.

Ability, Domain, Feat, Race, and Template files.

