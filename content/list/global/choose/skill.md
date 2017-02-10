+++
date = "2016-08-01"
title = "SKILL (Global: CHOOSE)"
original_url = "/list/global/choose.html#skill"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "SKILL"
    parent = "global_choose"
    identifier = "global_choose_SKILL"
+++

## Status

Updated 6.03.04

## Syntax

`CHOOSE:SKILL|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Skill name or key)
-   x: Text% (Search pattern by skill name or key)
-   x: FEAT=Text (Feat, by name or key)
-   x: TYPE=Text (Skill type)
-   x: !TYPE=Text (Prohibited skill type)
-   x: ALL
-   y: ANY (Default)
-   y: QUALIFIED
-   y: USEUNTRAINED
-   y: CLASS
-   y: CROSSCLASS
-   y: EXCLUSIVE
-   y: NORANK
-   y: RANKS=number (Skill ranks)



What it does
------------

-   This will produce a list of skills matching the stipulated criteria.
-   Using the percent sign (%) following a skill name forms a search
    pattern that will provide a list of skills that match the partial
    name provided.
-   Using the `FEAT=Text` sub-tag will provide a list of skills chosen
    by the referenced feat. The feat referenced must contain a
    `CHOOSE:SKILL` tag.
-   Using the `CLASS` sub-tag will provide a list of all class skills
    for the PC.
-   Using the `CROSSCLASS` sub-tag will provide a list of all crossclass
    skills for the PC.
-   Using the `EXCLUSIVE` sub-tag will provide a list of all exclusive
    skills for the PC.
-   Using the `NORANK` sub-tag will provide a list of all skills in
    which the PC has no rank.
-   Using the `RANKS=n` sub-tag will provide a list of all skills in
    which the PC has n or more ranks.
    -   The special value `MAXRANK` can be used with the `RANKS`
        qualifier to identify skills that are currently at the maximum
        ranks allowed.
-   Global qualifiers work for feats. Use of the qualifiers has the
    following effect:
    -   **ANY** - Will return a list of all skills.
    -   **QUALIFIED** - Will return a list of all skills that the player
        character is otherwise qualified for.
    -   **USEUNTRAINED** - Will return a list of all skills that the
        player character can use intrained.
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

`CHOOSE:SKILL|Search|Spot`

Will display a list of skills comprised of the **Search** and **Spot**
skills.

`CHOOSE:SKILL|CLASS`

This will produce a list of all the character's class skills.

`CHOOSE:SKILL|RANKS=1`

This will produce a list of all skills the character's has one or more
ranks in.

`CHOOSE:SKILL|!RANKS=MAXRANK`

This will produce a list of all skills the character's has that are not
at the maximum ranks allowed.

`CHOOSE:SKILL|Knowledge%`

This will produce a list of all knowledge skills.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files. For the eqmod version
see [CHOOSE:ABILITY (Equipment
Modifiers)](/list/data/equipmentmodifiers/chooseskill.html)

