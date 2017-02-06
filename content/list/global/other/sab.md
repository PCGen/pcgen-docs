+++
date = "2016-08-01"
title = "SAB (Global: OTHER)"
original_url = "/list/global/other.html#sab"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "SAB (Global: OTHER)"
    parent = "other"
+++

## Status

Updated 5.13.6

## Syntax

`SAB:x`

## Parameters

-   x: Text (Special Ability Name)
-   x: .CLEAR
-   x: .CLEAR.Text (Special Ability Name)



### SAB - 'special ability'

*Displays a text string in the 'special abilities' section of the
character sheet.*

#### What it does

-   This grants the character a Special Ability that will get listed
    together with all other special abilities the character has.
-   The `%` tag will fill in a number from a variable listed after a
    pipe `|` .
-   This can be done numerous times, with each successive percent sign
    `%` relating to the next variable listed after another pipe `|` .
-   This can be specified via number of `%#` , with each successive
    numbered `%` relating to the next variable listed after another pipe
    `|` . The count starts at zero and counts up.
-   Each variable needs to be defined (via the global `DEFINE` tag.)
-   The Special Ability will not be displayed if the last variable or
    formula equals zero.
-   `SAB:.CLEAR` can be used in conjunction with the `.MOD` but does not
    support cross-level interactions.
-   `SAB:.CLEAR` will only clear a previous `SAB` in the same object
    (class, template, etc.). It will not clear them across objects.
-   `SAB:.CLEAR.Text` must include the exact text of the Special Ability
    to be removed but only the exact text up to the
    first open-parentheses. The `CLEAR` and Replace tags should be at
    the end of the line, so the new and old tags are not.
-   SAB tags can be qualified with
    `[PRExxx](globalfilesprexxx.html)` tags.
-   SAB tags can be used with `%CHOICE` tags to display the result of a
    `CHOOSE` result.

#### Examples

1.  `SAB:Fire in the Hole`

    Grants the special ability "Fire in the Hole".

2.  `SAB:Sneak Attack +%d%|Sneak Attack|Sneak Attack Die`

    If the PC's `Sneak Attack` variable had value `2` , and the PC's
    `Sneak Attack Die` variable had value `6` , this would grant the
    special ability `Sneak Attack +2d6` .

3.  `SAB:.CLEAR.+1d6 to natural weapons → SAB:+1d8 to natural weapons`

    Clears the "Natural Weapons" value and makes it +1d8 instead.

4.  `SAB:Banana toss|PRERACE:monkey`

    Grants the special ability "Banana toss" if the character's race
    is "monkey".

5.  `SAB:Banana toss via elemental power of (%CHOICE) → STACK:NO → MULT:YES → CHOOSE:Air|Earth|Fire|Water`

    Offers a Choice between the elemental powers of `Air` , `Earth` ,
    `Fire` and `Water` for banana tossing. The same ability may be taken
    multiple times, but a different element must be chosen each time.

6.  `SAB:.CLEAR.Poison`

    Clears the `Poison` value and replaces it with nothing.

7.  Within a class definition in a [Class file](/list/data/classes.html)
    :

        CLASS:Basketweaver        
         1  →  SAB:Basket Toss
         5  →  SAB:.CLEAR.Basket Toss  →  SAB:Greater Basket Toss

    Replaces the `Basket Toss` ability with the `Greater Basket Toss`
    ability at `Basketweaver` class level 5.

8.  Within a class definition in a [Class file](/list/data/classes.html)
    :

        CLASS:Basketweaver
        1  →  SAB:Basket Toss|PREVARLT:CL,5
        5  →  SAB:Greater Basket Toss

    Another way of replacing the `Basket Toss` ability with the
    `Greater Basket Toss` ability at `Basketweaver` class level 5.

#### Remarks

The `SAB` tag has no effect on calculations. Its sole purpose is to
display a short ability description under the *Special Abilities*
section of the character sheet. An example for
`SAB:Plays nice with others.` is shown below.

![](../../images/tags/SAB_1.png)

The `ASPECT` tag can be used to display similar pieces of text in the
other boxes, *Conditional Save Modifiers* , *Conditional Combat
Modifiers* , and *Conditional Skill Modifiers* .

-   Conditional combat bonus:
    `ASPECT:CombatBonus|+2 to attack and damage vs. elves.`
-   Conditional saving throw bonus:
    `ASPECT:SaveBonus|-2 penalty on saving throws vs. fear effects.`
-   Conditional skill bonus:
    `ASPECT:SkillBonus|+2 Competence bonus on Climb checks when climbing trees.`

Example code for an Ability list file:

    My Ability Name
      →  CATEGORY:Special Ability
      →  ASPECT:CombatBonus|+2 to attack and damage vs. elves.
      →  ASPECT:SaveBonus|-2 penalty on saving throws vs. fear effects.
      →  ASPECT:SkillBonus|+2 Competence bonus on Climb checks when climbing trees.

