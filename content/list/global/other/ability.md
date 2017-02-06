+++
date = "2016-08-01"
title = "ABILITY (Global: OTHER)"
original_url = "/list/global/other.html#ability"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "ABILITY (Global: OTHER)"
    parent = "other"
+++

## Status

Updated 6.03.02

## Syntax

`ABILITY:x|y|z|z`

## Parameters

-   x: Text (Ability category)
-   y: Text (Ability nature)
-   z: Text (Ability name or key)
-   z: TYPE=Text (Ability type)
-   z: .CLEAR
-   z: .CLEAR.Text (Ability name or key)



What it does
------------

-   Adds an ability, of the given category and nature, to a character.
-   The listed Ability Category must have been defined in the
    appropriate *gamemode/miscinfo.lst* or *abilitycategory.lst* file.
-   Valid Ability Natures are NORMAL, AUTOMATIC, or VIRTUAL.
-   When adding an ability to a category, that category's pool will be
    charged only if the "Nature" is NORMAL.
-   When including a feat with an internal chooser, subchoices can be
    handled one of two ways.
-   -   Subchoices must be specified within the tag. (e.g. Weapon Focus
        (Longsword)).\
         or
    -   Used in conjunction with the `CHOOSE` tag, `%LIST` can be used
        with this tag to provide the required choice.
-   The standard list for the ability category will be used to find a
    matching ability.
-   ABILITY tags can be qualified with [PRExxx](/list/global/pre.html)
    tags unless they use the `%LIST` parameter. ABILITY tags qualified
    with PRExxx tags will not be added unless the character meets
    the prerequisites.
-   For specific infomation on the `.CLEAR` tag, read the
    [.CLEAR](/list/global/other/clear.html) docs.
-   This tag is a replacement for the following tags: FEAT, VFEAT,
    and FEATAUTO.

**Note:** This tag **WILL NOT** activate a CHOOSER inside of a feat. You
must use [ADD:FEAT](/list/global/add/feat.html) to activate a chooser
inside of a feat being granted.

Examples
--------

`ABILITY:FEAT|AUTOMATIC|Empower Spell`

Adds the empower spell feat as an Auto feat.

`ABILITY:FEAT|AUTOMATIC|TYPE=SpecialFu`

Adds all feats with SpecialFu Type.

`ABILITY:Special Ability|AUTOMATIC|Monkey Fu Mastery`

Adds the Monkey Fu Mastery 'Special Ability' and lists it as Automatic
nature (if visible).

`ABILITY:CLASSFEATURE|VIRTUAL|Stunning Fist`

Adds the Stunning Fist ability as a virtual class feature.

`CHOOSE:WEAPONPROFS|LIST <tab> ABILITY:FEAT|AUTOMATIC|Weapon Focus (%LIST)`

The feat "Weapon Focus" is granted as an automatic feat with the weapon
chosen with the `CHOOSE` tag.

`ABILITY:FEAT|AUTOMATIC|.CLEAR`

Clears all automatic feats from the character.

`ABILITY:FEAT|VIRTUAL|.CLEAR.Empower Spell`

Clears the empower spell feat as an virtual feat.

`ABILITY:FEAT|AUTOMATIC|Toughness|Track`

Example of granting more than one feat. This grants 'Track' and
'Toughness' as automatic feats

`ABILITY:Special Ability|AUTOMATIC|Wild Shape(Small Animal)|Wild Shape(Medium Animal)|PREVARGTEQ:DruidWildShape,4`

Grants the Special Ability 'Wild Shape (Small Animal)' and 'Wild Shape
(Medium Animal' as an automatic ability once the variable
'DruidWildShape' equals or is greater than '4'

`ABILITY:Special Ability|AUTOMATIC|Wild Shape(Small Animal,Medium Animal)|PREVARGTEQ:DruidWildShape,4`

This shows an example of Abilities with sub-choices being granted in a
shorthand manner. Same as the above and grants the Special Ability 'Wild
Shape (Small Animal)' and 'Wild Shape (Medium Animal)' as an automatic
ability. Note: The Comma delimiter.

`ABILITY:Special Ability|AUTOMATIC|%LIST <tab> CHOOSE:ABILITYSELECTION|Special Ability|TYPE=CuteBunnies <tab> MULT:YES`

Would grant automatically, a Choice of type "CuteBunnies".

