+++
date = "2016-08-01"
title = "FAVCLASS (Data: races.lst)"
original_url = "/list/data/races.html#favclass"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "FAVCLASS"
    parent = "data_races"
+++

## Status

Updated 5.15.8

## Syntax

`FAVCLASS:x|x.y`

## Parameters

-   x: Text (Base class name)
-   x: ANY
-   y: Text (Base class or sub-class name)



What it does
------------

-   Determines the Race's favored class.
-   Classes with sub-classes must use the (x.y) syntax and must include
    the base-class name or the sub-class name.
-   More than one class may be included as a pipe-delimited (|) list
    with all listed classes identified as "Favored".
-   Special type 'ANY' will grant the character's highest level class
    as Favored.
-   When 'ANY' is used no other class is allowed.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `FAVCLASS` tag, the data included in a new `FAVCLASS`
    tag will overwrite the existing tag data.

Example
-------

`FAVCLASS:Wizard|Fighter`

The character's favored classes are "Wizard" (including any sub-class of
wizard) and "Fighter".

`FAVCLASS:Wizard.Wizard`

Race's favored class is "Wizard" (excluding any sub-class of wizard).

`FAVCLASS:Wizard.Illusionist`

Race's favored class is the "Wizard" sub-class, the "Illusionist".

**.MOD Example:**

Initial Race: `<race name> <tab> FAVCLASS:Wizard|Fighter`

Modified By: `<race name>.MOD <tab> FAVCLASS:Wizard.Illusionist`

Is Equivalent To: `<race name> <tab> FAVCLASS:Wizard.Illusionist`

Race's favored class is changed to "Wizard" sub-class, the
"Illusionist".

