+++
date = "2016-08-01"
title = "Special Ability Related Output Sheet Tokens"
original_url = "/outputsheet/tokens/special-ability.html"

[menu.main]
    identifier = "tokens_special-ability"
    name = "Special Ability Related Output Sheet Tokens"
    parent = "tokens"
    
+++
------------------------------------------------------------------------

**<span id="class"></span> Token Name:** CLASS.x.SALIST

**Variables Used (x):** Number (The x-th class in the character's class
list - 0-based index).

**What it does:**

Displays the Special Abilities granted by the x-th class.

**Example:**

`CLASS.0.SALIST`

Displays the Special Abilities granted by the characters 1 ^st^ class.

------------------------------------------------------------------------

**<span id="prohibitedlist"></span> Token Name:** PROHIBITEDLIST

**What it does:**

A Specialist Wizard must choose some prohibited schools. The selected
school will be displayed in this list.

**Example:**

`PROHIBITEDLIST`

Displays a comma delimited list of prohibitions

------------------------------------------------------------------------

**<span id="race.abilitylist"></span> Token Name:** RACE.ABILITYLIST

**What it does:**

Displays a comma delimited list of the characters racial special
abilities.

**Example:**

`RACE.ABILITYLIST`

Displays a comma delimited list of the characters racial special
abilities.

------------------------------------------------------------------------

**<span id="speciallist"></span> Token Name:** SPECIALLIST

**What it does:**

Displays a comma delimited list of the characters special abilities.

**Example:**

`SPECIALLIST`

Displays a comma delimited list of the characters special abilities.

------------------------------------------------------------------------

**<span id="specialability"></span> Token Name:** SPECIALABILITY.x.y

**Variables Used (x):** Text (The x-th special ability in the
character's special ability list - 0-based index).

**Variables Used (y):** Text (Property).

-   None - Displays the name of the x-th special ability in the
    character's special ability list.
-   DESCRIPTION - Displays the description of the x-th special ability
    in the character's special ability list.

**What it does:**

Displays the name or description of a character's special abilities.

**Example:**

`SPECIALABILITY.0.DESCRIPTION`

Displays the description of the 1 ^st^ special ability in the
character's special ability list.

------------------------------------------------------------------------

**<span id="temp"></span> Token Name:** TEMP.x

**Variables Used (x):** Number (The special ability's position in the
character's special ability list - 0-based index).

**What it does:**

Displays the name of the characters x-th Special Ability.

**Example:**

`TEMP.0`

Displays the name of the characters 1 ^st^ Special Ability.



