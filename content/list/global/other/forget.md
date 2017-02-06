+++
date = "2016-08-01"
title = "FORGET (Global: OTHER)"
original_url = "/list/global/other.html#forget"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "FORGET (Global: OTHER)"
    parent = "other"
+++

## Status

Updated 5.13

## Syntax

`w|x.FORGET`

## Parameters

-   w: CATEGORY=Text (Ability category. Used only when
    modifying abilities.)
-   x: Text (Object name or key)



The .FORGET Tag
---------------

What it does
------------

-   Completely removes a LST object from the loaded dataset.
-   When forgeting abilities you reference the ability by its
    "category", i.e. `CATEGORY=<category>` , and its name, or "key".
-   This tag has no other tags following it.
-   The name of the object must match EXACTLY the existing object, i.e.
    case sensitive.
-   Forgeting a "class" requires that the object include the beginning
    `CLASS:` tag.
-   The order of operations is: Native line, `COPY` , `MOD` , then
    `FORGET` , but the order of operation is also controlled by the
    `RANK` tag in the PCC file.
    -   Given: `1.MOD``1.FORGET``2.COPY``2.Blank``2.MOD``3.MOD`
    -   Order of processing is:
        `2.Blank``2.COPY``1.MOD``2.MOD``3.MOD``1.FORGET`

Examples
--------

`Human.FORGET`

Removes the Human race (in a race.lst file)

`Dagger.FORGET`

Removes the Dagger weapon (in equipment.lst file)

`CLASS:Ranger.FORGET`

Removes the Ranger class (in class.lst)

`Skill Focus.FORGET`

Removes the Skill Focus feat (in feat.lst)

`CATEGORY=(foo)|(key).FORGET`

The new syntax to be used to .FORGET an ability.

