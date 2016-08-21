+++
date = "2016-08-01"
title = "ADDLEVEL (Data: templates.lst)"
original_url = "list/data/templates.html#addlevel"
categories = [ "all-tag", "templates-tag" ]
+++

## Status

New 5.9.7

## Syntax

`ADDLEVEL:x|y`

## Parameters

-   x: Text (Class name)
-   y: Number or Formula (Number of levels to add)



What it does
------------

-   This tag will add the specified number of levels of the given class
    to the character the template is applied to.
-   The levels function as normal class levels in all ways except that
    they will be removed when the template is removed.
-   These levels will be added regardless of whether or not the
    character qualifies for the class in question.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `ADDLEVEL` tag, the data included in a new
    `ADDLEVEL` tag will be included as if it were a separate tag.

Example
-------

`ADDLEVEL:Animal|6`

Adds six levels of the Animal class to the character.

**.MOD Example (Included Separately):**

Initial Template: `Werewolf <tab> ADDLEVEL:Animal|2`

Modified By: `Werewolf.MOD <tab> ADDLEVEL:Animal|1`

Is Equivalent To:
`Werewolf <tab> ADDLEVEL:Animal|2 <tab> ADDLEVEL:Animal|1` .

The werewolf gains three levels in the class "Animal".

