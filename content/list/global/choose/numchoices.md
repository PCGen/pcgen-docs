+++
date = "2016-08-01"
title = "NUMCHOICES (Global: CHOOSE)"
original_url = "list/global/choose.html#numchoices"
categories = [ "all-tag", "choose-tag" ]
+++

## Status

None

## Syntax

`NUMCHOICES=x`

## Parameters

-   x: Number or Formula (Maximum number of total
    selections that can be taken)



<span id="numchoices"></span>

What it does
------------

-   Sets the total number of choices that can be made by taking a
    particular feat multiple times.
-   Used in conjunction with the MULT tag.
-   When used in conjunction with the `SELECT` tag, the NUMCHOICES value
    should equal a multiple of the SELECT value.

Example
-------

`CHOOSE:NUMCHOICES=3|SKILLSNAMED|Spot|Listen|Search`

The user can select the same choice more than once, but the user will
never be allowed more than 3 choices total, each made one at a time.

`CHOOSE:NUMCHOICES=6|SKILLSNAMED|Craft%|3`

The user can select this chooser multiple times and will be allowed to
select up to 3 Craft subskills each time the chooser is selected, but
may only make 6 Craft subskill sellection total.

`CHOOSE:NUMCHOICES=3|SKILLSNAMED|TYPE=Strength|TYPE=Dexterity|TYPE=Constitution|TYPE=Intelligence|TYPE=Wisdom`

The user will be allowed to select one skill from "Strength" "Dexterity"
"Constitution" "Intelligence" and "Wisdom" skills each time the chooser
is taken but is limited to a maximum of three such selections through
this chooser.

`SELECT:3 <tab> CHOOSE:NUMCHOICES=6|SKILLSNAMED|TYPE=Knowledge`

The user can select three (3) "Knowledge" type skills each time he takes
the associated feat but may take no more than six (6) "Knowledge" type
skills total no matter how many times the feat is taken.

`CHOOSE:NUMCHOICES=3|NOCHOICE`

A feat, or ability, containing this tag may be applied three times, with
no CHOOSER window being displayed, as long as there is no `SELECT` tag
included giving more than 1 choice per feat application.

