+++
date = "2016-08-01"
title = "The Global BONUS Tags"
original_url = "/list/global/bonus.html"

[menu.main]
    identifier = "global_bonus"
    name = "The Global BONUS Tags"
    parent = "global"
    
+++
The BONUS tag tells PCGen that the following information is to be added
to a character as well as where it is to be added.

The general format for bonus tags are as follows:

> `BONUS:<category>|<group>|<formula>`

This can be followed by pipe-delimitated `PRExxx` or `TYPE=<type>` tags.

Each of the "Tag Names" in this page go in the &lt;category&gt; field,
and the "Variables Used" go in the &lt;group&gt; field.

For the Formula syntax, see the [Math Operators and
Formulas](/list/global/formulas.html) page.

`LIST` is a special case in <span class="lstfile"> feats.lst </span> .
It can be placed in most &lt;group&gt; categories. `LIST` will be
replaced by the choice from a `CHOOSE` tag contained within the feat.

------------------------------------------------------------------------

<span id="bonustypes"></span> BONUS Types
-----------------------------------------

Each bonus comes in four different types.

1.  The **Typeless** bonus with no type
2.  The **Standard** bonus with type (TYPE=name)
3.  The **.REPLACE** bonus type (TYPE=name.REPLACE)
4.  The **.STACK** bonus type (TYPE=name.STACK)

------------------------------------------------------------------------

**Bonus Type:** Typeless

**What it Does:**

-   These have no `TYPE=` statement, and are always added into the
    final result.
-   Because it is typeless, it can not be tracked in the OS sheets in a
    breakdown by bonus type.

**Examples:**

`BONUS:HP|CURRENTMAX|3`

This bonus would grant the character an additional three hit points.\

`BONUS:SKILL|Bluff,Listen|4`

This bonus would grant the character a bonus to the listed skills of
four.\

`BONUS:SKILL|STAT=DEX|1`

This would grant the character a bonus of one to all skills based on
DEX.

------------------------------------------------------------------------

**Bonus Type:** Standard

**What it Does:**

-   These have a TYPE=name and are used for stacking purposes.
-   There is a special system file called system\\miscinfo.lst.
-   If a **TYPE** is listed in that file, then these TYPEs behave just
    like a type-less bonus.
-   Otherwise, only the highest value of the same type is used in the
    final result.

**Examples:**

`BONUS:HP|CURRENTMAX|2|TYPE=Luck          BONUS:HP|CURRENTMAX|3|TYPE=Luck`

So long as the 'Luck' type is not listed in miscinfo.lst, these two
would result in a final value of 3, since 3 is the largest 'Luck' type.\

`BONUS:SKILL|Bluff,Listen|3|TYPE=Luck          BONUS:SKILL|Bluff,Listen|4|TYPE=Divine`

These would return a 3 from Luck, and a 4 from Divine, for a total of 7.
They are different Types.\

`BONUS:SKILL|Bluff,Listen|2|TYPE=Luck          BONUS:SKILL|Bluff,Listen|3|TYPE=Luck          BONUS:SKILL|Bluff,Listen|4|TYPE=Divine`

This would also return a value of 7, since 3 is the highest Luck bonus,
and 4 is the highest Divine bonus.

------------------------------------------------------------------------

**Bonus Type:** .REPLACE

**What it Does:**

-   This is subtype of the TYPE= standard type.
-   .REPLACE items are counted together to determine the final value of
    a particular TYPE.

**Examples:**

`BONUS:SKILL|Bluff,Listen|3|TYPE=Luck.REPLACE          BONUS:SKILL|Bluff,Listen|2|TYPE=Luck.REPLACE          BONUS:SKILL|Bluff,Listen|4|TYPE=Luck          BONUS:SKILL|Bluff,Listen|2|TYPE=Luck`

This would take the 2 and 3 with the .REPLACE (total 5) and compares it
to the standards, which are 2 and 4, and takes the highest value, for
5.\

`BONUS:SKILL|Bluff,Listen|1|TYPE=Luck.REPLACE          BONUS:SKILL|Bluff,Listen|1|TYPE=Luck.REPLACE          BONUS:SKILL|Bluff,Listen|2|TYPE=Luck.REPLACE          BONUS:SKILL|Bluff,Listen|2|TYPE=Luck          BONUS:SKILL|Bluff,Listen|6|TYPE=Luck`

This would take the values from the .REPLACE (total 4), and compares it
to the standards, which are 2 and 6, and takes the highest value, for 6.

------------------------------------------------------------------------

**Bonus Type:** `.STACK`

**What it Does:**

-   This is subtype of the `TYPE=<type>` standard type.
-   `.STACK` items are counted in addition to the normal and `.REPLACE`
    to determine the final value of a particular type.
-   `.STACK` stacks together with itself like `.REPLACE` , but is also
    added to normal types.

**Examples:**

`BONUS:SKILL|Bluff,Listen|4|TYPE=Luck`

`BONUS:SKILL|Bluff,Listen|2|TYPE=Luck.STACK`

This would take the 4 of type `Luck` , and then add 2 more from the
`Stack` , on top of it.

`BONUS:SKILL|Bluff,Listen|4|TYPE=Luck.REPLACE`

`BONUS:SKILL|Bluff,Listen|4|TYPE=Luck.STACK`

This would take the 4 of type `Luck` , and then add 4 more from the
`Stack` , on top of it.

`BONUS:SKILL|Bluff,Listen|4|TYPE=Luck`

`BONUS:SKILL|Bluff,Listen|3|TYPE=Luck.REPLACE`

`BONUS:SKILL|Bluff,Listen|3|TYPE=Luck.REPLACE`

`BONUS:SKILL|Bluff,Listen|1|TYPE=Luck.STACK`

This would take the 4 normal, compare to the `.REPLACE` (6) and give the
higher value, then add in the `.STACK` , for a final value of 7.

`BONUS:SKILL|Bluff,Listen|4|TYPE=Luck`

`BONUS:SKILL|Bluff,Listen|1|TYPE=Luck.REPLACE`

`BONUS:SKILL|Bluff,Listen|1|TYPE=Luck.REPLACE`

`BONUS:SKILL|Bluff,Listen|3|TYPE=Luck.STACK`

`BONUS:SKILL|Bluff,Listen|3|TYPE=Luck.STACK`

This would take the normal (4), compare it to the total `.REPLACE` (2),
give the higher value, then add in the `.STACK` (6) for a final value of
10.

------------------------------------------------------------------------

Special BONUS Types
-------------------

There are two types of special "types" defined in the *miscinfo.lst*
file in the *system/gamemode* folders. These are the [Bonus Stack
Types](/list/global/bonus.html#bonusstacks) and the [AC
Types](/list/global/bonus.html#actype) .

> ### <span id="bonusstacks"></span> Bonus Stacks
>
> Within PCGen, tags which do not have a `TYPE=<type>` sub-tag appended
> are assumed to stack, tags which do have a type appended do not
> normally stack. Some games have exceptions to this rule and list
> specific types which always do stack. In the fantasy gameModes Dodge
> and Circumstance always stack. The
> [BONUSESTACKS](/list/system/gamemode-miscinfo/bonusstacks.html) tag in
> the *miscinfo.lst* file lists those exceptions. The following are
> commonly used types that are defined within the *miscinfo.lst* file
> for this purpose.
>
> `Defense`
>
> `Dodge`
>
> `Circumstance`
>
> `NotRanged`
>
> `NotFlatFooted`
>
> ### <span id="actype"></span> Armor Class Types
>
> PCGen tracks bonuses to the armor class through the use of several AC
> types. The following are commonly used types that are defined with the
> [ACTYPE](/list/system/gamemode-miscinfo/actype.html) tag in the
> GameMode's *miscinfo.lst* file.
>
> `Total`
>
> `Flatfooted`
>
> `Touch`
>
> `Base`
>
> `Equipment`
>
> `Armor`
>
> `Shield`
>
> `Ability`
>
> `Size`
>
> `NaturalArmor`
>
> `NaturalArmorEnhancement`
>
> `Misc`
>
> `ClassDefense`
>
> `Dodge`

------------------------------------------------------------------------

Miscellaneous BONUS Type Notes
------------------------------

Bonuses with negative numbers have been found to stack even when they
have matching types.

While you can't `.CLEAR` a `BONUS` tag you can add a counter bonus that
would negate it. In this case you would add a counter bonus and `PRExxx`
tag it with the reverse of the feat's prerequisite.

------------------------------------------------------------------------

<span id="taglist"></span> BONUS Tag List
-----------------------------------------

------------------------------------------------------------------------

