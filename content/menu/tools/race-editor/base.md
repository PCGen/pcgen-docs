+++
date = "2016-08-01"
title = "Race Editor: Base Tab"
original_url = "/menu/tools/race-editor/base.html"

[menu.main]
    identifier = "race-editor_base"
    name = "Race Editor: Base Tab"
    parent = "race-editor"
    
+++
![Race Editor: Base Tab](../../../images/editors/race/basetab.png)

The **Base Tab** has everything required to make a simple Race.  The
remaining tabs are for more advanced Race creation.  The Races created
will be saved into the data/custom directory under the name of
customRaces.lst.

The **Race Name** is where you will enter the name for your Race.

The **Hands** is where you will enter the number of hands your race has.
It determines the Number of Hands the creature has for purposes of
Multi-attack and Multi-dexterity. It is also used in the Inventory,
Equipping screen which asks which hand to use the weapon (Shows as
Primary Hand, Secondary Hand, Secondary Hand 2, etc.).

The **Legs** is where you will enter the number of legs for your race
has. It is used to determine encumbrance and carrying capacity for
creatures/characters with a non-standard amount of legs. (i.e. more than
2).

The **Reach** is where you will enter the attack range in feet for your
race.

The **Skill Multiplier** is where you will enter the 1 ^st^ level
multiplier for determining starting skills for your race. The default is
x4. Most Multi-hit die creatures have x1 since adding class levels is
done as Multi-Classing

The **Bonus Skill Points / Level** is where you will enter additional
skill points that your race receives with each level increase. This
happens before multiplication of the first class level's skill points.

The **Bonus Starting Feats** is where you will enter additional feats
that your race receives at 1 ^st^ level. These are unrestricted feats.

The **CR** is where you will enter the starting Challenge Rating of your
race. For CR's less than 1, fractions are used (1/2, 1/4, 3/4).

The **Level Adjustment** is where you will enter the Effective Character
Level (ECL) of the race.

The **Size** is where you will enter the size class of your race. Size
is used in determining TO-HIT, AC, and affects some skills.

The **Hit Dice Advancement** is where you will enter highest HD the
creature can advance to. The last number in the comma delimited list is
the highest HD the creature can advance to, through HD advancement. All
the numbers preceding the last number each indicate the highest number
of HD the creature can have before its size increases by one category.
(Example: Assassin Vine: starts out as Large, with 4 HD. 5-16 it is
Huge, 17-32 it is Gargantuan, 33+ it is Colossal. 99 HD is the maximum
it can ever raise to so it's HD advancement would be 4,16,32,99)

The **Monster Class** is where you will enter the advancement type of
your race.

The **Monster Level** is where you will enter the number of Monster
Levels the race gets on creation. (Note: This is only used with Default
Monsters OFF)

The **Number of Hit Dice** is where you will enter the number of
Automatic Hit Dice the race starts with. (Note: This is used Only with
Default Monsters ON)

The **Hit Dice Size** is where you will enter the Hit Die Size for the
Number of **Hit Dice.** (Note: This is used Only with Default Monsters
ON)

The two **Type** windows, **Available** and **Selected** are used to
create a list of languages which the Race grants.

-   The **Add** and **Remove** buttons will move the highlighted
    language between the 2 windows, as will double clicking on a
    Type name.
-   New Types can be added by manually typing them and then clicking the
    **Add** button
-   It is important for matching up with Monster HD, and for references
    to race, such as the Rangers favored Enemy. Currently existing
    selections from the Monster List include: Aberration, Animal, Beast,
    Construct, Dragon, Elemental, Fey, Giant, Humanoid, Magical Beast,
    Monstrous Humanoid, Ooze, Outsider, Plant, Shapechanger, Undead
    and Vermin.

The **Source** field is a text window for listing what source material
the Race is from.  If it is a custom created Race, then you can leave
this blank or simply put in "custom"

The **Product Identity** checkbox is to denote if the Race's name being
created is the Product Identity of a publisher

The **Cancel** and **Save** buttons, which appear on every tab, are used
to either cancel the Race creation or save it to the customRaces.lst
file.



