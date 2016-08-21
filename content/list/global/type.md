+++
date = "2016-08-01"
title = "Global TYPE Page"
original_url = "/list/global/type.html"

[menu.main]
    identifier = "global_type"
    name = "Global TYPE Page"
    parent = "global"
    
+++
The LST file tag `TYPE` has many uses within the PCGen, most commonly it
is used to sort objects by type within the display or to identify a
group of objects to another object that grants a choice from that type.
Additionally there are certain types which have uses beyond sorting the
display and identification within the data. Examples of this include
types used to identify objects for the output sheets and special case
types used by the code for various purposes. This page will list these
types and explain their uses. This page will not detail all TYPEs used
in our data (that would be a long list) just the ones more commonly used
and/or which have uses outside of the dataset which may not be
immediately apparent.

The following Objects utilize TYPE tags:

-   [Classes](/list/global/type.html#class)
-   [Companion Modifiers](/list/global/type.html#companionmod)
-   [Deities](/list/global/type.html#deity)
-   [Equipment](/list/global/type.html#equipment)
-   [Equipment Modifiers](/list/global/type.html#equipmod)
-   [Feats and Abilities](/list/global/type.html#feat)
-   [Languages](/list/global/type.html#language)
-   [PCC Files](/list/global/type.html#pcc)
-   [Races](/list/global/type.html#race)
-   [Skills](/list/global/type.html#skill)
-   [Spells](/list/global/type.html#spell)
-   [Starting Kits](/list/global/type.html#startkit)
-   [Templates](/list/global/type.html#template)
-   [Weapon Proficiencies](/list/global/type.html#weaponprof)

------------------------------------------------------------------------

<span id="class"></span> Class TYPE
-----------------------------------

**Tag Name:** TYPE:x

**Variables Used (x):** Text (Class type)

**What it does:**

-   This is used within the filters of PCGen to sort the classes by
    their respective types (makes it easier to find a specific class).
-   In addition to sorting classes in the display, class type is used by
    the gameMode to define certain properties of the class as set by the
    <span class="lstfile"> miscinfo.lst </span> tag
    [CLASSTYPE](/list/system/gamemode-miscinfo/classtype.html) . These
    properties include how much (if any) CR is added per level of the
    class, whether or not the class is considered a monster class and if
    the class is subject to an XP penalty for multiclassing.
-   See also [CRFORMULA](/list/system/gamemode-miscinfo/crformula.html)
    , [ISMONSTER](/list/system/gamemode-miscinfo/ismonster.html) and
    [XPPENALTY](/list/system/gamemode-miscinfo/xppenalty.html)

**Example:**

`TYPE:Base.PC`

The class will appear if the "Base" or "PC" filter options are selected.

**Where it is used:**

Class Line.

**Commonly Used Types:**

RSRD

`PC`

`NPC`

`Prestige`

`Monster`

MSRD

`Advanced`

------------------------------------------------------------------------

<span id="companionmod"></span> Companion Modifier TYPE
-------------------------------------------------------

**Tag Name:** TYPE:x

**Variables Used (x):** Text (Companion type)

**What it does:**

-   Used to define what the creature is for the purposes of display on
    the resources tab.
-   Companion Modifiers can be composed of several lines, each requiring
    the `TYPE` tag.
-   Each companion Modifier line begins with a
    [FOLLOWER](/list/data/companionmodifiers/follower.html) or
    [MASTERBONUSRACE](/list/data/companionmodifiers/masterbonusrace.html)
    tag and not a name or KEY, using the type as the primary
    identifier instead.
-   Types in Companion Modifiers can contain Spaces, though this is
    normally not recommended.

**Example:**

`TYPE:Familiar`

Defines the creature as a "Familiar" for resources tab display purposes.

**Commonly Used Types:**

`Familiar`

`Animal Companion`

`Special Mount`

------------------------------------------------------------------------

<span id="deity"></span> Deity TYPE
-----------------------------------

**Tag Name:** TYPE:x.x

**Variables Used (x):** Text (Deity Type)

**What it does:**

-   This is a period-delimited (".") list of the types the deity
    belongs to.
-   TYPE is not commonly used in Deity files.

**Examples:**

`TYPE:Good`

The deity belongs to the "Good" type.

`TYPE:Good.Chaotic`

The deity belongs to the "Good" and "Chaotic" types.

------------------------------------------------------------------------

<span id="equipment"></span> Equipment TYPE
-------------------------------------------

**Tag Name:** TYPE:x.x

**Variables Used (x):** Text (Item Type)

**What it does:**

-   The `TYPE` tag is used for many filtering and PRExxx tags. Please
    follow the conventions used in the Players Rules for the `TYPE` tag.
-   The `TYPE` tag may also be used to identify which "slot" the item
    will be equiped to. See [Equipment Type
    Slots](/list/global/type.html#equipslottypes) below

**Example:**

`TYPE:Weapon.Simple.Melee.Slashing.Metal`

Item is a Simple Melee Slashing Metal Weapon.

`Scythe.MOD <tab> TYPE:.CLEAR <tab> TYPE:Weapon.Exotic.Melee.Piercing.Slashing.Standard`

Modifying the Scythe to have a few more capabilities.

**Special Case and Commonly Used Types:**

> <span id="equipslottypes"></span> **Equip Slot Types** - Equipment
> slot types are specific types which are used to control how many of a
> specific equipment TYPE a character can Equip to any one Equipset.
> Equipment slots and their associated types are defined in the
> [equipmentslots.lst](/list/system/gamemode-equipmentslots.html)
> gameMode file. Since Slot TYPEs control where an item can be equipped
> no item should have more than one of these types, an item with more
> than one slot type will confuse PCGen and may not be equipped into the
> expected slot. A slot type is not required and any item with no slot
> type designated can still be equipped. There is no limit on how many
> such items can be equipped.
>
> **Common Equip Slot Types**
>
> `Eyegear`
>
> `Headgear`
>
> `Amulet`
>
> `Armor`
>
> `Robe`
>
> `Cape`
>
> `Shirt`
>
> `Clothing`
>
> `Belt`
>
> `Shield`
>
> `Bracer`
>
> `Glove`
>
> `Weapon`
>
> `Ring`
>
> `Legwear`
>
> `Boot`
>
> **Uncommon Equip Slot Types**
>
> `PsionicTattoo` - used in SRD and RSRD
>
> `Tattoo` - used in MSRD
>
> `Transportation` - used in MSRD
>
> `Vehicle` - used in Spycraft
>
> **Output Sheet Types**
>
> Items with the following types are not listed in the Equipment List
> but are instead listed in a separate block labeled Money.
>
> `Coin`
>
> `Gem`
>
> The following types trigger special blocks for these types of
> equipment and are mutually exclusive.
>
> `Armor`
>
> `Ammunition`
>
> `Shield`
>
> `Weapon`
>
> The following is used to identify Equipment which can be useful in
> combat during ones turn but which is not a Weapon or Ammunition (and
> thus already listed under attacks). This is used in some newer stat
> block formats. Examples might include a wand of Fireballs, a
> Thunderstone and a Tanglefoot Bag.
>
> `OffensiveGear`
>
> The following is used to identify Equipment which can be useful for
> defense in combat but which is not an Armor or Shield item (and thus
> already listed under Armor Class). This is used in some newer stat
> block formats. Examples might include a Cloak of Displacement and a
> Ring of Invisibility.
>
> `DefensiveGear`
>
> The following is used to identify Equipment which can be used to cast
> illumination. The item should also contain certain `QUALITY` tags
> which define the brightness and duration of the light source.
>
> `LightSource`
>
> **Weapon Types:**
>
> All items of type `Weapon` must also have at least one of the types
> `Melee` or `Ranged` .
>
> The type `Thrown` is designates a weapon as a thrown weapon and
> activates a second output block showing the weapons Ranged statistics.
>
> The type `Double` designates a weapon as a double weapon and activates
> the three [ALTxxx](/list/data/equipment/altcritmult.html) tags for the
> statistics for the second head.
>
> **Weapon Damage Types**
>
> Weapon Damage types are defined in the
> [miscinfo.lst](/list/system/gamemode-miscinfo.html) gameMode file by
> the [WEAPONTYPE](/list/system/gamemode-miscinfo/weapontype.html) tag.
>
> `Bludgeoning`
>
> `Piercing`
>
> `Slashing`
>
> `Fire`
>
> `Acid`
>
> `Electricity`
>
> `Cold`
>
> `Poison`
>
> `Sonic      `
>
> Additional MSRD Weapon Damage Types:
>
> `Ballistic`
>
> `Concussion`
>
> `Radiation`
>
> `Disintegration`
>
> **Miscellaneous Types:**
>
> `Container` designates the item is a container and activates the
> [CONTAINS](/list/data/equipment/contains.html) tag in the item.

------------------------------------------------------------------------

<span id="equipmod"></span> Equipment Modifier TYPE
---------------------------------------------------

**Tag Name:** TYPE:x.x

**Variables Used (x):** Text (Type name)

**What it does:**

-   Provides a list of the types of items that the modifier can be
    applied to.
-   Equipment must have at least one type that an equipment modifier has
    in order for that modifier to be applied.
-   Used in conjunction with `PRETYPE` and `ITYPE` .

**Example:**

`TYPE:Armor.Shield`

Item is of the "Armor" & "Shield" types.

`EDF Combat Armor.MOD <tab> TYPE:.CLEAR <tab> TYPE:Armor.Medium.Suit.Tactical.PL6`

Modifies the item is of the "Armor" "Medium" "Suit" "Tactical" "PL6"
types.

**Special Case:**

`BaseMaterial`

The BaseMaterial TYPE is used to identify Equipment Modifiers which
represent materials an item can be made from such as Mithral,
Adamantine, Steel and Wood. An equipment item can only have one
Equipment Modifier with the "BaseMaterial" type, if a second one is
applied the first is automatically removed.

------------------------------------------------------------------------

<span id="feat"></span> Feat and Ability TYPEs
----------------------------------------------

**Tag Name:** TYPE:x

**Variables Used (x):** Text (Feat or Ability type)

**What it does:**

This is a period-delimited (.) list of the types assigned to the feat or
ability.

**Example:**

`TYPE:General.Fighter`

This Feat is part of the "General" and "Fighter" feat types.

`Acrobatic.MOD <tab> TYPE:.CLEAR <tab> TYPE:General.Fast.Pugilist.Rustler.Showman`

Modification of the Acrobatic Class to be "General", "Fast", "Pugilist",
"Rustler", "Showman", feat types.

`Charm.MOD <tab> TYPE:Efficacious`

This modification adds the "Efficacious" feat type to the list of types
for this feat.

**Special Case and Common Types:**

> Feat and Ability types fall into three general uses; Game Rule types,
> Class Bonus Feat or Ability types, and types used by the Output
> Sheets. Game rule types represent the types the game itself groups the
> feats or abilities into and are derived from the source material.
> Class bonus feat or ability types are used to create a group of feats
> or abilities from which a class is granted a selection.
>
> **Common Game Rule Types**
>
> `General`
>
> `ItemCreation`
>
> `Metamagic`
>
> **Common Class Bonus Feat or Ability Types**
>
> `Fighter`
>
> `Wizard`
>
> `FavoredEnemy`
>
> `Turning`
>
> `RogueAbilities`
>
> **Output Sheet types**
>
> Types used by the output sheets require more explanation since their
> purpose is not evident in the data files.
>
> The following two types are used in Abilities of CATEGORY=Special
> Ability (in the RSRD). Every Ability in this category should have one
> of these types or the other. Depending on the type the output sheet
> will list the ability in the Special Attacks block or the Special
> Qualities block.
>
> `SpecialAttack`
>
> `SpecialQuality`
>
> Abilities designated as Extraordinary, SpellLike, Supernatural or
> PsiLike in the source material do so with an abbreviation at the end
> of the name, (Ex), (Sp), (Su) and (Ps). The output sheet can use this
> type to add the abbreviation to the end of the ability name if it is
> appropriate for that sheet. Not all sheets will want to display the
> name in that way and by using a type rather than having the
> abbreviation be part of the name this makes it optional.
>
> `Extraordinary`
>
> `SpellLike`
>
> `Supernatural`
>
> `PsiLike`
>
> The following type identifies the Feat or Ability as one which
> provides an alternate attack or modifies a standard attack. This is
> used in some newer stat block formats.
>
> `AttackOption`
>
> The following type identifies the Feat or Ability as one which
> represents an Aura or continuous area of effect ability. This is used
> in some newer stat block formats.
>
> `Aura`
>
> The following type identifies the Feat or Ability as one which grants
> some ability to communicate. This is used in some newer stat block
> formats where the ability is listed with languages.
>
> `Communicate`
>
> The following type identifies the Feat or Ability of a Defensive
> nature other than Resistances, Immunities, AC or HP effecting
> abilities. This is used in some newer stat block formats.
>
> `Defensive`
>
> The followng type identifies the Feat or Ability as one which
> represent a specific immunity. This is used in some newer stat block
> formats.
>
> `Immunity`
>
> The following type identifies the Feat or Ability as one which provide
> a circumstantial AC bonus or other defensive benefit. This is used in
> some newer stat block formats where the ability is listed with AC
> details.
>
> `ModifyAC`
>
> The following type identifies the Feat or Ability as one which provide
> a bonus or other defensive benefit related to hit points. This is used
> in some newer stat block formats where the ability is listed with hit
> points.
>
> `ModifyHP`
>
> The following type identifies the Feat or Ability as one which
> provides some for of special movement or modifies the movement rate.
> This is used in some newer stat block formats where the ability is
> listed with movement rates.
>
> `ModifyMovement`
>
> The following type identifies the Feat or Ability as one which
> represent a specific resistance. This is used in some newer stat block
> formats.
>
> `Resistance`
>
> The following type identifies the Feat or Ability as one which
> represent a circumstancial bonus to one or more saving throws. This is
> used in some newer stat block formats where the bonus is listed with
> saving throws.
>
> `SaveBonus`
>
> The following type identifies the Feat or Ability as one which
> represent a specific special sense or perception. This is used in some
> newer stat block formats.
>
> `Sense`
>
> The following type identifies the Feat or Ability as one which
> represent a specific weakness. This is used in some newer stat block
> formats.
>
> `Weakness`

------------------------------------------------------------------------

<span id="language"></span> Language TYPE
-----------------------------------------

**Tag Name:** TYPE:x.x

**Variables Used (x):** Text (Language type)

**What it does:**

This is a period-delimited (".") list of the types that languages are.

**Example:**

`TYPE:Spoken.Written.Read`

Language is "Spoken", "Written" and "Read".

`Celestial <tab> TYPE:Spoken`

Language Celestial is "Spoken", not "Written" or "Read".

**Commonly Used Types:**

`Read`

`Spoken`

`Written`

------------------------------------------------------------------------

<span id="pcc"></span> PCC TYPE
-------------------------------

**Tag Name:** TYPE:x.x

**Variables Used (x):** Text (Source types)

**What it does:**

-   This tag ***MUST*** be the third tag in the file.
-   The `TYPE` tag is used to set the source display tree in the
    Sources Tab.
-   PCC types can contain spaces.
-   PCC `TYPE` tags cannot have more than three type elements as
    follows:
    -   element 1 is the name of the company or individual that produced
        the material that the data files are based.
    -   element 2 is the format of that original material (e.g.,
        Sourcebook, Web Enhancement, Magazine, Supplement, etc.).
    -   element 3 is the "campaign setting" for the original material
        (such as the publisher's campaign realm) and is optional.
-   **Caution:** If two PCC files use the same types but in different
    order the display in the Sources Tab can potentially be disrupted.
    Side effects can include sources being displayed more than once.
    Duplicate types should be used in the same order in every file.

**Example:**

`TYPE:Foo Games.Core Rules.Core`

------------------------------------------------------------------------

<span id="race"></span> Race TYPE
---------------------------------

**Tag Name:** TYPE:x

**Variables Used (x):** Text (Race type)

**What it does:**

-   Defines the Type of creature the race is.
-   Important for matching up with Monster HD, and for references to
    race, such as the Rangers Favored Enemy.
-   Currently existing selections from the Monster List include:\
     Aberration, Animal, Beast, Construct, Dragon, Elemental, Fey,
    Giant, Humanoid, Magical Beast, Monstrous Humanoid, Ooze, Outsider,
    Plant, Shapechanger, Undead, and Vermin
-   **Note:** In the past, the `TYPE` tag in race files has been used to
    set the races Creature Type as defined in the game rules. This
    function is now being performed by the
    [RACETYPE](/list/data/races/racetype.html) tag and the use of the
    `TYPE` tag to set this is being phased out.

**Example:**

`TYPE:Outsider`

The race is of the "Outsider" type.

**Commonly Used Types:**

`Aberration          Animal          Beast          Construct          Dragon          Elemental          Fey          Giant          Humanoid          Magical Beast          Monstrous Humanoid          Ooze          Outsider          Plant          Shapechanger          Undead          Vermin`

------------------------------------------------------------------------

<span id="skill"></span> Skill TYPE
-----------------------------------

**Tag Name:** TYPE:x.x

**Variables Used (x):** Text (Skill type)

**What it does:**

-   All skill type tags should use the skill's key attribute as the
    first type ("None" is an acceptable option).
-   Multiple types can be specified as a period-delimited (".") list.

**Example:**

`TYPE:Charisma.Perform`

This skill belongs to the "Charisma" and "Perform" types.

`Craft (Electronic - class skill).MOD <tab> TYPE:.CLEAR <tab> TYPE:Scientist_Skills.Terraformer_Skills`

This skill is modified to be in the "Scientist\_Skills" and
"Terraformer\_Skills" types.

**Commonly Used Types:**

**To group by relevant ability**

`Strength          Dexterity          Constitution          Intelligence          Wisdom          Charisma`

**To group by relevant skill type**

`Craft          Knowledge          Perform`

------------------------------------------------------------------------

<span id="spell"></span> Spell TYPE
-----------------------------------

**Tag Name:** TYPE:x.x

**Variables Used (x):** Text (Spell type)

**What it does:**

-   Indicates what "types" are associated with the spell.
-   You can also Specify multiple types using the . (period) delimiter.

**Example:**

`TYPE:Arcane.Divine`

Spell is both "Arcane" and "Divine".

**Commonly Used Types:**

`Arcane`

`Divine`

`Psionic`

------------------------------------------------------------------------

<span id="startkit"></span> Starting Kit TYPE
---------------------------------------------

**Tag Name:** TYPE:x.x

**Variables Used (x):** Text (Start Kit type)

**What it does:**

-   Indicates what "types" are associated with the starting kit.
-   You can also specify multiple types using the period-delimiter.

**Example:**

`TYPE:DefaultMonster`

Kit is a "DefaultMonster" kit.

**Commonly Used Types:**

`DefaultMonster`

`Treasure`

`NPC`

`PC`

`StartingKit`

------------------------------------------------------------------------

<span id="template"></span> Template TYPE
-----------------------------------------

**Tag Name:** TYPE:x.x

**Variables Used (x):** Text (Template type)

**What it does:**

-   Defines the Type of creature members of the template are.
-   Important for matching up with Monster HD, and for references to
    race, such as the Rangers Favored Enemy
-   **Note:** In the past, the `TYPE` tag in tTemplate files have been
    used to alter the races Creature Type as defined in the game rules.
    This function is now being performed by the
    [RACETYPE](/list/data/races/racetype.html) tag and the use of `TYPE`
    to alter this is being phased out.

**Example:**

`TYPE:Outsider`

Is a "Outsider" if this template is selected.

------------------------------------------------------------------------

<span id="weaponprof"></span> Weapon Proficiency TYPE
-----------------------------------------------------

**Tag Name:** TYPE:x.x

**Variables Used (x):** Text (Type name)

**What it does:**

-   Defines what type of weapon proficiency isrequired for a character
    to be able to use a particular weapon.
-   Proficiency types are used to grant proficiencies and to grant
    bonuses to weapons of a certain proficiency.
-   Types generally represent broad groups of weapons, such as Simple,
    Martial and Exotic, or a smaller, more specific group of weapons
    such as Axe, Sword, Crossbow and Thrown used for granting bonuses.

**Example:**

`TYPE:Simple`

Characters with "Simple" weapon proficiency can use this weapon.

------------------------------------------------------------------------



