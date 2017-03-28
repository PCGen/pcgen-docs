+++
date = "2016-08-01"
title = "BENEFIT (Data: feats.lst)"
original_url = "/list/data/feats.html#benefit"
categories = [ "all-tag", "feats-tag" ]
[menu.main]
    name = "BENEFIT"
    parent = "data_feats"
    identifier = "data_feats_BENEFIT"
+++

## Status

None

## Syntax

`BENEFIT:x`

## Parameters

-   x: Text (feat benefit text)



What it does
------------

-   This is the benefit text of the feat from the source material.
-   The included text will be displayed in the feat description field if
    the ["Display Feat
    Description"](/menu/settings/appearance/display.html) checkbox in
    the Appearance/Display Options Preference window is unchecked.
    Otherwise the text from the [DESC](/list/data/feats.html#desc) tag
    will be displayed.
-   PRExxx tags can be used with the `BENEFIT` tag.
-   Multiple `BENEFIT` tags per line are allowed with all qualifying
    `BENEFIT` tags being concatonated for output and separated
    by spaces.
-   `.CLEAR` will clear all `BENEFIT` tags.
-   `.CLEAR.(regular expression match)` will clear specific instances.
-   `BENEFIT` tags will take variable substitution.
    -   Within the text a % followed by a number will substitute the
        \#th variable from the variable list associated with the
        `BENEFIT` .
    -   Variables are specified after the descriptive text and are
        pipe-delimited (|).
    -   The special parameter %% will insert an actual % character into
        the text.
    -   If the parameter needs to be next to a number the parameter
        number should be surrounded in curly brackets { }. For
        example, %{1000}gp.
-   The following special variables are allowed within the variable
    list:
    -   `%NAME` - The name of the object this `BENEFIT` tag is in.
    -   `%FEAT` - Will substitute the descriptions of feats within the
        object that match the associated preqrequisites.
    -   `%CHOICE` - Will replace the first associated choice in
        the object.
    -   `%LIST` - Will substitute all choices into that parameter as a
        comma-delimited list.
-   Formulas can be parsed and the results replaced in the output by
    enclosing the variables and formulas within parentheses.
    -   [CASTERLEVEL](/list/data/feats.html#casterlevel) , a variable
        specifically designed for this purpose, is commonly used though
        other variables can be used as well.
    -   Because anything within parentheses is assumed to be a formula
        to be parsed, text containing parentheses must substitute
        brackets \[ \] in place of parentheses.
-   **Regular Expressions:** Java has a Regular Expression library built
    in that is very similar to Perl regular expressions. Basically it
    allows for pattern matching in strings. You can create fairly
    powerful match structures using things like character groups
    "\[a-zA-Z\]" match any alphabetic character or groupings
    "(bat|super)man" match batman or superman and many more. So,
    for example, you could clear all benefits by doing
    `BENEFIT:.CLEAR..*` , or clear all exceptional abilities by doing
    `BENEFIT:.CLEAR.\(Ex\)` , or clear everything that's non-numeric
    with `BENEFIT:.CLEAR.[A-Za-z]` .
-   **.MOD Behavior:** When modifying a feat with the `.MOD` tag, given
    an existing `BENEFIT` tag, the data included in a new `BENEFIT` tag
    will be included as a separate tag.

Example
-------

`BENEFIT:This is sample text for the example purposes`

Adds feat benefit.

**.MOD Example (Include Separately):**

Initial Feat: `<feat name> <tab> BENEFIT:Initial benefit text.`

Modified By: `<feat name> <tab> BENEFIT:New benefit text.`

Is Equivalent To:
`<feat name> <tab> BENEFIT:Initial benefit text. <tab> BENEFIT:New benefit text.`

The output of the modified will show the following: &quotInitial benefit
text. New benefit text."

