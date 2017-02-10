+++
date = "2016-08-01"
title = "SHIELDPROFICIENCY (Global: CHOOSE)"
original_url = "/list/global/choose.html#shieldproficiency"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "SHIELDPROFICIENCY"
    parent = "global_choose"
+++

## Status

New 5.17.4

## Syntax

`CHOOSE:SHIELDPROFICIENCY|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Shield proficiency)
-   x: FEAT=Text (Feat, by name or key)
-   x: TYPE=Text (Shield proficiency type)
-   x: !TYPE=Text (Prohibited shield proficiency type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED
-   y: EQUIPMENT\[x\] (Special Qualifier)



What it does
------------

-   This will produce a list of all shield proficiencies matching
    the criteria.
-   Using the `FEAT=Text` sub-tag will provide a list of shield
    proficiencies selected by the referenced feat. The feat referenced
    must contain a `CHOOSE:SHIELDPROFICIENCY` tag.
-   When using the `EQUIPMENT` qualifier the parameters included inside
    the brackets are used to identify a list of equipment from which the
    shield proficiencies are taken and added to the final list of
    provided shield proficiencies. The criteria included in the
    brackets (\[x\]) are used to summarize shields and not
    shield proficiencies.
-   Global qualifiers work for shield proficiencies. Use of the
    qualifiers has the following effect:
    -   **ANY** - Will return a list of all shield proficiencies.
    -   **PC** - Will return a list of all shield proficiencies already
        taken by the Player Character.
    -   **QUALIFIED** - Will return a list of all shield proficiencies
        that the player character is otherwise qualified for.
-   Qualifiers can be logically negated by prefacing with the
    exclamation point (!), i.e. `!PC` is a valid usage.
-   Criteria can be logically combined by using the comma (,), logical
    **AND** , and the pipe (|), logical **OR** . Logical **AND** s are
    evaluated before logical **OR** s.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

Example
-------

`CHOOSE:SHIELDPROFICIENCY|TYPE=Foo`

Will display a list of proficiencies for all shield proficiencies of
type **Foo** .

`CHOOSE:SHIELDPROFICIENCY|Buckler|Tower Shield`

Will display no proficiencies as no shield will have both proficiencies
lisyted.

`CHOOSE:SHIELDPROFICIENCY|EQUIPMENT[Buckler]`

Will display a list the proficiencies for the Buckler.

`CHOOSE:SHIELDPROFICIENCY|EQUIPMENT`

Will display a list the shield proficiencies of all shields taken.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

