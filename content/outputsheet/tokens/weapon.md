+++
date = "2016-08-01"
title = "Weapon Output Sheet Tokens"
original_url = "/outputsheet/tokens/weapon.html"

[menu.main]
    identifier = "tokens_weapon"
    name = "Weapon Output Sheet Tokens"
    parent = "tokens"
    
+++
The below Tokens control how weapon and weapon proficency information is
presented in Output Sheets (OS).

------------------------------------------------------------------------

**<span id="weapon"></span> Token Name:** WEAPON.\[q.\]\[r.\]s.z

**Variables Used (q):** Text (Merge Type - Optional).

-   MERGEALL - Causes all weapons with the same name to be merged -
    default behavior.
-   MERGELOC - Causes all weapons with the same name and in the same
    location to be merged.
-   MERGENONE - No weapons with the same name are merged.

**Variables Used (r):** Text (Weapon Status - Optional).

-   CARRIED - Creates a 0-based index of carried or equipped weapons.
-   EQUIPPED - Creates a 0-based index of equipped weapons.
-   NOT\_CARRIED - Creates a 0-based index of weapons that are not
    carried or equipped.
-   NOT\_EQUIPPED - Creates a 0-based index of weapons that are not
    equipped (although they may be carried).

**Variables Used (s):** Number - The weapons position in the character's
weapon list - 0-based index

**Variables Used (z):** Text (The weapon property to be output).

-   ATTACKS - The number of attacks for weapon type (ie: 2 for double
    headed, etc).
-   ATTACKS - The number of attacks for weapon type (ie: 2 for double
    headed, etc).
-   BASEDAMAGE - The weapon's unadjusted damage (e.g. 1d8+3).
-   BASEDAMAGEBONUS - The weapon's unadjusted damage bonus (e.g. +3).
-   BASEHIT - The weapon's to hit containing most adjustments (no
    adjustment for two weapon fighting, even if weapons are equipped
    that way in the program).
-   BASICDAMAGE - The weapon's damage including most adjustments (no
    adjustment for which hand or hands are wielding the weapon).
-   BONUSDAMAGE - The weapon's bonus to damage (+1, etc.).
-   CATEGORY - The weapons category, such as Mithril, Melee,
    Slashing, etc.
-   CRIT - Weapon's Critical Range (ie 20 = 1, 19-20 = 2, 18-20 = 3,
    17-20 = 4).
-   DAMAGE - The amount of damage the weapon does.
-   FEATDAMAGE - Bonus to damage, based on feats.
-   FEATHIT - Bonus to hit, based on feats.
-   HAND - Hand that weapon is currently equipped in, Else none.
-   HEFT - Returns LIGHT, MEDIUM or HEAVY, looking for weapon size and
    character size. If the weapon is smaller, then it is LIGHT. This is
    not as useful in 3.5 mode because all weapons made for a specific
    sized character are the same size as the character and thus will
    always return MEDIUM. If the weapon is made for a smaller sized
    creature it will return LIGHT and if larger, HEAVY.
-   HIT - Weapon's modified bonus to hit, from character's total to
    hit bonus.
-   ISTYPE - Weapon's Type, for detecting if it is a Double Weapon
    or not.
-   LONGNAME - A more descriptive name.
-   MAGICDAMAGE - Weapon's magical bonus to damage.
-   MAGICHIT - Weapon's magical bonus to hit.
-   MISC - Returns all miscellaneous to hit bonuses.
-   MULT - Multiplier of Critical.
-   NAME(.NOSTAR) - Weapon's name (which matches the entry from the
    WEAPONPROF.LST file). If .NOSTAR is appended, the asterisk
    indicating whether the weapon is equipped will be stripped from
    the output.
-   NUMATTACKS - Displays the number of attacks the PC gets with the
    selected weapon.
-   OHDAMAGE - Displays the damage done by an offhand attack with the
    selected weapon (e.g. 1d8+1).
-   OHDAMAGEBONUS - Displays the damage bonus done by an offhand attack
    with the selected weapon (e.g. +1).
-   RANGE - Range of weapon, in feet.
-   RANGE.NOUNITS - Range of weapon, in feet (no ' indicator).
-   RATEOFFIRE - Rate of fire of the weapon, displayed as listed in the
    LST files following the RATEOFFIRE tag.
-   REACH - Reach of weapon, in feet.
-   SIZE - Size of weapon.
-   SIZEMOD - Returns the character size modifier.
-   SPROP - Special Properties of weapon.
-   TEMPLATEDAMAGE - Bonus to damage, from templates.
-   TEMPLATEHIT - Bonus to hit, from templates.
-   THDAMAGE - Displays the damage done by a two-handed attack with the
    selected weapon (e.g. 2d6+4).
-   THDAMAGEBONUS - Displays the damage bonus done by a two-handed
    attack with the selected weapon (e.g. +4).
-   TOTALHIT.x - The weapon's adjusted to hit bonuses for all attacks,
    or for attack x if it is specified (0-based index).
-   TWOHIT - The weapon's to hit bonuses if used in the off hand.
-   TWPHITH - The weapon's to hit bonuses if used in the primary hand
    with a heavy weapon in the other hand.
-   TWPHITL - The weapon's to hit bonuses if used in the primary hand
    with a light weapon in the other hand.
-   TYPE - Type of damage the weapon does.
-   WT - Weight of weapon in lbs.

**What it does:**

Displays various information about a character's weapons. Note: Use the
WEAPON token with the RANGELIST option (see below) if you want
ammunition bonuses included.

**Example:**

`WEAPON.0.SIZE`

Displays the size of the first weapon.

------------------------------------------------------------------------

**<span id="weapon_rangelist"></span> Token Name:**
WEAPON.\[q.\]\[r.\]s.RANGELIST.n.u

**Variables Used (q):** Text (Merge Type - Optional).

-   MERGEALL - Causes all weapons with the same name to be merged -
    default behavior.
-   MERGELOC - Causes all weapons with the same name and in the same
    location to be merged.
-   MERGENONE - No weapons with the same name are merged.

**Variables Used (r):** Text (Weapon Status - Optional).

-   CARRIED - Creates a 0-based index of carried or equipped weapons.
-   EQUIPPED - Creates a 0-based index of equipped weapons.
-   NOT\_CARRIED - Creates a 0-based index of weapons that are not
    carried or equipped.
-   NOT\_EQUIPPED - Creates a 0-based index of weapons that are not
    equipped (although they may be carried).

**Variables Used (u):** Text (Weapon Property).

-   None - Displays n-th range increment of the selected weapon.
-   DAMAGE - Displays the damage for the n-th range increment of the
    selected weapon.
-   TOTALHIT - Displays the complete hit progression for the n-th range
    increment of the selected weapon.
-   TOTALHIT.x - Displays the x-th attacks to hit modifier for the n-th
    range increment of the selected weapon (0-based index).

**Variables Used (z):** Text (The weapon property to be output).

-   ATTACKS - The number of attacks for weapon type (ie: 2 for double
    headed, etc).
-   ATTACKS - The number of attacks for weapon type (ie: 2 for double
    headed, etc).
-   BASEDAMAGE - The weapon's unadjusted damage (e.g. 1d8+3).
-   BASEDAMAGEBONUS - The weapon's unadjusted damage bonus (e.g. +3).
-   BASEHIT - The weapon's to hit containing most adjustments (no
    adjustment for two weapon fighting, even if weapons are equipped
    that way in the program).
-   BASICDAMAGE - The weapon's damage including most adjustments (no
    adjustment for which hand or hands are wielding the weapon).
-   BONUSDAMAGE - The weapon's bonus to damage (+1, etc.).
-   CATEGORY - The weapons category, such as Mithril, Melee,
    Slashing, etc.
-   CRIT - Weapon's Critical Range (ie 20 = 1, 19-20 = 2, 18-20 = 3,
    17-20 = 4).
-   DAMAGE - The amount of damage the weapon does.
-   FEATHIT - Bonus to hit, based on feats.
-   HAND - Hand that weapon is currently equipped in, Else none.
-   HEFT - Returns LIGHT, MEDIUM or HEAVY, looking for weapon size and
    character size. If the weapon is smaller, then it is LIGHT.
-   HIT - Weapon's modified bonus to hit, from character's total to
    hit bonus.
-   LONGNAME - A more descriptive name.
-   MAGICDAMAGE - Weapon's magical bonus to damage.
-   MAGICHIT - Weapon's magical bonus to hit.
-   MISC - Returns all miscellaneous to hit bonuses.
-   MULT - Multiplier of Critical.
-   NAME(.NOSTAR) - Weapon's name (which matches the entry from the
    WEAPONPROF.LST file). If .NOSTAR is appended, the asterisk
    indicating whether the weapon is equipped will be stripped from
    the output.
-   NUMATTACKS - Displays the number of attacks the PC gets with the
    selected weapon.
-   OHDAMAGE - Displays the damage done by an offhand attack with the
    selected weapon (e.g. 1d8+1).
-   OHDAMAGEBONUS - Displays the damage bonus done by an offhand attack
    with the selected weapon (e.g. +1).
-   RANGE - Range of weapon, in feet.
-   RANGE.NOUNITS - Range of weapon, in feet (no ' indicator).
-   RATEOFFIRE - Rate of fire of the weapon, displayed as listed in the
    LST files following the RATEOFFIRE tag.
-   REACH - Reach of weapon, in the selected unit set.
-   REACHUNIT - The unit that the reach is measured in (normally ft
    or m)
-   SIZE - Size of weapon.
-   SIZEMOD - Returns the character size modifier.
-   SPROP - Special Properties of weapon.
-   TEMPLATE - Bonus to hit, from templates.
-   THDAMAGE - Displays the damage done by a two-handed attack with the
    selected weapon (e.g. 2d6+4).
-   THDAMAGEBONUS - Displays the damage bonus done by a two-handed
    attack with the selected weapon (e.g. +4).
-   TOTALHIT.x - The weapon's adjusted to hit bonuses for all attacks,
    or for attack x if it is specified (0-based index).
-   TWOHIT - The weapon's to hit bonuses if used in the off hand.
-   TWPHITH - The weapon's to hit bonuses if used in the primary hand
    with a heavy weapon in the other hand.
-   TWPHITL - The weapon's to hit bonuses if used in the primary hand
    with a light weapon in the other hand.
-   TYPE - Type of damage the weapon does.
-   WT - Weight of weapon in lbs.

**What it does:**

Displays various attack information about a weapon depending on the
range increment. The SHORTRANGE (as defined in the miscinfo.lst) is
inserted into the range array if it is not already one of the weapon's
standard increments.

**Example:**

`WEAPON.0.RANGELIST.0`

Would display the damage for the 1st range increment for the 1st weapon.

------------------------------------------------------------------------

**<span id="weapon_ammunition"></span> Token Name:**
WEAPON.\[q.\]\[r.\]s.RANGELIST.n.u.AMMUNITION.v.w

**Suntoken Name:** AMMUNITION (Can only be used with RANGELIST)

**Variables Used (v):** Number (Displays the properties of the v-th
ammunition that will fit the s-th selected weapon at the n-th range
increment, 0-based index).

**Variables Used (w):** Text (Weapon Property).

-   None - Displays y-th range increment of the selected weapon.
-   DAMAGE - Displays the damage for the y-th range increment of the
    selected weapon.
-   SPROP - Displays the special properties for the y-th ammunition
    contained by the selected weapon.
-   TOTALHIT - Displays the complete hit progression for the y-th range
    increment of the selected weapon.
-   TOTALHITx - Displays the x-th attacks to hit modifier for the range
    increment of the selected weapon (0-based index).

**What it does:**

Displays information about the ammunition types that will fit the
selected weapon at the selected range increment.

**Example:**

`WEAPON.0.RANGELIST.0.AMMUNITION.0.DAMAGE`

Displays the damage from the 1st type of compatible ammunition at point
blank range for the 1st weapon.

------------------------------------------------------------------------

**<span id="weapon_contents"></span> Token Name:**
WEAPON.\[q.\]\[r.\]s.CONTENTS.v.w

**Suntoken Name:** CONTENTS

**Variables Used (v):** Number (Displays the properties of the v-th
ammunition contained by the s-th selected weapon, 0-based index).

**Variables Used (w):** Text (Weapon Property).

-   None - Displays name of the v-th selected contents of the s-th
    selected weapon.
-   QTY - Displays the number of the for the v-th ammunition contained
    by the s-th selected weapon.

**What it does:**

Displays information about the contents the selected weapon.

**Example:**

`WEAPON.0.CONTENTS.0`

Displays the name of the 1st type of contained ammunition.

------------------------------------------------------------------------

**<span id="weapon_rangelist_contents"></span> Token Name:**
WEAPON.\[q.\]\[r.\]s.RANGELIST.n.u.CONTENTS.v.w

**Suntoken Name:** CONTENTS

**Variables Used (v):** Number (Displays the properties of the v-th
ammunition contained by the s-th selected weapon at the n-th range
increment, 0-based index).

**Variables Used (w):** Text (Weapon Property).

-   None - Displays n-th range increment of the selected weapon.
-   DAMAGE - Displays the damage for the n-th range increment of the
    selected weapon.
-   SPROP - Displays the special properties for the n-th ammunition
    contained by the selected weapon.
-   TOTALHIT - Displays the complete hit progression for the n-th range
    increment of the selected weapon.
-   TOTALHITx - Displays the x-th attacks to hit modifier for the n-th
    range increment of the selected weapon (0-based index).

**What it does:**

Displays information about the contents the selected weapon at the
selected range increment.

**Example:**

`WEAPON.0.RANGELIST.0.CONTENTS.0.DAMAGE`

Displays the damage from the 1st type of contained ammunition at point
blank range fired by the 1st weapon.

------------------------------------------------------------------------

**<span id="weaponh"></span> Token Name:** WEAPONH.\[q.\]\[r.\]s.z

**Variables Used:** The same options available to the
[WEAPON](/outputsheet/tokens/weapon.html#weapon) token.

**What it does:**

Displays information about the "Unarmed" Weapon.

------------------------------------------------------------------------

**<span id="weapono"></span> Token Name:** WEAPONO.\[q.\]\[r.\]s.z

**Variables Used:** The same options available to the
[WEAPON](/outputsheet/tokens/weapon.html#weapon) token.

**What it does:**

Displays information about the Weapon equipped to the off-hand.

------------------------------------------------------------------------

**<span id="weaponp"></span> Token Name:** WEAPONP.\[q.\]\[r.\]s.z

**Variables Used:** The same options available to the
[WEAPON](/outputsheet/tokens/weapon.html#weapon) token.

**What it does:**

Displays information about the Weapon equipped to the primary hand.

------------------------------------------------------------------------

**<span id="weaponprofs"></span> Token Name:** WEAPONPROFS

**What it does:**

Displays the characters weapon proficiencies.

**Example:**

`WEAPONPROFS`

Displays the characters weapon proficiencies.



