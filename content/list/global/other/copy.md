+++
date = "2016-08-01"
title = "COPY (Global: OTHER)"
original_url = "list/global/other.html#copy"
categories = [ "all-tag", "other-tag" ]
+++

## Status

Updated 5.13

## Syntax

`w|x.COPY=y`

## Parameters

-   w: CATEGORY=Text (Ability category. Used only when
    copying abilities.)
-   x: Text (Object name)
-   y: Text (Copied object's name)



The .COPY Tag
-------------

What it does
------------

-   Copies a LST object, creating a new object with the same properties
    as the original object.
-   When copying abilities you reference the ability by its
    "category", i.e. `CATEGORY=<category>` , and its name, or "key".
-   The name of the object must match EXACTLY the existing object, i.e.
    case sensitive.
-   Copying a "class" requires that the object include the beginning
    `CLASS:` tag.
-   Tags following the `.COPY` line modify the new object in the same
    way the `.MOD` tag modifies objects.
-   Any tags that follow the `.COPY` tag are added to the list of tags
    already in the object.
-   If only one tag is allowed, such as `HD` for classes or `COST` in
    equipment, the new tag will replace the tag in the original entry.
-   If more than one tag is allowed, most notably `BONUS` statements,
    then the new tag will be added to the other tags in the object.
-   The order of operations is: Native line, `COPY` , `MOD` , then
    `FORGET` , but the order of operation is also controlled by the
    `RANK` tag in the PCC file.
    -   Given: `1.MOD``1.FORGET``2.COPY``2.Blank``2.MOD``3.MOD`
    -   Order of processing is:
        `2.Blank``2.COPY``1.MOD``2.MOD``3.MOD``1.FORGET`

Note: When copying a Class it is important to remember that while the
class lines are copied into a new class, there remain tags in those
lines which refer to the original class by name. The effect of this is
that your new class will not inherit any class abilities that reference
the old class name, e.g. Spellcasting, Favored Enemies, etc.

Examples
--------

`Human.COPY=Aboriginee`

Creates a new race called Aboriginee based on the Human race.

`Dagger.COPY=Hunting Knife`

Creates a new weapon called Hunting Knife based on the weapon Dagger.

`CLASS:Ranger.COPY=Woodsman`

Creates a new class called the Woodsman based on the Ranger class.

`Skill Focus.COPY=Heighten Knowledge`

Creates a new feat called Heighten Knowledge based on the Skill Focus
feat.

`CATEGORY=(foo)|(key).COPY`

The new syntax to be used to `.COPY` an ability.

