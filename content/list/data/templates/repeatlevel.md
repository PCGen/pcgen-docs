+++
date = "2016-08-01"
title = "REPEATLEVEL (Data: templates.lst)"
original_url = "/list/data/templates.html#repeatlevel"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "REPEATLEVEL (Data: templates.lst)"
    parent = "templates"
+++

## Status

Updated 5.11.13

## Syntax

`REPEATLEVEL:v|w|x:y:z`

## Parameters

-   v: Number (Levels per interval)
-   w: Number (Number of intervals before skipping one
    interval, use 0 for no skip)
-   x: Number (Maximum level)
-   y: Number (Minimum level)
-   z: Text (Tag to be repeated)



What it does
------------

-   Repeats the application of the specified tag to the character on the
    intervals specified.
-   If you specified "Levels per Interval" as 3 ("v") beginning at level
    one ("y"), the line would repeat again at levels 4, 7, 10, etc...
-   Continuing the above example, if you specified skipping an interval
    every two (2) intervals ("w"), the line would repeat at levels 4,
    10, 13, 19, 22, 28, etc...
-   "x" specifies the level at which the progression ends.
-   "y" specifies the level at which the progression starts.
-   "z" specifies the tag which provides the benefit granted by the
    REPEATELEVEL tag.
-   Valid tags to be used as part o the REPEATELEVEL tag are: `SR` ,
    `SAB` , `DR` , `CR` , and `FEAT` , each with its own suntax and
    parameter requirements.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `REPEATLEVEL` tag, the data included in a new
    `REPEATLEVEL` tag will be included as if it were a separate tag.

Example
-------

`<Template Name> <tab> REPEATLEVEL:5|4|20:1:FEAT(ABonusFeat)`

Would add "ABonusFeat" at levels 5, 10, 15, and 20.

`<Template Name> <tab> REPEATLEVEL:1|0|20:1:FEAT(ABonusFeat)`

Would add "ABonusFeat" at levels 1, 2, 3, 5, 6, 7, 9, 10, 11, 13, 14,
15, 17, 18, and 19.

`<Template Name> <tab> REPEATLEVEL:2|1|20:2:FEAT(ABonusFeat)`

Would add "ABonusFeat" at levels 2, 4, 6, 8,... up to level 20.

`Drow Male <tab> REPEATLEVEL:1|0|10:1:FEAT(AWizardFeat) <tab> PRERACE:Elf (Drow) <tab> SUBRACE:Male <tab> GENDERLOCK:Male`

Would add "AWizardFeat" at levels 1, 2, 3, 5, 6, 7, 9, and 10.

**.MOD Example:**

Initial Template:
`Advanced Werewolf <tab> REPEATLEVEL:5|4|20:1:FEAT(ABonusFeat)`

Modified By:
`Advanced Werewolf.MOD <tab> REPEATLEVEL:2|1|20:2:FEAT(ABonusFeat)`

Is Equivalent To:
`Advanced Werewolf <tab> REPEATLEVEL:5|4|20:1:FEAT(ABonusFeat)          <tab> REPEATLEVEL:2|1|20:2:FEAT(ABonusFeat)`
.

The Advanced Werewolf gains a bonus feat at levels 2, 4, 5, 6, 8, 12,
14, 15, 16, and 18, and gains two bonus feats at levels 10 and 20.

