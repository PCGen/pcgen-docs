+++
date = "2016-08-01"
title = "TEMPLATES (Data: templates.lst)"
original_url = "/list/data/templates.html"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "FEAT"
    parent = "data_templates"
    identifier = "data_templates_FEAT"
+++

## Status

None

## Syntax

`FEAT:x|x`

## Parameters

-   x: Text (Feat Name)



**Status:**

-   6.05.04 (July 2015): JIRA
    [NEWTAG-477](http://jira.pcgen.org/browse/NEWTAG-477) / Github [PR
    \#380](https://github.com/PCGen/pcgen/pull/380)
    -   The `FEAT` tag is deprecated. Use
        [`ABILITY`](/list/global/other/ability.html) instead.
    -   All `FEAT` tags have been **deprecated** and replaced by the
        `ABILITY` system, which is more general. The `ABILITY` system
        can model feats, racial features, class features, traits, flaws,
        temporary bonuses, and so on, all using a common format.

What it does
------------

-   This is a pipe-delimited (|) list of feats from which one is
    selected and then granted to the character.
-   The hyphen (-) is used only in the `OUTPUTNAME` of feats and should
    NOT be used in the feat list for this tag.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `FEAT` tag, the data included in a new `FEAT` tag
    will overwrite the existing tag data.

Example
-------

`FEAT:Blind Fight|Alertness`

Presents the "Blind-Fight" & "Alertness" feats to the user and grants
the feat selected to the character.

**.MOD Example:**

Initial Template: `Darkling <tab> FEAT:Blind Fight|Alertness`

Modified By: `Darkling.MOD <tab> FEAT:Blind Fight|Combat Reflexes`

Is Equivalent To: `Darkling <tab> FEAT:Blind Fight|Combat Reflexes`

Presents the "Blind-Fight" and "Combat Reflexes" feats to the user and
grants the feat selected to the character.

