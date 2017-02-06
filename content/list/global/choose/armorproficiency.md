+++
date = "2016-08-01"
title = "ARMORPROFICIENCY (Global: CHOOSE)"
original_url = "/list/global/choose.html#armorproficiency"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "ARMORPROFICIENCY (Global: CHOOSE)"
    parent = "choose"
+++

## Status

New 5.17.4

## Syntax

`CHOOSE:ARMORPROFICIENCY|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Armor proficiency)
-   x: FEAT=Text (Feat, by name or key)
-   x: TYPE=Text (Armor proficiency type)
-   x: !TYPE=Text (Prohibited armor proficiency type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED
-   y: EQUIPMENT\[x\] (Special Qualifier)



What it does
------------

-   This will produce a list of all armor proficiencies matching
    the criteria.
-   Using the `FEAT=Text` sub-tag will provide a list of armor
    proficiencies selected by the referenced feat. The feat referenced
    must contain a `CHOOSE:ARMORPROFICIENCY` tag.
-   When using the `EQUIPMENT` qualifier the parameters included inside
    the brackets are used to identify a list of equipment from which the
    armor proficiencies are taken and added to the final list of
    provided proficiencies. The criteria included in the
    brackets (\[x\]) are used to summarize armor and not
    armor proficiencies.
-   Global qualifiers work for armor proficiencies. Use of the
    qualifiers has the following effect:
    -   **ANY** - Will return a list of all armor proficiencies.
    -   **PC** - Will return a list of all armor proficiencies already
        taken by the Player Character.
    -   **QUALIFIED** - Will return a list of all armor proficiencies
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

`CHOOSE:ARMORPROFICIENCY|TYPE=Heavy`

Will display a list of proficiencies for all heavy armors.

`CHOOSE:ARMORPROFICIENCY|Scale Mail|Chainmail`

Will display a list consisting of Scale Mail and Chainmail.

`CHOOSE:ARMORPROFICIENCY|EQUIPMENT[Chainmail]`

Will display a list the proficiencies for Chainmail.

`CHOOSE:ARMORPROFICIENCY|EQUIPMENT`

Will display a list the proficiencies of all equipment taken.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

