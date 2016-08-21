+++
date = "2016-08-01"
title = "DESC (Global: OTHER)"
original_url = "list/global/other.html#desc"
categories = [ "all-tag", "other-tag" ]
+++

## Status

Updated 6.01.3

## Syntax

`DESC:x`

## Parameters

-   x: Text (ability description)
-   x: Text (deity description)
-   x: Text (domain description)
-   x: Text (equipment description)
-   x: Text (feat description)
-   x: Text (spell description)



What it does
------------

-   The `DESC` tags provides a description appropriate for the object it
    is attached to, i.e. ability, deity, domain, equipment, feat,
    or spell.
-   PRExxx tags can be used with the `DESC` tag.
-   Multiple `DESC` tags per line are allowed with all qualifying `DESC`
    tags being concatonated for output and separated by spaces.
-   `.CLEAR` will clear all `DESC` tags.
-   `.CLEAR.(regular expression match)` will clear specific instances.
-   `DESC` tags now take variable substitution.\
    -   Within the text a percent-sign (%) followed by a number (\#)
        will substitute the \#th variable from the variable list
        associated with the `DESC` . For example, %1 will substitute the
        first variable into that position in the `DESC`
    -   Variables are specified at the end of the descriptive text and
        are pipe-delimited (|).
    -   The special parameter %% will insert an actual % character into
        the text.
    -   If the parameter needs to be next to a number the parameter
        number should be surrounded in curly brackets { }. For
        example, %{1000}gp.
-   The following special variables are allowed within the variable
    list:\
    -   `%CHOICE` - Will replace the first associated choice in
        the object.
    -   `%FEAT` - Will substitute the descriptions of feats within the
        object that match the associated preqrequisites.
    -   `%LIST` - Will substitute all choices comma separated into
        that parameter.
    -   `%NAME` - The name of the object this `DESC` tag is in.
-   Formulas can be parsed and the results replaced in the output by
    enclosing the variables and formulas within parentheses.\
    -   [CASTERLEVEL](/list/global/define.html#casterlevel) , a variable
        specifically designed for this purpose, is commonly used though
        other variables can be used as well.
    -   Because anything within parentheses is assumed to be a formula
        to be parsed, text containing parentheses must substitute
        brackets \[ \] in place of parentheses.
    -   Java has a Regular Expression library built in that is very
        similar to Perl regular expressions. Basically it allows for
        pattern matching in strings. You can create fairly powerful
        match structures using things like character groups "\[a-zA-Z\]"
        match any alphabetic character or groupings "(bat|super)man"
        match batman or superman and many many more. So, for example,
        you could clear all DESC tags by doing `DESC:.CLEAR..*` , or
        clear all exceptional abilities by doing `DESC:.CLEAR.\(Ex\)` ,
        or clear everything that's non-numeric with
        `DESC:.CLEAR.[A-Za-z]` .

Example
-------

`DESC:This domain grants the turn code monkey speech into english`

The domain description.

`DESC:This is a description of the item.`

Adds a description for the equipment.

`DESC:This is sample text for the example purposes`

Adds feat description.

`DESC:Kick Butt (level 3)|PRELEVEL:3`

Adds feat description only if the PC is level 3 or higher.

`DESC:Assembly ~ 1 table|PREVAREQ:AssemblyTables,1          DESC:Assembly ~ %1 tables|AssemblyTables|PREVARGTEQ:AssemblyTables,2`

Adds a feat description which is dependent upon the value of the
variable AssemblyTables.

`DESC:You get a +2 bonus on all %1 saving throws|%CHOICE`

Adds feat description and replaces %1 with the first choice made.

`DESC:Bardic Music %1/day (%2)|BardicMusicTimes|%FEAT=TYPE.BardicMusic`

The variable "BardicMusicTimes" is substituted for "%1" and the text
from the "DESC" tags in all granted feats with type "BardicMusic" are
concatenated and substituted for "%2".

`DESC:You get a +3 bonus on all checks involving %1|%LIST.`

Adds feat description replaces %LIST with all choices made.

`DESC:%3 Sneak Attacks per day for +%1d%2 damage|SneakAttack|SneakAttackDie|SneakAttackTimes`

Adds feat description substituting the variables from the positions
specified.

`Advanced Combat Martial Arts.MOD <tab> DESC:.CLEAR <tab> DESC:When the character scores a critical hit on an opponent with an unarmed strike, the character deals triple damage`

Changes the feat description, substituting the specified.

`DESC:Toasts the monsters with fire`

What the spell does.

`DESC:Target is prone for (CASTERLEVEL) rounds.`

If the value of CASTERLEVEL is equal to 3 then this would output:
"Target is prone for 3 rounds.".

`Maximize Power.MOD <tab> DESC:.CLEAR <tab> DESC:You can manifest powers to maximum effect.`

Replaces the standard spell DESC with the attached.

