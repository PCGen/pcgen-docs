+++
date = "2016-08-01"
title = "Race Files"
original_url = "/list/data/races.html"

[menu.main]
    identifier = "data_races"
    name = "Race Files"
    parent = "data"
    
+++
The "Name" of the race must be the first field on each line, the
remaining tags may be of any order.

`Boar (Wild Pig)`

The race named "Boar (Wild Pig)" is to be created.

`Bugbear.COPY=Bugbear (Shadowkind)`

Copies the race named "Bugbear" to a new race called "Bugbear
(Shadowkind)".

`Shark (Huge).MOD`

The race named "Shark (Huge)" is to be modified.

If you want to get rid of **racex** in your campaign, better put
`racex.           FORGET     ` in one of your **RACE** files. That will
remove **racex** from your campaign. In fact you won't even be able to
use the name **racex** for a new race in your campaign. If you want to
do so later you will need to use the [.MOD](/list/global/other/mod.html)
tag.

`Shark (Huge).FORGET`

The race named "Shark (Huge)" is to be forgotten.

------------------------------------------------------------------------

Race File Tag Dictionary
------------------------

------------------------------------------------------------------------

