+++
date = "2016-08-01"
title = "Miscellaneous Output Sheet Tokens"
original_url = "/outputsheet/tokens/misc.html"

[menu.main]
    identifier = "tokens_misc"
    name = "Miscellaneous Output Sheet Tokens"
    parent = "tokens"
    
+++
------------------------------------------------------------------------

**<span id="math"></span> Token Name:** x&lt;Mathematical Operator&gt;x

**Variables Used (x):** Number or Numeric Token (Operand).

**Variables Used (y):** Mathematical Operator

**What it does:**

-   Simple mathematical operations are supported in the output sheets.
-   Valid operators include the following:
    -   + (Addition operator).
    -   - (Subtraction operator).
    -   \* (Multiplication operator).
    -   / (Divisor operator).
    -   @ (Divisor operator that returns an integer).
    -   \^ (Exponentiation operator).
    -   INTVAL (Displays just the integer portion of the result).
    -   NOZERO (Displays blank if the result is zero, otherwise displays
        the result with the appropriate sign).
    -   SIGN (Pre-pends a sign (+ or -) to the result. This is ignored
        if it already has a sign).
    -   TRUNC (Displays the integer and the first decimal place of
        the result).
-   Do not use spaces in between the operands and the operator.

**Example:**

`TOTALLEVELS+15`

Displays the total number of levels plus 15.

`(COMBAT.AC.TOTAL-3).INTVAL`

Displays the integer portion of the Combat Armor Class minus 3.

`SKILL.Spot.RANKS*SKILL.Listen.RANKS`

Displays the number of spot ranks multiplied by the number of listen
ranks.

`(SKILLPOINTS.UNUSED/2).TRUNC`

Displays the integer and fist decimal place of the unused skill points
divided by 2.

`(VAR.RangeMod-2).INTVAL.SIGN`

Displays the integer portion preceded with a sign (+ or -) for the
result of the Range Modifier minus 2.

------------------------------------------------------------------------

**Token Name:** |%x|

**Variables Used (x):** Text (Filter Option).

-   ARMOR.x - Will stop all output unless the character has at least x
    pieces of Armor.
-   ARMOR.ITEM.x - Will stop all output unless the character has at
    least x items that confer armor bonuses.
-   ARMOR.SHIELD.x - Will stop all output unless the character has at
    least x Shields.
-   BIO - Will stop all output unless the character has a
    Biography entered.
-   CATCHPHRASE - Will stop all output unless the character has a Catch
    Phrase entered.
-   COUNT.x - Will stop all output unless the character has more than
    zero of the counted entity.
-   DESC - Will stop all output unless the character has a
    Description entered.
-   DOMAIN.x - Will stop all output unless the character has at least
    x Domains.
-   GAMEMODE.x - Will stop all output unless Gamemode x is used.
-   INTERESTS - Will stop all output unless the character has an
    Interest entered.
-   LOCATION - Will stop all output unless the character has a
    Location entered.
-   MISC.COMPANIONS - Will stop all output unless the character has
    Companions entered.
-   MISC.FUNDS - Will stop all output unless the character has
    Funds entered.
-   MISC.MAGIC - Will stop all output unless the character has
    Magic entered.
-   NOTES - Will stop all output unless the character has Notes entered.
-   PERSONALITY.x - Will stop all output unless the character has
    personality x entered.
-   PHOBIAS - Will stop all output unless the character has a
    Phobia entered.
-   PROHIBITEDLIST - Will stop all output unless the character has a
    Prohibited Spell List entered.
-   REGION - Will stop all output unless the character has a
    Region entered.
-   RESIDENCE - Will stop all output unless the character has a
    Residence entered.
-   SKILLPOINTS - Will stop all output unless the character has the
    total skill points specified.
-   SPEECHTENDENCY - Will stop all output unless the character has a
    Speech Tendency entered.
-   SPELLLISTBOOK.class.level.sbook - Will stop all output unless the
    character has the specified spell in their spell book.
-   SPELLLISTCLASS.x - Will stop all output unless the character has at
    least x Class Spell Lists.
-   SUBREGION - Will stop all output unless the character has a
    Sub-region entered.
-   FOLLOWERTYPE.type - Will stop all output unless the character has a
    follower of the type specified.
-   TEMPLATE - Will stop all output unless the character has a Template.
-   TEMPLATE.x - Will stop all output unless the character has at least
    x Templates.
-   WEAPON.x - Will stop all output unless the character has at least
    x Weapons.
-   WEAPONPROFS - The WEAPONPROFS filter is special in that it doesn't
    rely on the count, but on a setting in the preferences. If you
    choose to display WEPONPROFS on your sheet, the filter is ignored.
    If you choose not to, it filters even if you have WEAPONPROFS.

**What it does:**

-   Used for filtering.
-   Where x is the number of appropriate items the character must have
    or the filter will filter out all output until the next filter is
    reached or the filter is ended via the |%| token.
-   Filter can also be a **comma delimited list of Classname=level**
    pairs (where Classname is a valid Class name and level is the
    minimum level of the class for the filter).
-   Classname could also be **SPELLLISTCLASS.x=level** where x is the
    xth spellcasting class of the character.
-   Filter can also be in the form **VAR.name.label.value** where name
    is the name of a defined variable, label is one of EQ (equals), NEQ
    (not equals), LT (less than) LTEQ, (less than equal to), GT (greater
    than), GTEQ (greater than equal to), and value is some value to
    which the named variable is compared. Only 1 filter is active at a
    time (they can't be nested).

**Example:**

`|%WEAPON.3|`

The filter will stop all output (until this filter is ended or the next
filter started) unless the character has at least 3 weapons.

------------------------------------------------------------------------

**<span id="bonuslist"></span> Token Name:** BONUSLIST.w,x,y,z

**Variables Used (w):** Text (The type of bonus to be displayed).

**Variables Used (x):** Text (The subtype of bonus to be displayed).

**Variables Used (y):** Text (Optional Bonus Value Seperator - Defaults
to a space " ").

**Variables Used (z):** Text (Optional Bonus Delimiter - Defaults to a
comma-space ", ").

**What it does:**

Displays the list of bonuses by type and value associated with the tags
involved.

**Example:**

`BONUSLIST.COMBAT.AC`

Would list all COMBAT.AC bonuses as a comma-space delimited list.

------------------------------------------------------------------------

**<span id="br"></span> Token Name:** BR

**What it does:**

Adds a carriage return to the output. Normally only used on text output
sheets and inside manualwhitespace sections.

**Example:**

`2|BR|3`

Then the output would look like:\
`2          3`

------------------------------------------------------------------------

**<span id="count"></span> Token Name:** COUNT\[x\]

**Variables Used (x):** Text (Count Type).

**What it does:**

-   Used to count objects and insert the result in other places.
-   Can be used in any of the FOR loops in place of max.
-   If you are having problems, try remembering this is a base 0 list.
    The first item is number Zero, not One.
-   Also if you are still having problems, then you might have a Base 1
    list, where the start is at One not Zero. Different programmers,
    different styles.
-   The following are the tags that can be used as the &lt;Count
    Type&gt;:
    -   CHECKS - The number of checks defined in the gameMode.
    -   CLASSES - The number of classes a character has.
    -   CONTAINERS - The number of containers a character has.
    -   DOMAINS - The number of domains a character has.
    -   EQTYPE.&lt;type1&gt;.ADD.&lt;type2&gt;.ADD.&lt;typen&gt; - The
        number of items of the type specified a character has. (All
        types present in equipment .lst files can be used here).
    -   EQTYPE.WEAPON - The number of weapons a character has.
    -   EQTYPE.ACITEM - The number of armor a character has.
    -   EQUIPMENT - The number of items a character has (one arrow in
        bow, 19 carried and 40 in backpack will return 1).
    -   EQUIPMENT.MERGELOC - The number of items a character has,
        including items split between locations (one arrow in bow, 19
        carried and 40 in backpack will return 3).
    -   FEATNAME=&lt;featname&gt; - Some feats can be taken more
        than once. This will tell you how many times a particular feat
        has been taken. (If &lt;featname&gt; is VISIBLE:YES)
    -   FEATNAME=&lt;featname&gt;.ALL - Some feats can be taken more
        than once. This will tell you how many times a particular feat
        has been taken. (If &lt;featname&gt; is VISIBLE:NO)
    -   FEATS - This has been deprecated, use FEATS.VISIBLE instead.
    -   FEATS.ALL - The total number of visible and hidden feats a
        character has excluding automatic feats.
    -   FEATS.HIDDEN - The number of hidden feats a character has
        excluding automatic feats.
    -   FEATS.VISIBLE - The number of visible feats a character has
        excluding automatic feats.
    -   FEATSALL - This has been deprecated, use
        FEATSALL.VISIBLE instead.
    -   FEATSALL.ALL - The number of both visible and hidden feats a
        character has including automatic feats.
    -   FEATSALL.HIDDEN - The number of hidden feats a character has
        including automatic feats.
    -   FEATSALL.VISIBLE - The number of visible feats a character has
        including automatic feats.
    -   FEATSAUTO - This has been deprecated, use
        FEATAUTO.VISIBLE instead.
    -   FEATSAUTO.ALL - The number of both visible and hidden automatic
        feats a character has.
    -   FEATSAUTO.HIDDEN - The number of hidden automatic feats a
        character has.
    -   FEATSAUTO.VISIBLE - The number of visible automatic feats a
        character has.
    -   FEATTYPE.&lt;type1&gt;.&lt;type2&gt;.&lt;typen&gt; - This has
        been deprecated, use
        FEATTYPE.&lt;type1&gt;.&lt;type2&gt;.&lt;typen&gt;.VISIBLE instead.
    -   FEATTYPE.&lt;type1&gt;.&lt;type2&gt;.&lt;typen&gt;.ALL - The
        number of both visible and hidden feats of the type specified a
        character has.
    -   FEATTYPE.&lt;type1&gt;.&lt;type2&gt;.&lt;typen&gt;.HIDDEN - The
        number of hidden feats of the type specified a character has.
    -   FEATTYPE.&lt;type1&gt;.&lt;type2&gt;.&lt;typen&gt;.VISIBLE - The
        number of visible feats of the type specified a character has.
    -   FOLLOWERTYPE.&lt;followertype&gt; - The number of followers of
        the type specified a character has.
    -   LANGUAGES - The number of languages the character knows.
    -   MOVE - The number of movement types the character has.
    -   NOTES - The items notes entered when creating a custom item.
    -   RACESUBTYPES - The number of racial subtypes the character has.
    -   SA - The number of special abilities a character has.
    -   SKILLS - The number of skills the character knows.
    -   SPELLBOOKS - The number of spellbooks a character has.
    -   SPELLRACE - Returns 1 if the character has any innate spells, 0
        if the character has no innate spells.
    -   SPELLSKNOWN - The number of spells the character knows.
    -   SPELLSINBOOK%class.%book.%level - The number of spells of a
        particular class, in a particular spell book and of a particular
        level that the character has (Note: The Known Spellbook is
        number 0, The Innate Spellbook is number 1 and the -1 Spellbook
        should not be used anymore).
    -   SPELLTIMES%class.%book.%level.%spell - The number of times the
        referenced spell has been memorized.
    -   STATS - The number of stats a character has.
    -   TEMPBONUSNAMES - The number of Temporary Bonus Tab items a
        character has.
    -   TEMPLATES - The number of templates a character has.
    -   VFEATS - This has been deprecated, use VFEATS.VISIBLE instead.
    -   VFEATS.ALL - The number of both visible and hidden virtual feats
        a character has.
    -   VFEATS.HIDDEN - The number of hidden virtual feats a
        character has.
    -   VFEATS.VISIBLE - The number of visible virtual feats a
        character has.
    -   VISION - The number of vision types a character has.

**Example:**

`BONUS:HP|CURRENTMAX|3*COUNT[FEATNAME=Toughness]`

The count token is used in this example to calculate the total bonus.

`FOR,%num,0,COUNT[SKILLS],1,1          {Statements}          ENDFOR`

The {statements} would be processed for each of the skills the character
has.

`FOR,%spell,0,COUNT[SPELLSINBOOK0.0.0],1,1          {Statements}          ENDFOR`

The {statements} would be processed for each of the 0 ^th^ level spells
in the 1 ^st^ classes 1 ^st^ spellbook (known) that the character has.

------------------------------------------------------------------------

**<span id="count"></span> Token Name:** count(x,y) - See [jep count
()](/list/global/formulas.html#count) function in the Global Formulas
page.

------------------------------------------------------------------------

**<span id="csheettag2"></span> Token Name:** CSHEETTAG2.x

**Variables Used (x):** Symbol (Replacement symbol for the default
"\\").

**What it does:**

Changes the delimiter used by embedded DFOR/FOR loops to the character
specified.

**Example:**

`CSHEETTAG2.~          DFOR.0,(COUNT[SKILLS]+1)/2,1,COUNT[SKILLS],(COUNT[SKILLS]+1)/2,<td>~SKILL%~</td> <td>~SKILL%.TOTAL~</td><td>~SKILL%.RANK~</td>          <td>~SKILL%.ABILITY~</td><td>~SKILL%.MOD~,<tr align="center">,</tr>,0`

This would change the field delimiter from the default "\\" character
for "\~". This allows the FOR/DFOR loop to be used in RTF output which
does not allow the "\\" character to be used

------------------------------------------------------------------------

**<span id="dfor"></span> Token Name:** DFOR.r,s,t,u,v,w,x,y,z

**Variables Used (r):** Number (The initial value).

**Variables Used (s):** Number (Limit for new line progression).

**Variables Used (t):** Number (Value added once per line).

**Variables Used (u):** Number (Limit for in line progression).

**Variables Used (v):** Number (Value added in line until totalMax is
passed).

**Variables Used (w):** Text (The phrase is the code that is parsed for
tokens - use \\'s instead of |'s, and the % within the tokens will be
replaced with the actual value of the index).

**Variables Used (x):** Text (The text that will be printed at the
beginning of the for loop and after the Variable "y").

**Variables Used (y):** Text (The text that will be printed every time
through the loop).

**Variables Used (z):** Number (The loop will break when no more items
are found before the natural end of the loop (max) if exists is 1. If
exists is 2 and the charactersheet is currently within a filter, PCGen
will not print anything else until the end of the filter |%| is reached
or another filter is begun. 0 means it will always loop to the natural
end of the loop.).

**What it does:**

-   Creates loop processing of statements. This is very similar to the
    FOR loop, except this allows for stepping across the table (in the
    same line) independent of stepping down.
-   The initial value is **r** , the values going down are found by
    adding **t** to **r** once for each line.
-   To find the value within the same line, this starting value ( **r**
    for the first line, **r** + **t** for the next, etc.) has **v**
    added to it, this is done as may times until **u** is passed.
-   Likewise, **t** is added to **r** each line until **s** is passed.
-   The same logic that handles the FOR loop handles the DFOR loop.
-   The display of the output can be controlled via the COMMA and CRLF
    iteration terminators.

**Example:**

`DFOR.0,(COUNT[SKILLS]+1)/2,1,COUNT[SKILLS], (COUNT[SKILLS]+1)/2,<td>\SKILL%\</td>          <td>\SKILL%.TOTAL\</td><td>\SKILL%.RANK\</td>          <td>\SKILL%.ABILITY\</td><td>\SKILL%.MOD\,<tr align="center">,</tr>,0`

Produces a 2 column row table of all skills.

------------------------------------------------------------------------

**<span id="dir"></span> Token Name:** DIR.x

**Variables Used (x):** Text (Directory Option).

-   PCG - Displays the PCGen Character file (.PCG) directory.
-   PCGen - Displays the PCGen System Directory.
-   HTML - Displays the PCGen Character Output HTML directory.
-   TEMP - Displays the system TEMP directory.
-   TEMPLATES - Displays the PCGen Character Output Template directory.

**What it does:**

Displays File output paths.

**Example:**

`DIR.PCGen`

Would display " `D:\RPG\PCGen\system` " if PCGen was installed in "
`D:\RPG\PCGen` ".

`DIR.TEMPLATES`

Would display " `D:\RPG\PCGen\outputsheets\d20\fantasy` " if PCGen was
installed in " `D:\RPG\PCGen` ".

`DIR.PCG`

Would display " `D:\RPG\PCGen\characters` " if PCGen was installed in "
`D:\RPG\PCGen` ".

`DIR.html`

Would display " `D:\RPG\PCGen\outputsheets\d20\fantasy\htmlxml` " if
PCGen was installed in " `D:\RPG\PCGen` ".

`DIR.TEMP`

Would display " `C:\Temp` " if that was the Operating System's temp
directory.

------------------------------------------------------------------------

**<span id="export"></span> Token Name:** EXPORT.x

**Variables Used (x):** Text (Export Option).

-   DATE - Displays the date of export.
-   TIME - Displays the time of export.
-   VERSION - Displays the version of PCGen used to export
    the character.

**What it does:**

Displays character export details.

**Example:**

`EXPORT.DATE`

Displays the date of export.

------------------------------------------------------------------------

**<span id="for"></span> Token Name:** FOR,%v,w,x,y,z

`FOR,%v,w,x,y,z          {Statements}          ENDFOR`

**Variables Used (v):** Text (Variable Name).

**Variables Used (w):** Number (The initial value).

**Variables Used (x):** Number (Limit for new line progression - You may
use a number, COUNT token, STRLEN token or any valid csheet token).

**Variables Used (y):** Number (Value added once per line).

**Variables Used (z):** Number (The loop will break when no more items
are found before the natural end of the loop (max) if exists is 1. If
exists is 2 and the charactersheet is currently within a filter, PCGen
will not print anything else until the end of the filter |%| is reached
or another filter is begun).

**What it does:**

-   Creates loop processing of statements.
-   Nested FOR loops are supported.
-   The FOR and ENDFOR tokens must be at the start of the line or they
    will not function properly.
-   STRLEN takes the form of STRLEN\[stringtobecounted\] and returns the
    number of characters in the string.

**Example:**

`FOR,%test,0,20-STRLEN[SKILL.%skill],1,0          {Statements}          ENDFOR`

Counts from 0 to 20 minus the sting length of the skill name.

------------------------------------------------------------------------

**Token Name:** FOR.t,u,v,w,x,y,z

**Variables Used (t):** Number (Loop control variable initial value)

**Variables Used (u):** Number (Loop control variable max limit)

**Variables Used (v):** Number (Loop control variable increment value)

**Variables Used (w):** Text (Code phrase to be parsed for tokens)

**Variables Used (x):** Text (Text output at the beginning of the loop)

**Variables Used (y):** Text (Text output at the end of each loop)

**Variables Used (z):** Number (Loop break switch, 1 or 2)

**What it does:**

-   Creates loops for processing of statements and is the only FOR loop
    type that can be used for a party sheet.
-   This style of FOR loop does not support nesting without the
    double-backslash (\\\\).
-   The code phrase to be parsed must use backslashes's (\\) instead of
    pipe's (|), and the percent sign (%) within the tokens will be
    replaced with the actual value of the index.
-   If you have a `FOR.` loop involving the characters within the party
    for-loop, you must enclose the character for-loop in
    double-backslash (\\\\) token markers.
-   `FOR.` loop on party sheets ( <span class="lstfile"> psheet\*.\*
    </span> ) can only loop on character numbers, so `\\%.NAME\\`
    is valid.
-   You may use the special keywords **COMMA** or **NONE** for either
    **x** or **y** (COMMA prints out a comma and NONE prints
    out nothing)
-   **STRLEN** takes the form of `STRLEN[stringtobecounted]` and returns
    the number of characters in the string.
-   The loop break switch, parameter (z), determines when the loop
    breaks:
    -   With z=1, the loop will break at the natural end of the
        loop, i.e. the loop continues until the control variable reaches
        the max limit per parameter (u).
    -   With z=2, and with a character sheet currently within a filter,
        PCGen will not print anything else until the end of the
        filtering loop is reached, or another filter is begun.

**Example:**

`<table>`

`|FOR.0,10,1,[td]`

`\\%.FOR.0,100,1,\SKILL%\,(,),2\\`

`,<tr>,</tr>,1|`

`</table>`

Produces a list of all the party member's skills.

`<table>`

`|FOR.0,100,1,`

`\\%.NAME\\`

`,[ , ],1|`

`<table>`

Produces a list of all the party member's names.

------------------------------------------------------------------------

**<span id="iif"></span> Token Name:** IIF

**General Usage:**

IIF(x)

{y}

ELSE

{z}

ENDIF

**Variables Used (x):** Text (Conditional statement. To be evaluated)

**Variables Used (y):** Text (True statement)

**Variables Used (z):** Text (False statement)

**What it does:**

-   Evalutes the Conditional Statement and processes the
    relevant statements.
-   The true statements will be evaluated if the condtional statement
    is true.
-   The false statements will be evaluated if the conditional statement
    is false.
-   ELSE and the second set of statements are optional.
-   Nested IIFs are supported.

**Example:**

`IIF(CL>3)          {True Statement}          ELSE          {False Statement}          ENDIF`

Returns the results of the evaluation of the true statement if Class
Level is greater then 3. Otherwise, the results of the evaluation of the
false statement is returned.

**<span id="iif"></span> Token Name:** IIF(x.y.x)

**Variables Used (x):** Text (Condition to be evaluated).

**Variables Used (y):** Text (Operator, i.e. AND, OR).

**What it does:**

-   Evalutes the condition and processes the relevant statements.
-   The logical operator and second expression are optional.

**Example:**

`IIF(CL>3.AND.TL<10)`

Returns TRUE is Class Level was greater then 3 and the Total Level was
less than 10.

**Token Name:** IIF(&lt;JEP boolean expression&gt;)

**What it does:**

Evaluates the [JEP boolean
expression](/list/global/formulas.html#boolean) .

**Example:**

`IIF((CL>5)||(TL>5))`

Returns TRUE if Class Level or Total Level are greater-then 5.

**Token Name:** IIF(EVEN)

**What it does:**

True if the variable is an even number (frequently used to control
grey/white shading by line).

**Example:**

`IIF(EVEN:%spell)`

Would be true if the spell line was even.

**Token Name:** IIF(UNEVEN)

**What it does:**

True if the variable is an uneven number.

**Example:**

`IIF(VAR.IF(VAR("COUNT[SKILLTYPE=Strength]")>0;1;0):1)`

Evaluates to true if number of skills with type of Strength are greater
than 0 Notice the use of semi-colon where a comma should normally be
used. This is because the comma is a delimeter at a higher level. Byngl

**Token Name:** IIF(HASEQUIP)

**What it does:**

True if the character has the listed equipment.

**Example:**

`IIF(HASEQUIP:Dagger)`

Would be true if character had a dagger.

**Token Name:** IIF(HASFEAT)

**What it does:**

True if the character has the listed feat.

**Example:**

`IIF(HASFEAT:Sneak Attack)`

Would be true if character has the Sneak Attack Feat.

**Token Name:** IIF(HASSA)

**What it does:**

True if the character has the listed Special Ability.

**Example:**

`IIF(HASSA:Greater Rage)`

Would be true if character has the Greater Rage Special Ability.

**Token Name:** IIF(HASVAR)

**What it does:**

True if the user has taken a class that defined the named (often used to
determine whether or not to display special abilities).

**Example:**

`IIF(HASVAR:BasePowerPoints)`

Would be true if character has a class with Base Power Points.

**Token Name:** IIF(SKILL.x.UNTRAINED)

**Variables Used (x):** Number (The array number of the skill).

**What it does:**

True if Skill x is usable untrained.

**Example:**

`IIF(SKILL.%skill.UNTRAINED)`

Would be true if the current skill is usable untrained.

**Token Name:** IIF(SKILL.UNTRAINED,x,y)

**Variables Used (x):** Text (Result if usable untrained).

**Variables Used (y):** Text (Result if usable trained).

**What it does:**

-   Prints out **x** if the skill is usable untrained or **y** if not
    usable untrained.
-   If **y** is not supplied, nothing is printed if trained only, and
    **x** is printed if usable untrained.
-   If neither **x** nor **y** are supplied, nothing is output and the
    output sheet wastes processor cycles.

**Example:**

`IIF(SKILL%.UNTRAINED,YES,NO)`

Prints out "YES" if the skill is usable untrained or "NO" if not usable
untrained.

**Token Name:** IIF(SKILL.ACP,w,x,y,z)

**Variables Used (w):** Text (Result if the skill is not affected by
ACP).

**Variables Used (x):** Text (Result if the skill is affected by ACP).

**Variables Used (y):** Text (Result if the skill is only affected by
ACP if the user is untrained).

**Variables Used (z):** Text (Result if the skill has the special weight
penalty like Swim).

**What it does:**

Tests for armor check penalty (ACP) interaction with this skill.

**Example:**

`IIF(SKILL%.ACP,NOT,IS,UNTRAINED,SWIM)`

Prints out "YES" if the skill is not effected by ACP, "NO" if the skill
is effected by ACP, "UNTRAINED" if the skill is effected by ACP only if
the character is untrained , "SWIM" if the skill is effected by ACP only
if it has a special weight penalty.

**Token Name:** IIF(SPELLCASTER:x)

**Variables Used (x):** Text (Caster Type - Possible values include
Wizard or Arcane).

**What it does:**

True if character is a spell caster of type specified.

**Example:**

`IIF(SPELLCASTER:Wizard)`

Would be true if the character is a Wizard.

**Token Name:** IIF(SPELLCASTER:x=PREPARE)

**Variables Used (x):** Number (The array number of the spellcaster
class).

**What it does:**

True if the characters spellcaster class **x** has to prepare spells.

**Example:**

`IIF(SPELLCASTER:0=PREPARE)`

Would be true if the character's 1st class prepares spells.

`IIF(SPELLCASTER:0=!PREPARE)`

Would be true if the character's 1st class does not prepare spells.

**Token Name:** IIF(WEAPON.x.CATEGORY:y)

**Variables Used (x):** Number (The array number of the weapon).

**Variables Used (y):** Text (Weapon Type - Possible values include:
Melee, Ranged, Exotic, Non-Standard-Melee).

**What it does:**

True if the weapon **x** is part of the category **y** .

**Example:**

`IIF(WEAPON.%weap.CATEGORY:Ranged)`

True if the current weapon is part of the Ranged category.

**Token Name:** IIF(x:=y)

**Variables Used (x):** Text (Any valid token or value).

**Variables Used (y):** Text (Any valid token or value).

**What it does:**

True if both tokens or values evaluate to the same value.

**Example:**

`IIF(COMBAT.AC.TOTAL:20)`

Would be true if the combat AC total was 20.

`IIF(ABILITY.Special Ability.%subability.ASPECT.ChildAbility:ABILITYAUTO.Special Ability.%ability.ASPECT.MasterAbility)`

This could occur inside a double loop, and would be true if the value of
the ChildAbility ASPECT of the ability represented by %subability is
equal to the value of the MasterAbility ASPECT of the ability
represented by %ability.

**Token Name:** IIF(x:y)

**Variables Used (x):** Text (Any valid token or value).

**Variables Used (y):** Text (Any valid token or value).

**What it does:**

True if token **y** evaluates to the same value or a substring of the
evaluation result of token **x** .

**Example:**

`IIF(COMBAT.AC.TOTAL:20)`

Would be true if the combat AC total was 20.

`IIF(ABILITY.Special Ability.%subability.ASPECT.ChildAbility:ABILITYAUTO.Special Ability.%ability.ASPECT.MasterAbility)`

This could occur inside a double loop, and would be true if the value of
the ChildAbility ASPECT of the ability represented by %subability is
equal to the value of the MasterAbility ASPECT of the ability
represented by %ability.

------------------------------------------------------------------------

**<span id="manualwhitespace"></span> Token Name:** MANUALWHITESPACE

`MANUALWHITESPACE          {Statements}          ENDMANUALWHITESPACE     `

**What it does:**

Marks a section where the author does not want white space added to the
output sheet. If white space is desired the |BR| tag can be used, or a
sheet format specific entry such as &nbsp; can be used in the sheet
definition.

Within a manual whitespace section, all whitespace in the output sheet
i.e. all newlines, spaces, tabs, etc. disappears. Whitespace inside the
text of returned from a OS token is preserved however. All leading and
trailing whitespace is trimmed, as is normally done.

**Example:**

`|MANUALWHITESPACE| 1&nbsp;          |PLAYERNAME|          2 3<br>          4          |ENDMANUALWHITESPACE|`

Where |PLAYERNAME| in this case is "Chuck Pint". Then the output would
look like:\
`1&nbsp;Chuck Pint23<br>4`

------------------------------------------------------------------------

**<span id="oif"></span> Token Name:** OIF(x,y,z)

**Variables Used (x):** Text (Condition to be evaluated).

**Variables Used (y):** Text (Value returned if True).

**Variables Used (z):** Text (Value returned if False).

**What it does:**

-   Provides conditional processing of expressions.
-   Will take [JEP boolean
    expressions](/list/global/formulas.html#boolean) as the
    conditional statement.
-   Only the expressions mentioned above for IIF are
    currently supported.

**Example:**

`OIF(HASFEAT:Armor Proficiency (Light),YES,NO)`

If the character has the Light Armor proficiency, then returns "YES".
Otherwise it returns "NO".

`OIF((CL>5)||(TL>5),YES,NO)`

Returns "YES" if Class Level or Total Level ar greater then 5. Oterwise
it returns "NO"

------------------------------------------------------------------------

**<span id="pipe"></span> Token Name:** PIPE

**What it does:**

Inserts a pipe ("|") character.

**Example:**

`Pipe|PIPE|Example`

Would display "Pipe|Example".

------------------------------------------------------------------------

\*\*\* New 5.15.7

**<span id="space"></span> Token Name:** SPACE

**What it does:**

Inserts a Space (" ") character. Normally only used on text output
sheets and inside manualwhitespace sections.

**Example:**

`Space|SPACE|Example`

Would display "Space Example".

------------------------------------------------------------------------

**<span id="sub"></span> Token Name:** SUBx.y

**Variables Used (x):** Number (Number of Text Characters)

**Variables Used (y):** Subtoken (OS Token)

**What it does:**

-   Limits the length of the string written to the output sheet to no
    more than x characters.
-   Must be the first subtoken.

**Example:**

`SUB10.SPELLMEM.0.0.0.0.COMPONENTS`

Would limit the output from the above tag to no more than 10 characters.

------------------------------------------------------------------------

**<span id="tempbonus"></span> Token Name:** TEMPBONUS.x.y

**Variables Used (x):** Number (Bonus index)

**Variables Used (y):** NAME (Name of the temporary bonus. Optional.
Default)

**Variables Used (y):** DESC (Description of the temporary bonus.)

**What it does:**

Outputs the designated temporary bonus information.

**Example:**

`|FOR,%temp,0,COUNT[TEMPBONUSNAMES]-1,1,0|`

`|TEMPBONUS.%temp|`

`|ENDFOR|`

------------------------------------------------------------------------

**<span id="text"></span> Token Name:** TEXT.x.y

**Variables Used (x):** LOWER

**Variables Used (x):** LOWERCASE

**Variables Used (x):** REPLACEALL

**Variables Used (x):** REPLACEFIRST

**Variables Used (x):** SENTENCE

**Variables Used (x):** SENTENCECASE

**Variables Used (x):** TITLE

**Variables Used (x):** TITLECASE

**Variables Used (x):** UPPER

**Variables Used (x):** UPPERCASE

**Variables Used (x):** NUMSUFFIX

**Variables Used (y):** Subtoken (OS Token)

**Variables Used (y):** Number

**What it does:**

Alters the output of the following OS token. For it to work it has to be
the first subtoken. The following are the subrags allowed and their
effect.

-   `LENGTH` - Returns the length of the string the specified
    token produces. (Mostly useful to test for 0 length strings)
-   `LOWER` , `LOWERCASE` - Output the tag result in lower case. e.g.
    the vitamins are in my fresh brussels sprouts
-   `NUMSUFFIX` - Output a numeric suffix appropriate for the
    tag result. e.g "th" or "rd"
-   `REPLACEALL` and `REPLACEFIRST` - Performs a regular expression
    based search and replace on the string produced by the
    associated token. Multiple replacements can be specified and are
    processed right to left. The proper syntax for these tags are as
    follows:
    -   `REPLACEALL{regexp,newtest}`
    -   `REPLACEFIRST{regexp,newtest}`
    -   When writing regular expressions you may need to use character
        substitution to get the results you are looking for. Examples:
        -   "\_\_LP\_\_" as the substitute for "{"
        -   "\_\_RP\_\_" as the substitute for "}"
        -   "\_\_PLUS\_\_" as the substitute for "+"
        -   Note: Help on regular expressions can be found at the [Java
            Platform SE6
            Pattern](http://docs.oracle.com/javase/6/docs/api/java/util/regex/Pattern.html) page.
-   `SENTENCE` , `SENTENCECASE` - Output the tag result in
    sentence case. e.g. The vitamins are in my fresh brussels sprouts
-   `TITLE` , `TITLECASE` - Output the tag result in title case. e.g.
    The Vitamins Are In My Fresh Brussels Sprouts
-   `UPPER` , `UPPERCASE` - Output the tag result in upper case. e.g.
    THE VITAMINS ARE IN MY FRESH BRUSSELS SPROUTS

**Example:**

`TEXT.LOWER.SPELLMEM.%class.0.%level.%spell.NAME`

Would output the name for the spell in lower case.

`TEXT.REPLACEFIRST{\.0,}.SKILL.%skill.RANK`

Would output "5" instead of "5.0" but would leave "5.5" as is.

`TEXT.NUMSUFFIX.22`

Would output a suffix of "nd" rather than the value 22.

------------------------------------------------------------------------

**<span id="var"></span> Token Name:** VAR.x

**Variables Used (x):** Text (Any defined variable name).

**What it does:**

-   Displays the value of a defined variable.
-   The default is with one decimal place of precision (i.e. x.x).
-   You can also append .INTVAL as an optional argument which displays
    the result with no decimal points (as an integer).
-   It is possible to define the Turn Undead variable more than once.
    The program keeps track of this. (say one instance is 2 and the
    other 4).
-   Also `.MINVAL` should be included if instead of the default maximum
    of multiple defines, you want the minimum.

**Example:**

`VAR.Turn Undead.MINVAL.INTVAL`

Would return 2.

`VAR.Turn Undead.INTVAL`

Would return 4.

`VAR.Turn Undead.MINVAL`

Would return 2.0.

`VAR.Turn Undead`

Would return 4.0.

------------------------------------------------------------------------



