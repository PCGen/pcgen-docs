+++
date = "2016-08-01"
title = "Math Operators and Formulas"
original_url = "/list/global/formulas.html"

[menu.main]
    identifier = "global_formulas"
    name = "Math Operators and Formulas"
    parent = "global"
    
+++
**Important:** Starting with version 5.7.1 PCGen has incorporated the
[JEP (Java Mathematical Expression Parser)
library](http://www.singularsys.com/jep/) . This was done because the
original code which has evolved over time is problematic due to its
complexity and lack of documentation. The JEP library has a clearly
defined grammar which is available on the web site. JEP supports user
defined variables, constants, and functions. A number of common
mathematical functions and constants are included. As a fall back, if
the JEP parser fails to parse the function then the old code is called.
At some point in the future the old code support will be dropped and all
formulas must be in JEP syntax.

The library we are using to parse math expressions defines the syntax
they want to test for string equality. If you are curious you can check
out the JEP library at [Singular Sys](http://www.singularsys.com/jep/)

To reverse the sign (go from positive number to negative) use -1\*().
EXAMPLE:

`BONUS:CHECKS|BASE.Will|CL/3` is a positive 1 at 3rd level and

`BONUS:CHECKS|BASE.Will|-1*(CL/3)` is a -1 at 3rd level.

***PCGen \*does\* round each tag down rather than add the tags together
and then round down. See example before 'Operators'***

**Using variables within JEP expressions**

In most cases variables can be used directly in an expression, however
there are some cases when you must use the var() function. This is
because some variables can contain characters which are not valid JEP
variables. For example the variable CL can be used in a formula without
a problem but the variable CL=Fighter cannot be used because of the "="
symbol. In these cases you must use var("CL=Fighter") in the formula for
it to parse correctly. The formal description of a JEP variable is "a
letter followed by one or more letters and digits" where a letter is
defined as: '\$', '\_', a-z and A-Z.\
\

Examples of variables that may be used alone:

`CL, TL, ARMORACCHECK, BardicKnowledgeLevel, TirelessRage.` ,

Examples of variables that must be called with the getvar() function:

`var("CL=Fighter"), var("COUNT[FEATS]"), var("COUNT[FEATTYPE=type]").`

Consult the [DEFINE](/list/global/define.html) page for the list of hard
coded variables available for use in formulas.

**Operator order of processing:**

Anything within ()'s are done first, and processing is done
left-to-right.

`2+(3*5+2)/2`

Would become 2+(15+2)/2 (3\*5 replaced)

then 2+17/2 (15+2 replaced)

then 19/2 (2+17 replaced)

then 9 (result of 19/2, the .5 is dropped, see below.).

**PCGen truncates (or rounds down to the nearest integer) the results of
each formula,** so 4/3 will return a 1 and 7/3 will return a 2 etc. If
you need to truncate within the formula you can use the min(x,y) or
max(x,y) and floor(a) or ceil(a) tags.

------------------------------------------------------------------------

<span id="operators"></span>

Operators
---------

<span id="mathoperators"></span>

#### Mathematical Operators

**Addition:** `x+y`

**Subtraction:** `x-y`

**Division:** `x/y`

**Multiplication:** `x*y`

> **Variable Used (x):** Number, Variable, or Formula
>
> **Variable Used (y):** Number, Variable, or Formula
>
> **What They Do:**
>
> -   These are the four traditional mathematical operators.
> -   Order of Operation:
>     -   For JEP Commands - Per standard mathematical order
>         of operation. (i.e. Parenthises -&gt; Multiplication/Division
>         -&gt; Addition/Subtraction)
>     -   For Non-JEP Commands - Parenthesis are resolved first, then
>         operators will be processed from left to right.
>     -   Parenthesis may be nested with the inner-most parenthesis
>         being processed first.
>
> **Examples:**
>
> `2+1`
>
> Returns a value of 3.
>
> `CL-1`
>
> Returns a value equal to the Class Level minus 1.
>
> `CL/2`
>
> Returns a value equal to the Class Level divided by 2.
>
> `CL*3`
>
> Returns a value equal to the Class Level multiplied by 3.
>
> `((CL+1)+(3*TL)/2)+4` (JEP Expression)
>
> Returns the result of three multiplied by Total Level divided by two,
> plus Class Level plus 1, plus four. Assuming CL=TL=4, this expression
> returns 15.
>
> `((CL+1)+(3*TL)/2)+4` (Non-JEP Expression)
>
> Returns the result of Class Level plus 1, plus three multiplied by
> Total Level, divided by two, plus four. Assuming CL=TL=4, this
> expression returns 12.

------------------------------------------------------------------------

<span id="boolean"></span>

#### Boolean Operators

**Equal:** `x==y`

**Not Equal:** `x!=y`

**Greater Than:** `x>y`

**Less Than:** `x<y`

**Greater Than or Equal:** `x>=y`

**Less Than or Equal:** `x<=y`

**Logical AND:** `x&&y`

**Logical OR:** `x||y`

> **Variable Used (x):** Number, Variable, or Formula
>
> **Variable Used (y):** Number, Variable, or Formula
>
> **What They Do:**
>
> Boolean expressions are evaluated to be either 1 or 0 (true or false
> respectively).
>
> **Examples:**
>
> `CL==1`
>
> Will return "True" if Class Level is equal to 1.
>
> `CL!=1`
>
> Will return "True" if Class Level is not equal to 1.
>
> `CL>1`
>
> Will return "True" if Class Level is greater than 1.
>
> `CL<1`
>
> Will return "True" if Class Level is less than 1.
>
> `CL>=1`
>
> Will return "True" if Class Level is greater than or equal to 1.
>
> `CL<=1`
>
> Will return "True" if Class Level is less than or equal to 1.
>
> `(CL>5)&&(TL>5)`
>
> Will return "True" if Class Level **and** Total Level are greater than
> 5.
>
> `(CL>5)||(TL>5)`
>
> Will return "True" if Class Level **or** Total Level is greater than
> 5.

------------------------------------------------------------------------

<span id="symboloperators"></span>

#### Symbol Operators

<span id="percentchoice"></span>

**Choice:** `%CHOICE`

> **What it does:**
>
> The %CHOICE will put the input from a CHOOSE tag into its place.
>
> **Where it is used:**
>
> -   In conjunction with the CHOOSE tag.
> -   May be used within math computations.
>
> **Example:**
>
> `SPROP:Unreliable (%CHOICE) <tab> CHOOSE:5%|10%|15%|20%|25%|30%|35%|40%|45%|50%|55%|60%|65%|70%|75%|80%|85%|90%|95%|100%`
>
> Chooser to select the level of unreliablty.

<span id="percentlist"></span>

**List:** `%LIST`

> **What it does:**
>
> The %LIST will put the input from a CHOOSE tag into its place.
>
> **Where it is used:**
>
> -   In conjunction with the CHOOSE tag.
> -   May not be used within math computations.
>
> **Example:**
>
> `CHOOSE:NUMCHOICES=1|FORTITUDE|REFLEX|WILL <tab> BONUS:CHECKS|%LIST|1`
>
> Will insert the "Choice" made in the "CHOOSE:" tag into the "Bonus"
> tag and apply the bonus of "1" to the chosen "Checks" bonus.

<span id="exclamation"></span>

**Not:** `!`

> **What it does:**
>
> Performs a logical NOT operation.
>
> **Example:**
>
> `BONUS:SKILL|Swim|1|!PRESKILL:1,Swim=1.`
>
> If the character does not have swim, add 1 to it.

<span id="percent"></span>

**Replacement/Substitution:** `%`

> **What it does:**
>
> The Replacement/Substitution Operator is used in the
> [SAB](/list/global/other/sab.html) tag.
>
> **Example:**
>
> `SAB:Resistance to % 5|MyFooVariable`
>
> Will substitute the value of "MyFooVariable" for the "%" in the
> [SAB](/list/global/other/sab.html) tag.

------------------------------------------------------------------------

Formulas/Functions
------------------

**Modulus/Remainder**

**Formula:** `x%y`

> **Variables Used (x):** Variable (Dividend)
>
> **Variables Used (y):** Number (Divisor)
>
> **What it Does:**
>
> Performs a modulus, returning the remainder for the operation.
>
> **Examples:**
>
> `CL%3`
>
> Divides the character's class level by 3 and returns the remainder
>
> If the class level was 7, the remainder is 1.

------------------------------------------------------------------------

<span id="minmax"></span>

**Minimums and Maximums (JEP Expression)**

**Formula:** `min(x,x)` or `max(x,x)`

> **Variables Used (x):** Number, Variable, or Formula (Value list)
>
> **What it Does:**
>
> -   Returns the lowest (min) or highest (max) value from the
>     value list.
> -   The value list is a comma-delimited (",") list of values to
>     be compared.
> -   The value-list may contain any number of values desired.
>
> **Exqmples:**
>
> `min(10,CL,TL/2)` given a multi-class character: Wiz8/Ftr6 and looking
> at it from the Wizard's perspective.
>
> Evaluating: min(10,\[CL=8\],\[TL/2 -&gt; (8+6)/2 -&gt; (14/2)=7\])
> -&gt; min returns the value "7".
>
> `max(3,CL,TL/2)` given a multi-class character: Wiz4/Rog6 and looking
> at it from the Rogue's perspective.
>
> Evaluating: max(3,\[CL=6\],\[TL/2 -&gt; (4+6)/2 -&gt; (10/2)=5\])
> -&gt; max returns the value "6".

------------------------------------------------------------------------

<span id="truncation"></span>

**Truncation, Rounding Up or Down (JEP Expression)**

**Formula:** `floor(x)` or `ceil(x)`

> **Variables Used (x):** Number, Variable, or Formula
>
> **What it Does:**
>
> The function "floor" returns the highest integer that is less than
> 'x'.
>
> The function "ceil" returns the lowest integer that is greater than
> 'x'.
>
> **Examples:**
>
> `floor((FooVariable+4)/6)` Assume FooVariable is "7"
>
> Evaluate: (FooVariable+4)/6 -&gt; (7+4)/6 -&gt; 11/6 -&gt; 1 5/6 -
> &gt; floor returns 1.
>
> `ceil(STR/2)` Assume STR=15
>
> Evaluate: STR/2 -&gt; 15/2 -&gt; 7 1/2 -&gt; ceil returns 8.

------------------------------------------------------------------------

<span id="booleanif"></span>

**Boolean If**

**Formula:** `if(x,y,z)`\

> **Variable Used (x):** Formula (Boolean expression)
>
> **Variable Used (y):** Number (Result if True)
>
> **Variable Used (z):** Number (Result if False)
>
> **What it Does:**
>
> -   The boolean "if" operator will return one of two results after
>     evaluating a boolean expression.
> -   When evaluating the boolean expression, any result beside "0"
>     is "True".
> -   If the boolean expression (x) is "True", i.e. not equal to "0",
>     the "True" result (y) is returned.
> -   If the boolean expression (x) is "False", i.e. equal to "0", the
>     "False" result (z) is returned.
>
> **Examples:**
>
> `if(CL<10,1,2)`
>
> Asks if Class Level is less than 10 then returns 1 or else returns 2.
>
> `if(CL>=4,10,0)`
>
> Asks if Class Level is greater than or equal to 4 then returns 10 or
> else returns 0.
>
> `if((CL>5)||(TL>5),2,-4)`
>
> Asks if Class Level **or** Total Level is greater than 5 then returns
> 2 or else returns -4.
>
> `if(STR,5,0)`
>
> Asks if Strength modifier is greater than or less than 0 then returns
> 5 or else returns 0.

------------------------------------------------------------------------

<span id="randomnumbers"></span>

#### Random Number Generation (JEP Expression)

**Formula:** `roll("x")`

> **Variables Used (x):** Formula (JEP formula or "xdx")
>
> **What it Does:**
>
> -   The formula used within the roll("x") function can use all the
>     standard JEP operators and in addition it can take a dice
>     expression in the form of xdx, for example 2d6, 1d20 and 3d4.
> -   The following functions are also supported within the roll
>     function and must be encapsulated in a roll("x") call to function
>     properly:
>     -   `min(v1,v2)`
>     -   `max(v1,v2)`
>     -   `pow(base, exponent)`
>     -   `roll(times, sides)`
>     -   `roll(times, sides, [keep])`
>     -   `roll(times, [sides])`
>     -   `roll(times, [sides], [keep])`
>
> <span class="new"> **Warning:** </span>
>
> Although the JEP function roll("x") can generate a random number in
> any formula that takes JEP there are few places in the program where
> this is actually useful. This is because the roll function will
> generate a new random number every time the formula is evaluated which
> happens many times while you use the program. So if you were to use
> roll("2d6") in a base attack bonus it would appear to add a number
> between 2 and 12 which would change frequently. Currently the QTY tag
> used [FUNDS](/list/data/startingkits/funds.html) lines in Kit files is
> one of the few places this JEP operator functions in a useful way.
>
> **Examples:**
>
> `roll("3d6")`
>
> Simulates rolling 3 six-sided dice.
>
> `roll("1d20+10")`
>
> Simulates rolling a twenty-sided die and adds 10.
>
> `roll("min(4,7)")`
>
> Returns a value of "4".
>
> `roll("max(4,7)")`
>
> Returns a value of "7".
>
> `roll("pow(10,2)")`
>
> Returns a value of "100".
>
> `roll("roll(3,6)")`
>
> Simulates rolling 3 six-sided dice.
>
> `roll("roll(4,6,[2,3,4])")`
>
> Simulates rolling 4 six-sided dice and keeps the 3 highest rolls.
>
> `roll("roll(1,[3,5,7,9])")`
>
> Similates rolling one 3, 5, 7 or 9 sided die, randomly selected.
>
> `roll("roll(3,[2,3,4,5,6],[2,3])")`
>
> Simulates rolling three 2, 3, 4, 5, or 6 sided dice, randomly selected
> and keeps the highest 2.

------------------------------------------------------------------------

<span id="classlevel"></span> \*\*\* Updated 6.03.04

**Class Level (JEP Expression)**

**Formula:** `classlevel("x")`

> **Variables Used (x):** Text (Class name)
>
> **Variables Used (x):** TYPE=Text (Class type)
>
> **Variables Used (x):** APPLIEDAS=NONEPIC
>
> **What it Does:**
>
> -   This function returns the number of level the PC has in the
>     specified class.
> -   When specifying a <span class="lstobj"> Class </span> by `TYPE` ,
>     use of a period-delimited list of types will return the level of
>     the <span class="lstobj"> Class </span> that is of all
>     types listed.
>
> **Examples:**
>
> `classlevel("Bard")`
>
> Returns the number of levels of <span class="lstobj"> Bard </span> .
>
> `classlevel("TYPE=PC.Prestige")`
>
> Returns the number of levels of the class of types <span
> class="lstobj"> PC </span> and <span class="lstobj"> Prestige </span>
> .
>
> `classlevel("APPLIEDAS=NONEPIC")`
>
> Returns the number of levels of applied as non-epic levels.
>
> **Deprecated Syntax:**
>
> `CL=<Bard>`

------------------------------------------------------------------------

<span id="skillinfo"></span> \*\*\* Updated 5.17.5 - Added STAT and MISC
properties.

**Skill Information (JEP Expression)**

**Formula:** `skillinfo("x","y")`

> **Variables Used (x):** RANK (Property)
>
> **Variables Used (x):** TOTALRANK (Property)
>
> **Variables Used (x):** MODIFIER (Property)
>
> **Variables Used (x):** STAT (Property)
>
> **Variables Used (x):** MISC (Property)
>
> **Variables Used (x):** TOTAL (Property)
>
> **Variables Used (y):** Text (Skill name)
>
> **What it Does:**
>
> This function returns information about the skill specified.
>
> -   RANK returns the number of ranks the PC has in the skill not
>     including those gained from BONUS:SKILLRANK tags.
> -   TOTALRANK returns the number of ranks the PC has in the skill
>     including those gained from BONUS:SKILLRANK tags.
> -   MODIFIER returns the total bonuses the PC has in the skill.
> -   STAT returns the bonus the PC has in the skill from his
>     abilityattribute bonus.
> -   MISC returns the total bonuses the PC has in the skill that do not
>     derive from his ability bonus.
> -   TOTAL returns the grand total in the skill from all ranks
>     and bonuses.
>
> **Examples:**
>
> `skillinfo("RANK", "Hide")`
>
> Returns the number of base ranks in Hide.
>
> `skillinfo("TOTALRANK", "Climb")`
>
> Returns the number ranks in Climb including those gained from
> BONUS:SKILLRANK tags.
>
> `skillinfo("MODIFIER", "Bluff")`
>
> Returns the total number of bonuses in Bluff.
>
> `skillinfo("STAT", "Diplomacy")`
>
> Returns the ability bonus for Diplomacy.
>
> `skillinfo("MISC", "Use Magic Device")`
>
> Returns the total miscellaneous bonuses in Use Magic Device.
>
> `skillinfo("TOTAL", "Spellcraft")`
>
> Returns the grand total in Spellcraft.

------------------------------------------------------------------------

<span id="charbonusto"></span>

**Character Bonus Information (JEP Expression)**

**Formula:** `charbonusto("x","y")`

> **Variable Used (x):** Text (Parameter 1 - Optional)
>
> **Variable Used (x):** Text (Parameter 2)
>
> **What it Does:**
>
> -   This function returns the value of the identified parameter pair.
> -   These values reflect only the bonuses applied to the parameter
>     identified and not the total value of that parameter.
> -   Valid parameter pairs (x - y) include:
>     -   PCLEVEL - &lt;class name&gt;
>     -   STAT - BASESPELLSTAT
>     -   STAT - BASESPELLSTAT;CLASS.&lt;class named&gt;
>     -   STAT - CAST.&lt;spell type&gt;
>     -   FEAT - POOL
>     -   VAR - &lt;variable name&gt;
>     -   CHECKS - &lt;check type&gt;
>     -   TOHIT - TOHIT
>     -   DOMAIN - NUMBER
>     -   CASTERLEVEL - &lt;class name&gt;
>     -   HP - ALTHP
>     -   COMBAT - BAB
>     -   WEAPONPROF=&lt;weapon name&gt; - PCSIZE
>     -   WEAPONPROF=TYPE.&lt;weapon proficency&gt; - PCSIZE
> -   Parameter 1 (x) is optional. If it is not present, it will default
>     to "PCLEVEL".
>
> **Examples:**
>
> `charbonusto("PCLEVEL","Cleric")`
>
> Returns the number of bonus Spellcaster Levels to the class specified,
> which usually come from Prestige classes.
>
> `charbonusto("CHECKS","Reflex")`
>
> Will return Reflex bonuses from a high Dexterity and other bonuses but
> not the full reflex save value.

------------------------------------------------------------------------

<span id="count"></span> \*\*\* Updated 6.01.09 - Added CAMPAIGNHISTORY
property.

**Count (JEP Expression)**

**Formula:** `count(x,y)`

> **Variables Used (x):** Text (Object to be counted)
>
> **Variables Used (y):** Text (Matching criteria)
>
> **What it does:**
>
> -   This token is used to obtain the number of objects matching the
>     provided criteria.
> -   The matching criteria are a comma-delimited (,) list of quotated
>     parameters ("parameter=text") associated with the "Object"
>     being counted.
> -   " `[and]` " and " `[or]` " can be used between parameters.
> -   Use of this token in conjunction with output sheet tokens `IIF`
>     and `VAR` require a semicolon-delimited (;) list of quotated
>     parameters instead of a comma-delimited list.
> -   This token can be used in any of the OS FOR loops in place of max.
> -   Valid &lt;Object to be counted&gt; and the associated &lt;Matching
>     criteria&gt; are listed below:
>     -   `ABILITIES` - Will count the abilities that satisfy the
>         following criteria:
>         -   `"CATEGORY=<text>"` - The ability category as defined in
>             the *gamemode/miscinfo.lst* file or the
>             *data/abilitycategory.lst* file.
>         -   `"NAME=<text>"` - The name of a specific Ability which can
>             be taken multiple times, returns the number of times it
>             was taken. For abilities with internal choices you include
>             the specific choices to be counted within
>             parenthesis, i.e. Weapon Focus (Longsword).
>         -   `"KEY=<text>"` - The key of a specific Ability which can
>             be taken multiple times, returns the number of times it
>             was taken. For abilities with internal choices you include
>             the specific choices to be counted within
>             parenthesis, i.e. Weapon Focus (Longsword).
>         -   `"NATURE=<text>"` - "NORMAL", "VIRTUAL", or "AUTOMATIC".
>         -   `"TYPE=<text>"` - The ability type as defined in the
>             ability.lst file. (e.g. "General", "Fighter",
>             "Metamagic", etc.)
>         -   `"VISIBILITY=<text>"`
>             -   "HIDDEN", includes abilities with VISIBLE:NO
>             -   "DEFAULT", includes abilities with VISIBLE:YES or no
>                 VISIBLE tag at all
>             -   "OUTPUT\_ONLY", includes abilities with VISIBLE:EXPORT
>             -   "DISPLAY\_ONLY", includes abilities with
>                 VISIBLE:DISPLAY
>         -   `"ASPECT=<text>"` - The aspect as defined for the ability
>             objects in the ability.lst file.
>
>         \
>     -   `CAMPAIGNHISTORY` - Will count the number of entries in the
>         character's campaign history page.
>     -   `CLASSES` - Not yet implemented.
>     -   `DOMAINS` - Not yet implemented.
>     -   `EQUIPMENT` - Not yet implemented..
>     -   `FOLLOWERS` - Not yet implemented..
>     -   `LANGUAGES` - Not yet implemented.
>     -   `RACESUBTYPES` - Not yet implemented.
>     -   `SKILLSIT` - Will count skills/situations that satisfy the
>         stipulated criteria (y) as `"VIEW=<text>"` . Valid views are
>         as per tag TBD .
>     -   `SPELLBOOKS` - Not yet implemented.
>     -   `SPELLS` - Not yet implemented.
>     -   `SPELLSKNOWN` - Not yet implemented.
>     -   `SPELLSINBOOK` - Not yet implemented.
>     -   `TEMPLATES` - Not yet implemented.
>
> **Example:**
>
> `count("ABILITIES","CATEGORY=FEAT","TYPE=Metamagic","VISIBILITY=DEFAULT[or]VISIBILITY=OUTPUT_ONLY")`
>
> This token returns the number of visible metamagic feats the character
> has.
>
> `count("ABILITIES","CATEGORY=FEAT","TYPE=Fighter","VISIBILITY=DEFAULT[or]VISIBILITY=OUTPUT_ONLY")`
>
> Returns the number of all visible Fighter type feat abilities.
>
> `count("ABILITIES","CATEGORY=FEAT","NAME=Toughness")`
>
> Returns the number of times the Toughness feat was taken.
>
> `count("ABILITIES","CATEGORY=FEAT","KEY=Toughness")`
>
> Returns the number of times the Toughness feat was taken.
>
> `count("ABILITIES","CATEGORY=Special Ability","NATURE=VIRTUAL[or]NATURE=AUTOMATIC")`
>
> Returns the number of abilities of category "Special Ability" the
> character has which are either virtual or automatic.
>
> `count("ABILITIES","CATEGORY=FEAT","VISIBILITY=HIDDEN[or]VISIBILITY=DISPLAY_ONLY")`
>
> Returns the number of hidden feats.
>
> `|VAR.count("ABILITIES","CATEGORY=Maneuver")|`
>
> Outputs the number of "Maneuver" abilities the character has.
>
> `count("CAMPAIGNHISTORY")`
>
> This token returns the number of campaign history chronicles marked as
> being for export.
>
> `count("CAMPAIGNHISTORY", "EXPORT=YES[or]EXPORT=NO")`
>
> This token returns the number of campaign history chronicles no matter
> how they are marked.

------------------------------------------------------------------------

<span id="isgamemode"></span> \*\*\* New 5.15.x

**isGameMode (JEP Expression)**

**Formula:** `isgamemode("x")`

> **Variables Used (x):** Text (GameMode name)
>
> **What it Does:**
>
> This function tests to see if the designated "gameMode" is running. It
> returns a "1" if the designated gameMode is running and a "0" if it is
> not.
>
> **Examples:**
>
> `isgamemode("35e")`
>
> Returns a "1" if the designated gameMode is running and a "0" if it is
> not.

------------------------------------------------------------------------

<span id="mastervar"></span> \*\*\* New 6.03.x

**mastervar (JEP Expression)**

**Formula:** `mastervar("x")`

> **Variables Used (x):** Text (Varuable Name)
>
> **What it Does:**
>
> This function used by a "companion" creature and returns the value of
> the designated variable attached to the relevant companion's Master
> PC.
>
> **Examples:**
>
> `mastervar("BAB")`
>
> Returns the base attack bonus of the relevant companion's Master PC.

------------------------------------------------------------------------

<span id="rollinfo"></span> \*\*\* New 6.01.02

**Roll Info**

**Formula:** `xdyz`

> **Variables Used (x):** Integer (Number of dice)
>
> **Variables Used (y):** Integer (Number of sides)
>
> **Variables Used (z):** +Integer (Modifier)
>
> **Variables Used (z):** -Integer (Modifier)
>
> **What it Does:**
>
> -   This formula syntax provides
>
> **Examples:**
>
> `4d8+5`
>
> Returns a number between 9 and 37.
>
> **Where it is Used:**
>
> `DAMAGE` and `ALTDAMAGE` tags.

------------------------------------------------------------------------

<span id="deprecatedoper"></span>

Deprecated Functions
--------------------

The following operators are deprecated as of version 5.7.1. The syntax
will be replaced with JEP syntax.

`((TL/3).TRUNC)*2`

Truncation - would divide TL by 3, truncate (or round down) and then
multiply by 2.

Deprecated, use floor(a).

`2MIN4`

Minimum - would return 2 since it's taking the minimum of the two values
(MIN is always between the values).

Deprecated, use min(a,b).

`2MAX4`

Maximum - would return 4 since it's the max of the two values (MAX is
always between the values).

Deprecated, use max(a,b).

------------------------------------------------------------------------



