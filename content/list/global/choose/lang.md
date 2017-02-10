+++
date = "2016-08-01"
title = "LANG (Global: CHOOSE)"
original_url = "/list/global/choose.html#lang"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "LANG"
    parent = "global_choose"
    identifier = "global_choose_LANG"
+++

## Status

New 5.17.4

## Syntax

`CHOOSE:LANG|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Language name)
-   x: FEAT=Text (Feat, by name or key)
-   x: LANGBONUS
-   x: TYPE=Text (Language type)
-   x: !TYPE=Text (Prohibited language type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED



What it does
------------

-   This presents a list of languages for selection.
-   Use of the `FEAT` sub-tag will provide the language selected by the
    referenced feat. The feat referenced must contain a
    `CHOOSE:LANG` tag.
-   Use of `LANBONUS` will provide a list of languages granted to the
    character by the `LANGBONUS` tag through the character's race, class
    or template.
-   Global qualifiers work for languages. Use of the qualifiers has the
    following effect:
    -   **ANY** - Will return a list of all languages.
    -   **PC** - Will return a list of all languages already taken by
        the Player Character.
    -   **QUALIFIED** - Will return a list of all languages that the
        player character is otherwise qualified for.
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

`CHOOSE:LANG|Common|Goblin`

Presents the "Common" and "Goblin" languages for selection.

`CHOOSE:LANG|Common,Goblin`

No languages are presented as no language is both "Common" and "Goblin".

`CHOOSE:LANG|Common|TYPE=Foo,PC`

Presents the "Common" language and any languages that have the "Foo"
type which are already selected by the Player Character.

Ability, Domain, Feat, Race, and Template files.

