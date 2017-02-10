+++
date = "2016-08-01"
title = "FAVOREDCLASS (Data: templates.lst)"
original_url = "/list/data/templates.html#favoredclass"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "FAVOREDCLASS"
    parent = "data_templates"
    identifier = "data_templates_FAVOREDCLASS"
+++

## Status

None

## Syntax

`FAVOREDCLASS:x|x.y`

## Parameters

-   x: Text (Class name)
-   x: ANY
-   y: Text (Class or sub-class name)



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
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `FAVOREDCLASS` tag, the data included in a new
    `FAVOREDCLASS` tag will be appended to the existing tag data.

Example
-------

`FAVOREDCLASS:Wizard|Fighter`

The character's favored classes are "Wizard", including any of its
sub-classes, and "Fighter".

`FAVOREDCLASS:Wizard.Wizard`

The character's favored class is "Wizard", excluding any of its
sub-classes.

`FAVOREDCLASS:Wizard.Illusionist`

The character's favored class is the "Wizard" sub-class, the
"Illusionist".

`<template name>.MOD <tab> FAVOREDCLASS:Wizard.Necromancer`

The character's favored class is the "Wizard" sub-class, the
"Necromancer".

**.MOD Example:**

Initial Template: `Darkling <tab> FAVOREDCLASS:Sorcerer`

Modified By: `Darkling.MOD <tab> FAVOREDCLASS:Wizard.Necromancer`

Is Equivalent To:
`Darkling <tab> FAVOREDCLASS:Sorcerer|Wizard.Necromancer`

Darkling's "favored class" is the "Sorcerer" and the "Wizard" sub-class,
the "Necromancer".

