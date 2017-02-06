+++
date = "2016-08-01"
title = "MOD (Global: OTHER)"
original_url = "/list/global/other.html#mod"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "MOD (Global: OTHER)"
    parent = "other"
+++

## Status

Updated 5.11.11 - 5.13

## Syntax

`w|x.MOD`

## Parameters

-   w: CATEGORY=Text (Ability category. Used only when
    modifying abilities.)
-   x: Text (Object name or key)



The .MOD Tag
------------

What it does
------------

-   Modifies an existing LST object.
-   `.MOD` is appended to the end of the first tag on an object line as
    follows:
    -   `<object name>.MOD` for dieties, domains, equipment (including
        weapons, armor, and shields), eqmods, feats, languages, race,
        skill, spell, and templates.
    -   `CLASS:<class name>.MOD` for classes.
    -   `CATEGORY=<category name>|<ability name or key>.MOD`
        for abilities.
-   The name of the object must match EXACTLY the existing object, i.e.
    case sensitive.
-   Any tags that follow the `.MOD` tag are added to the list of tags
    already in the object.
-   If only one tag is allowed, such as `HD` for classes or `COST` in
    equipment, the new tag will replace the tag in the original entry.
-   If more than one tag is allowed, most notably `BONUS` statements,
    then the new tag will be added to the other tags in the object.
-   When modifying an object to remove or replace a numerical `BONUS` ,
    you must duplicate the original `BONUS` with the number or formula
    used for the numerical bonus multiplied by "-1".
-   The order of operations is: Native line, `COPY` , `MOD` , then
    `FORGET` , but the order of operation is also controlled by the
    `RANK` tag in the PCC file.
    -   Given: `1.MOD``1.FORGET``2.COPY``2.Blank``2.MOD``3.MOD`
    -   Order of processing is:
        `2.Blank``2.COPY``1.MOD``2.MOD``3.MOD``1.FORGET`

<span id="modificationbehavior"></span> **Modification Behavior:**

When modifying a LST Object with the `.MOD` tag, there are four ways in
which tags are modified internally by PCGen: Modification by Overwriting
Data, Modification by Selective Overwriting, Modification by Appending
Data and Modification by Separate Tags. The behaviors are explained
below.

Modification by Overwriting Data

Initial LST Object: `<lst object> <tab> LSTFILETAG:A`

Modified By: `<lst object>.MOD <tab> LSTFILETAG:B`

Results In: `<lst object> <tab> LSTFILETAG:B`

Modification by Selective Overwriting Data

Initial LST Object: `<lst object> <tab> LSTFILETAG:A|A1`

Modified By: `<lst object>.MOD <tab> LSTFILETAG:A|A2`

Results In: `<lst object> <tab> LSTFILETAG:A|A2`

While

Initial LST Object: `<lst object> <tab> LSTFILETAG:A|A1`

Modified By: `<lst object>.MOD <tab> LSTFILETAG:B|B1`

Results In: `<lst object> <tab> LSTFILETAG:B|B1`

Modification by Appending Data

Initial LST Object: `<lst object> <tab> LSTFILETAG:A`

Modified By: `<lst object>.MOD <tab> LSTFILETAG:B`

Is Equivalent To: `<lst object> <tab> LSTFILETAG:A,B`

Modification by Separate LST Tags

Initial LST Object: `<lst object> <tab> LSTFILETAG:A`

Modified By: `<lst object>.MOD <tab> LSTFILETAG:B`

Is Equivalent To: `<lst object> <tab> LSTFILETAG:A <tab> LSTFILETAG:B`

But is Not Equivalent To: `<lst object> <tab> LSTFILETAG:A,B`

NOTE:The actual separator used in the equivalent syntax for each tag
will vary. Make sure you check the tag specific documentation to see an
example of that tags modification syntax.

Examples
--------

`Human.MOD`

Modifies the **Human** race (in a <span class="lstfile"> race.lst
</span> file)

`Dagger.MOD <tab> DESC:Short and pointy`

Replaces the description of the **Dagger** weapon (in <span
class="lstfile"> equipment.lst </span> file)

`CLASS:Ranger.MOD`

Modifies the **Ranger** class (in <span class="lstfile"> class.lst
</span> file)

`Acid Arrow.MOD <tab> OUTPUTNAME:My Acid Arrow`

Renames the **Acid Arrow** spell to **My Acid Arrow** (in a spells.lst
file)

`Resistance.MOD <tab> BONUS:CHECKS|Fortitude,Reflex,Will|1|TYPE=Resistance|PREAPPLY:ANYPC`

Adds a saving throw temporary bonus function to the **Resistance** spell

`CLASS:Arcane Archer.MOD <tab> BONUS:CHECKS|BASE.Will|-1*(CL/3) <tab> BONUS:CHECKS|BASE.Will|CL/2+2`

Modifies the **Arcane Archer** by first removing the original "Will"
bonus and then adding the new bonus.

`Skill Focus.MOD`

Modifies the **Skill Focus** feat ( <span class="lstfile"> in feat.lst
</span> file)

`BOWSTR.MOD`

Modifies the **BOWSTR** eqmod ( <span class="lstfile"> in eqmod.lst
</span> file)

`CATEGORY=Mutation|Weak Immune System.MOD`

Modifies an ability of the category "Mutation", which is called **Weak
Immune System** . Another ability of the same name, which belongs to
another category, would not be affected.

