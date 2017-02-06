+++
date = "2016-08-01"
title = "TEMPLATE (Global: CHOOSE)"
original_url = "/list/global/choose.html#template"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "TEMPLATE (Global: CHOOSE)"
    parent = "choose"
+++

## Status

New 5.17.4

## Syntax

`CHOOSE:TEMPLATE|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Template Name or Key)
-   x: FEAT=Text (Feat, by name or key)
-   x: TYPE=Text (Template Type)
-   x: !TYPE=Text (Template Type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED



What it does
------------

-   This presents a list of templates for selection.
-   Use of the `FEAT` sub-tag will provide a list of templates selected
    by the referenced feat. The feat referenced must contain a
    `CHOOSE:TEMPLATE` tag.
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

`CHOOSE:TEMPLATE|Mindless|Undead`

Presents the "Mindless" and "Undead" templates for selection.

`CHOOSE:TEMPLATE|Mindless,Undead`

No templates are presented as no template is both "Mindless" and
"Undead".

`CHOOSE:TEMPLATE|Mindless|TYPE=Foo,PC`

Presents the "Mindless" template and any templates that have the "Foo"
type which are already selected by the Player Character.

`CHOOSE:TEMPLATE|Mindless|PC[TYPE=Foo]`

Presents the "Mindless" template and any templates that have the "Foo"
type which are already selected by the Player Character.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

