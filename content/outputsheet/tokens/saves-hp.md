+++
date = "2016-08-01"
title = "Saves & Hit Points Output Sheet Tokens"
original_url = "/outputsheet/tokens/saves-hp.html"

[menu.main]
    identifier = "tokens_saves-hp"
    name = "Saves & Hit Points Output Sheet Tokens"
    parent = "tokens"
    
+++
------------------------------------------------------------------------

\*\*\* Updated 5.15.x

**<span id="check"></span> Token Name:** CHECK.x.y.y.z

**Variables Used (x):** Text (Save Type).

-   FORTITUDE - Use Fortitude save Check.
-   REFLEX - Use Reflex save Check.
-   WILL - Use Will save Check.
-   x - Where x is a digit, use the xth save check.

**Variables Used (y):** Text (Save Filter).

-   BASE - Displays only the class-based adjustment to the saving throw
    in question.
-   EPIC - Displays Epic bonuses to the saving throw in
    question (TYPE=EPIC).
-   MISC - Displays class, domain, luck, magical, racial, etc, bonuses
    to the saving throw in question.
-   TOTAL - Displays grand total for the saving throw in question. **Is
    the default if y is not supplied.**

\
 The following variables can be used on their own:

-   NAME - Displays the name of the save type.

\
 The following variables can be used on their own:

-   MAGIC - Displays only the bonuses from magic to the saving throw
    in question.
-   FEATS - Displays only the bonuses from feats to the saving throw
    in question.
-   RACE - Displays any racial bonuses to the saving throw in question.
-   STATMOD - Displays any stat bonuses to the saving throw in question.

OR as adjustments to BASE, EPIC, MISC or TOTAL

-   MAGIC - Adds the bonuses from Magic.
-   FEATS - Adds the bonuses from Feats.
-   RACE - Adds the bonuses from Race.
-   STATMOD - Adds the bonuses from Stats.

\
 The following variables are only applied to BASE, EPIC, MISC or TOTAL

-   NOEPIC - Removes the bonuses from Epic.
-   NOFEATS - Removes the bonuses from Feats.
-   NOMAGIC - Removes the bonuses from Magic.
-   NORACE - Removes the bonuses from Race.
-   NOSTAT - Removes the bonuses from Stats.
-   NOSTATMOD - Removes the bonuses from Stats. (same as NOSTAT)

**Variables Used (z):** Text (Output Restrictor).

\
 The following variables modify the end result the y variables

-   NOSIGN - Removes the leading "+" sign.

**What it does:**

-   Displays information about the characters saving throws.
-   Any check defined in *statsandchecks.lst* can be used by this tag.

**Example:**

`CHECK.REFLEX.FEATS`

Would display only the bonuses from feats to the Reflex saving throw.

**Example:**

`CHECK.REFLEX.BASE.NOSTAT.EPIC`

Would display the Base Reflex, minus any bonuses from Stats, plus any
bonuses from Epic.

------------------------------------------------------------------------

**<span id="hp"></span> Token Name:** HP

**What it does:**

Displays the characters maximum hit points.

**Example:**

`HP`

Would display the characters maximum hit points.

------------------------------------------------------------------------

**<span id="hproll"></span> Token Name:** HPROLL.x.y

**Variables Used (x):** Text (The level of the HP award).

**Variables Used (y):** Text (Property).

-   None - Displays the number entered by the player for the x-th level
    HP roll.
-   STAT - Displays the bonus due to stat modifier for the x-th level
    HP roll.
-   TOTAL - Displays the total hp gained for the x-th level.

**What it does:**

Displays the characters hit point information.

**Example:**

`HPROLL.0`

Displays the number entered by the player for the 1 ^st^ level HP roll.

`HPROLL.0.STAT`

Displays the bonus due to stat modifier for the 1st level HP roll.



