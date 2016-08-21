+++
date = "2016-08-01"
title = "CLEAR (Global: OTHER)"
original_url = "list/global/other.html#clear"
categories = [ "all-tag", "other-tag" ]
+++

## Status

None

## Syntax

`x.CLEAR.y`

## Parameters

-   x: Text (Tag to be cleared)
-   y: Text (Name of object being cleared, Optional))



The .CLEAR Tag
--------------

What it does
------------

-   This tag is used in conjunction with the `.MOD` and `.COPY` tags and
    may not be used for "Run-Time" changes.
-   This tag is also useful in CLASS lines. See
    [SAB](/list/global/other/sab.html) tag documentation.
-   Tags that can have multiple items, such as `TYPE` , or tags that can
    be used multiple times can be eliminated.
-   The `.CLEAR` syntax has not yet been standardized as many of the
    other tags have been and there are at least 2 variations on how it
    can be used.

Note: Although listed as global, `.CLEAR` will not work with all tags.
Some experimentation may be required to see which usage is required with
which tags.

**Syntax usage:**

`TAG:.CLEAR`

This syntax clears all the values of the original object. This tag is
followed by a second tag which sets the new values. It is important to
note that PCGen works in a sequential manner and if the two tags order
is swapped the new value will be cleared as well as the original values.

`TAG:.CLEAR.<Values to be cleared>`

The items which follow the `.CLEAR.` are cleared.

**Work Arounds:**

`.CLEAR` is not supported on the `CHOICE` tag, allowing the removal of
the tag from the item. Two ways to do that are:

-   `MULT:NO` - makes it a single feat, choice not supported.
-   `CHOOSE:NOCHOICE` - no popup, but selectable multiple times.

Examples
--------

`CLASS:Ranger.MOD <tab> CSKILL:.CLEAR.Animal Empathy`

Modifies the <span class="lstobj"> Ranger </span> class by eliminating
the <span class="lstobj"> Animal Empathy </span> skill from its class
skill list.

> `Dagger.COPY=Hunting Knife <tab> TYPE:.CLEAR <tab> TYPE:Weapon.Melee.Finesseable.Exotic.Standard.Piercing.Slashing.Dagger`

Creates a new weapon called <span class="lstobj"> Hunting Knife </span>
, clears ALL the types from the new weapon and then adds back the
desired types.

`Acid Arrow.MOD <tab> SCHOOL:.CLEAR <tab> SCHOOL:Lesser Conjuration`

Modifies the Acid Arrow spell by eliminating the original value of the
`SCHOOL` tag and then sets the new value with a second `SCHOOL` tag.

Where it is Used
----------------

In conjunction with `.MOD` and `.COPY`

