+++
date = "2016-08-01"
title = "Creating Character Sheet Templates"
original_url = "/outputsheet/tutorial.html"

[menu.main]
    identifier = "outputsheet_tutorial"
    name = "Creating Character Sheet Templates"
    parent = "outputsheet"
    
+++
Preface
-------

This guide is in the main going to focus on using the tokens effectively
and appropriately. For simplicity, we will primarily use HTML examples,
some of which may be fairly complicated.

If you need help with HTML or XML/XSL you should visit
[http://www.w3c.org](http://www.w3c.org/) and read their tutorials. For
information about FOP (.fo file processing), visit
[http://www.apache.org](http://www.apache.org/) .

After going over the basics, I will be taking you through the steps I
used to create a sheet to display a character's weapons and equipment.

Introduction
------------

You will need to have a basic understanding of how PCGen uses character
sheet templates to create them.

When you "Export" a character, the program will ask you which template
you would like to use. PCGen starts by reading that template into
memory. PCGen scans for special character sets called "tokens" as it
reads the template. These tokens represent various bits of information
about the character you are exporting. When PCGen encounters one of
these tokens, it retrieves the information from the character file and
inserts the information into the spot where the token was. PCGen writes
the file out to disk with the information in place of the tokens once it
has completely loaded the file.

A sample line in an HTML template file might be:

`<i>Character Name:</i> |NAME|`

If you open the template with an HTML browser you would see:

*Character Name:* |NAME|

When you open the output file after exporting a character named "Mad
Monkey Mynex" using that template you would see:

*Character Name:* Mad Monkey Mynex

The bodies of the templates themselves can be done in HTML or XML/XSL:FO
for PDF. In either case, the tokens used to get information from PCGen
into the sheet are the same. A word of warning: PCGen only changes the
token, nothing else. If you put in bad HTML or XML/XSL code, bad HTML or
XML/XSL code will come out.

The first and most important thing I want to stress is to read the
documentation on the individual output tokens. Then read them again.
There are many subtleties in the use of the tokens contained there that
cannot be covered in a quick walkthrough.

Through some frustrating trial and error when I began doing character
sheets for PCGen, I learned a few important things regarding basic
Character Sheet design:

1.  Decide on a specific purpose/use for your template. There are LOTS
    of tokens and there is no need to try and use them all.\
2.  Figure out what's going to go on the sheet. Are you just going to
    show the main AC? Are you going to want to show all the modifiers
    that make up the total AC? Do you want spell lists? Etc.\
3.  Identify most of your tokens beforehand. Once you have decided what
    you want on the sheet, it's time to start figuring out what tokens
    you need to use. It is easiest to sketch a simple layout on a sheet
    of paper and fill in what tokens go where so you have a
    quick reference. You don't have to get them all right now, but it is
    very helpful to have them right there so you don't have to go
    digging around through the documentation looking for the proper
    token when you're actually trying to type in the sheet.
4.  Remember that tokens do not like whitespace in front of them! It
    will make your sheets go wonky, without you knowing why...\

Tokens
------

Now down to the true nuts and bolts, the tokens. First, some general
notes:

1.  All tokens are CAPITALIZED. There may be variables or options that
    are not, but the token itself will be.\
2.  All tokens are delimited (set apart) from the rest of the text on
    the character sheets by either the | (pipe) character, a \\
    (single backslash) or a \\\\ (double backslash), depending on where
    the token is used. There are no spaces between the beginning and end
    of the token and the delimiter characters. The token documentation
    has the delimiter characters left out for ease of reading\
3.  Some tokens output a single item, some output comma delimited
    lists.\
4.  Not all tokens make PCGen output something. Some are control
    commands that make comparisons, cause loops or apply filters. We
    will discuss these shortly.\
5.  Many tokens use variables so you can get at certain aspects.
    Variables come immediately after the token with a period "."
    between them. For example the token `EXPORT` can provide date and
    time information on a sheet using `EXPORT.DATE` and `EXPORT.TIME` .
    The variables that may be used with each token are listed in the
    output sheet token documentation. Not all variables are capitalized.
    Some numeric variables start at zero (0) but those should be noted
    in the documentation for the token.

Control Tokens
--------------

### Filter Tokens

The first and easiest to understand of the control tokens are the filter
tokens. These are used to stop the normal output if the filter condition
is not met. Filters all begin with a % (percent) sign and will run from
the moment they are invoked until they encounter a different filter or
until they encounter the end of filter token, which is a single % symbol
(E.g. `|%|` ) In case this wasn't clear, what it essentially means is
that one, and only one, filter may be active at any time. Nested filters
are not supported.

The simplest ones are in the form `|%TOKEN|` . Here PCGen simply checks
to see if the character has the appropriate data. A good use of these
simple filters is to suppress spell list blocks for non-spellcasters so
you can use the same character sheet for both types of characters and
not have an empty spell list cluttering things up for a non-spellcaster.
Examples of these types of tokens would be `|%SPELLISTBOOK|` or `|%BIO|`
.

Some slightly more complex filters are in the form of `|%ARMORx|` and
`|%WEAPONx|` . In these filters x represents the number of appropriate
items (armor type or weapon type for the above examples) that the
character must have in order for the filter to allow output. For
example: `|%WEAPON3|` means that there would be no output after the
filter until it reaches the next filter or filter end token unless the
character has at least three weapons. If the character has three weapons
the output would proceed as normal.

The next form a filter may take is that of classname=level or
SPELLLISTCLASSx=level. For example, `|%BARD=3|` would filter output if
the character did not have at least three Bard levels.
`|%SPELLLISTCLASS0=2|` would filter output if the character did not have
at least two levels in his first spellcasting class. `SPELLLISTCLASS` is
one of the tokens that starts at zero as mentioned earlier. These
filters are usually used to put class specific information on a sheet
and keep it from appearing unless you are of the appropriate class and
level. (Barbarian Rage is a good example here).

The final form of filter is one that uses variables. They all start with
%VAR and take the form of `|%VAR.name.label.value|` . The "name" is the
name of any variable that has been set up in the LST files using the VAR
tag. The label is a comparator and must be one of the following:

-   `EQ` (equals).
-   `NEQ` (not equal).
-   `LT` (less than).
-   `LTEQ` (less than or equal to).
-   `GT` (greater than).
-   `GTEQ` (greater than or equal to).

An example using the variable TOTALPOWERPOINTS defined in a LST from the
Psionic Handbook would be: `|%VAR.TOTALPOWERPOINTS.GTEQ.1|` . This would
filter output unless the variable TOTALPOWERPOINTS was greater than or
equal to 1.

All of the available filters are listed in the output sheet token
documentation with the exception of the VAR ones which are too numerous
to include since every VAR in every LST can be used as a filter.

### Count Tokens

The second special token is the COUNT token. This token also takes a
variable, but in a slightly different form. The variable for the COUNT
token goes inside a set of \[\] (square brackets). This token returns
the number of items of the variable type given. `|COUNT[CLASSES]|` would
return the number of classes a character has. While this has some
limited use as an actual output token, these tags are more often used to
set the lower or upper limit in a FOR loop, which will be explained
shortly.

All of the available variables for the COUNT token are listed in the
output sheet token documentation.

### IF Tokens

The next set tokens in our review of control tokens are the IIF/OIF
tokens. The simpler of the two is the OIF token. It is used to evaluate
an expression and return a value (text or number). This token is in the
form `|OIF(expr,true,false)|` . There are only certain expressions that
may be used, and they are listed in the output sheet token
documentation. The "true" and "false" parts may be anything you want
them to be. `|OIF(SPELLCASTER0=PREPARE,Yes,No)|` would return "Yes" if
the character's first spellcasting class had to prepare spells and "No"
if it didn't.

The IIF token has a much broader range and does not return output
itself. The IIF statement takes the form of:

`|IIF(expr)|`

`<true actions>`

`|ELSE|`

`<false actions>`

`|ENDIF|`

The IIF token, like the OIF token, can only take the expressions listed
in the output sheet documentation as usable with IF tokens. The power of
this token is in the ability to perform a whole series of actions based
upon the evaluation of the expression. An example of the IIF token could
be:

`|IIF(SKILL0.UNTRAINED)|`

`*`

`|ELSE|`

`x`

`|ENDIF|`

This bit would check to see if your first skill (SKILL0) is usable
untrained. If the skill is, it outputs an "\*" otherwise it outputs an
"x".

\*\*\* Update - Additional functionality has been added so that you may
compare (exact match only) the result of **any** token to an expected
result. AND and OR functionality has also been added.

`|IIF(SPELLLISTCLASS.%class:Psychic Warrior.OR.SPELLLISTCLASS.%class:Psion)|`
would trigger if the class number represented by %class was either a
Psychic Warrior OR a Psion.

### Loop Tokens

The last set of control tokens we need to cover are the FOR/DFOR tokens.
These tokens provide loop capabilities for creating lists on character
sheets. These lists can include equipment, classes, skills, spells, etc.

The FOR loops come in three forms. The format of the first is:

`|FOR,%var,min,max,step,exists|`

`<character sheet stuff>`

`|ENDFOR|`

In this token, %var is a variable name that you assign when you create a
loop. It should not/cannot be the same as a variable defined in a LST by
the VAR tag.

Whenever you use that variable within that loop, it will be evaluated
and return the current iteration number. The min and max values are the
start and end points for the loop. It is normal to start the loops at
zero because most of the arrays in PCGen are zero indexed.

You may also use a COUNT statement here, or any token that returns a
number. You may use the `COUNT[xxx]` token in the max field to tell the
loop when to stop, or any token that normally returns a number. The step
field is how much you want it to increment the variable each time it
goes through the loop (this is usually 1).

The exists field controls how the loop acts if it runs out of data
before the max value is reached. There are only three valid values for
the exists field: 0, 1 or 2. If the exists field is a 0, the loop will
continue processing until the max is reached. If it is a 1, then the
loop will stop processing the contents of the loop and continue on
through the sheet as if the loop had reached the max. If exists is 2 and
the character sheet is currently within a filter, PCGen will not print
anything else until the end of the filter `|%|` is reached or another
filter is begun.

The `|ENDFOR|` token tells the program where the loop ends and is
required when you use a |FOR, loop.

Here is an example demonstrating a FOR loop:

`|FOR,%eqp,0,COUNT[EQUIPMENT]-1,1,1|`

`|EQ%eqp.NAME|<br>`

`|ENDFOR|`

This loop will generate a list of the names of all of your equipment,
one item to a line using the EQx.Name token, where x is the current
count in the loop. (The &lt;br&gt; is an HTML line break.)

Example output for a typical starting fighter would be:

`Half-Plate          Outfit (Explorer's)          Shield (Large/Steel)          Battleaxe`

The variable in the above loop is %eqp. The min is 0. The max is
`COUNT[EQUIPMENT]-1` . I subtracted 1 because we are going to cycle
through the equipment list and the equipment list array starts at 0
while the COUNT statement starts at 1. Because of this we need to reduce
the actual count by 1. The increment is going to be 1 and the loop will
exit immediately if it runs out of items before the max is reached.

Notice the use of the variable %eqp to define the equipment number each
time through. Using loop variables properly, you can accomplish the
creation of large lists with relatively little effort. This is the main
reason to use loops.

One last thing to know about these kinds of loops is that they may be
nested. For example:

`|FOR,%spbk,0,COUNT[SPELLBOOKS]-1,1,1|`

`|SPELLBOOKNAME%spbk|`

`|FOR,%lvl,0,9,1,1|`

`|SPELLLISTBOOK%spbk.%lvl|`

`|ENDFOR|`

`|ENDFOR|`

This would create a list of spells for each of your spellbooks (by
level).

The spell list loop is said to be nested inside of the spell book loop.
This allows us to use two variables. If you need more variables, you may
nest more loops. Notice that each loop needs its own `|ENDFOR|`
statement.

The format for the next kind of FOR loop looks like this:

`|FOR.min,max,perLine,phrase,startLine,endLine,exists|`

This kind of FOR loop can be used to generate multi-column lists. Notice
that the character following the FOR is a period instead of a comma.
There is no variable name in this kind of loop; to get the current
increment of the FOR loop you would use the "%" (percent) symbol.

The min and max variables are the start and end points for the loop. The
perLine variable is how many phrases will be repeated before the endLine
is printed (e.g. 3 if you wanted a 3-column list). The phrase is the
code that is parsed for tokens.

You must use "\\" (backslash) characters instead of "|" (pipe)
characters to delimit tokens within a FOR loop phrase. The startLine
will be output at the beginning of the loop and after the endLine. The
endLine variable will be printed every perLine times through the loop.

This type of FOR loop does not require an |ENDFOR| tag. This type of FOR
loop cannot be nested, ***except*** when doing a party sheet. Nesting in
this manner will be covered in the section dealing with party sheets.

**NOTE:** If you are using this type of FOR loop to create a party sheet
(psheet\*.\*) you must use a "\\\\" double backslash to delimit the
tokens within the phrase. Party sheets will be covered elsewhere, but it
is important to be aware of it.

A real example (for a single character sheet):

`<table>`

`|FOR.0,COUNT[EQUIPMENT]-1,2,<td>\EQ%.NAME\</td>,<tr>,</tr>,1|`

`</table>`

HTML note: The &lt;table&gt; and &lt;/table&gt; are the HTML table
opening and closing commands &lt;tr&gt; and &lt;/tr&gt; open and close a
table row respectively and &lt;td&gt; and &lt;/td&gt; open and close a
single piece of data in the table.

This would produce a table of two columns listing the names of all your
equipment.

Example Output:

`Half-Plate          Outfit (Explorer's)          Shield (Large/Steel)          Battleaxe`

There is no named variable in this loop. The min is 0. The max is
`COUNT[EQUIPMENT]-1` . The perLine is 2, so there will be two phrases
output before the endLine. The phrase is `<td>\EQ%.NAME\</td>` . The
startLine is `<tr>` (to start the row) and the endLine is `</tr>` (to
end the row).

The final type of for loop is the DFOR loop. While the format of the
loop itself is fairly complicated, what it does isn't. Instead of
creating a table of elements across and then down, it creates a table of
elements down and then across.

To illustrate the difference between the different loops:

`FOR,` Loop Output

`FOR.` Loop Output

`DFOR` Loop Output

1

1 2 3

1 4

2

4 5 6

2 5

3

3 6

5

6

The format for the DFOR loop:

`|DFOR.min,maxDown,stepNextLine,totalMax,stepInLine,phrase,startLine,endLine,exists|`

Explanation coming shortly (as soon as I figure out the best way to turn
this into Human English :p)

### Math

Simple mathematical operations are supported in the character sheets.

The operators +, -, \*, /, @ and \^ may be used and you may set the
order of operations using ().

You must use at least two operands. These operands can be valid tokens
(that return numbers), or they can both be hard-coded numbers or a token
and a number.

@ and / are both used for division, but the first one returns only the
integer portion of the operation.

Do not use spaces between the operands and the operator. Doing so will
cause the math operation to fail.

Math can also be performed on attack routines without any extra effort.
For example: Say you use the token `|WEAPON%.TOTALHIT|` and it returns
"+6/+1". Were you to use `|WEAPON%.TOTALHIT+2` |, the output would be
"+8/+3".

There are several variables you may append to a math operation (using a
"." As a delimiter) that will change the format of the output. These
variables are:

-   INTVAL - Displays just the integer portion of the result operation.
-   NOZERO - Displays blank if the result is zero, otherwise displays
    the result.
-   SIGN - Prepends the appropriate sign (+ or -) to the result.
-   TRUNC - Displays the result to the first decimal place.

These variables may be used in combination with each other. For
example:\
`|(VAR.Turn Level+STAT5.MOD).INTVAL.SIGN|` would add the variable "Turn
Level" and the Wisdom Modifier together, return only the integer portion
of that operation and prepend the appropriate sign to it.

Creating a new OS:
------------------

It has to be in the same directory as the other Output Sheets and the
name has to start with "csheet\_". Then it will show up in the export
list.

-   The standard file naming standard is "csheet\_genre\_identifier".

-   In
    [docs\\outputsheetpages\\outputsheetsstd.html](/outputsheet/std.html)
    a description of what makes your os sheet special if its html/xml in
    standard versions. In
    [docs\\outputsheetpages\\outputsheetspdf.html](/outputsheet/pdf.html)
    a description of what makes your os sheet special if its xslt/.fo
    in PDF. In
    [docs\\outputsheetpages\\outputsheetstxt.html](/outputsheetpages/outputsheetstxt.html)
    a description of what makes your os sheet special if its plain txt.

-   To get your sheet added to the repository and into the next
    distribution as soon as possible. Upload to the
    <http://groups.yahoo.com/group/pcgen_experimental/files/> in file
    section "2) Step 2 -PRE-ALPHA, COMPLETED DATASETS GO HERE", don't
    forget to check the box at the box at the bottom of the upload box
    to let others know its there. Either wait for the notice to appear
    on PcGen Experimental newsgroup and reply with the description as to
    what is special about the new csheet, or you can email it to
    the newsgroup.

    Note: It is PCGen's policy to not put author's web links, whether
    commercial or personal, on output sheets submitted for inclusion
    within PCGen. Author's of such pages will have their names added to
    the list of volunteers that have contributed to PCGen. Additionally,
    if requested, PCGen will place the author's name in the comments
    section of the sheet as the original author.

-   If you need assistance with tags, ask on
    <PCGenListFileHelp@yahoogroups.com> . Closed Content items are not
    discussed as such. Check the front of the book for the OGL
    disclaimer and see if what you need help with is Closed Content. If
    it is then ask about a "Foo" skill/fead/class/device that has the
    following capabilities, limited by the following and what you have
    tried to get the effect you are interested in.

Character Sheet Creation
------------------------

Now on to the actual process of creating a character sheet. The first
thing to do is to decide what our sheet is for. As a not too simple and
not too difficult one I will go through creating a complete equipment
list with the weapons separated out of it. We'll put the weapons on one
side and the equipment on the other.

Now that we've decided what our sheet is for we need to decide exactly
what is going to be displayed on it.

We should have some way of identifying the character the sheet goes
with, and the player playing the character. The class listing and level
could be helpful too. If you are anything like me, you have multiple
printed copies of your character floating around all the time in the
various stages of their development, so these last couple bits of
information can be invaluable.

For the weapons we should display all of the standard attributes you
usually see on character sheets; Weapon name, to hit, damage, hand,
range, type, size, any special properties and critical hit information.

For the rest of the equipment we can get away with a lot less
information. We would want the equipment name (lets make it bold if it's
a magic item), the location it's carried or equipped at, its weight, how
many of it we have and any special properties it might have.

The tokens for the above list (in the order I listed them above) are;

For the identification we have: `NAME` , `PLAYERNAME` , `CLASSLIST` ,
`TOTALLEVELS`

For the weapons we have: `WEAPONx.NAME` , `WEAPONx.TOTALHIT` ,
`WEAPONx.DAMAGE` , `WEAPONx.HAND` , `WEAPONx.RANGE` , `WEAPONx.TYPE` ,
`WEAPONx.SIZE` , `WEAPONx.SPROP` , `WEAPONx.CRIT` , `WEAPONx.MULT`

For the equipment we have: `EQx.NAME.MAGIC~<b>~</b>` , `EQx.EQUIPPED` ,
`EQx.WT` , `EQx.QTY` , `EQx.SPROP`

The "x" in all of the tokens above will actually be a variable of some
type (%weapon or %equipment perhaps). We'll cover that in more depth
shortly.

Next up is to decide on the actual layout. It is best to sketch what
you're looking to do as a quick reference, and then begin your HTML and
craft it to fit the visualization you sketched out.

While you may use an HTML editor such a Frontpage to create sheets, I
personally prefer to use a simple text editor and do it by hand.

Construction of character sheets for PCGen is done almost entirely
through the use of tables for both the .html and the .fo files. Some of
the tables are simple, some of them are deeply nested tables within
tables.

We need to start the HTML sheet and set a few basic parameters like a
white background, and a title to be displayed in the title bar of the
browser when the final sheet is opened.

`<html>          <head>          <title>|NAME|'s Weapons and Equipment</title>          </head>          <body bgcolor="white">`

Our first table will hold the identification and appear at the top of
the sheet. The HTML for this would look as follows ( *note that for the
sake of space here I have removed several bits of formatting information
regarding font's, etc. that you will see in the actual sheet this is
referring to* ):

`<!-- Start Character Info Table -->          <table cellpadding="0" cellspacing="4" border="0" width="100%">          <tr>          <td width="35%">|NAME|</td>          <td width="20%">|CLASSLIST|</td>          <td width="10%">|TOTALLEVELS|</td>          <td width="35%">|PLAYERNAME|</td>          </tr>          <tr>          <td>CHARACTER NAME</td>          <td>CLASS</td>          <td>LEVEL</td>          <td>PLAYER</td>          </tr>          </table>`

The `<tr>` and `</tr>` are the opening and closing tags for a table row.
The `<td>` and `</td>` are the opening and closing tags for each piece
of table data (basically an individual cell to think in spreadsheet
terms).

What we've done here is put our tokens in the top row, and then in the
row underneath put labels for the various tokens.

Note the comments and indentation. These can be very helpful when you
are in a deeply nested table and need to keep track of where you are.

Next we get into the aforementioned nested tables. Since we want to
divide the rest of the sheet in half, with one half being for the
weapons and the other half for the rest of the equipment, we start
another table.

`<!-- Start Main Sheet Table -->          <table cellpadding="0" width="100%" cellspacing="5" border="0">          <tr>          <td valign="top" width="50%">`

This opens the table we will use as the main container for the rest of
the tables on the sheet. We've created the table, started the first row
and told it that we want the first data field to take up half of the
available page width.

Our next task is to put the weapons tables into this data area. We'll
start with a simple table to put a banner across half the page with a
label describing what information the tables following it contain.

`<!-- Start Weapon Tables -->          <table cellpadding="0" width="100%" cellspacing="0" border="0">          <tr>          <td align="center">WEAPONS</td>          </tr>          </table>`

The next step is to start the actual weapons tables. The first step in
this process is to craft the loop to cycle through the weapons. For the
sake of simplicity, we'll use the most basic kind of FOR loop that I
described first.

We'll call our variable %weap just so it's easy to remember what we're
using it for. Then, because the equipment arrays are 0 indexed, we want
our start number to be 0. To get the max number we will use
`COUNT[EQTYPE.WEAPON]-1` (remember the loop starts at 0 so we need to
end it one step early, hence the -1 on the end). We want it to step
through the loop one at a time so we set the step parameter to 1 and we
want it to continue through to the end of the loop, so we set the exists
parameter to 0. What it took and entire paragraph to write out boils
down to the following:

`|FOR,%weap,0,COUNT[EQTYPE.WEAPON]-1,1,0|`

Our weapons information will be contained in two tables, one immediately
following the other. We do this so that we can have different numbers of
columns in each table. While it is possible to achieve this look with a
single table, it is much more involved to try and produce.

The first table will have the weapons name, attack bonus, damage and
critical hit information. The HTML would look like this:

`<table cellpadding="0" width="100%" cellspacing="0" border="0">          <tr>          <td align="center" height="15" rowspan="2" width="40%">|WEAPON.%weap.NAME|</td>          <td align="center" width="20%" height="15">TOTAL ATTACK BONUS</td>          <td align="center" width="20%" height="15">DAMAGE</td>          <td align="center" width="20%" height="15">CRITICAL</td>          </tr>          <tr>          <td align="center"><b>|WEAPON.%weap.TOTALHIT|</td>          <td align="center"><b>|WEAPON.%weap.DAMAGE|</td>          <td align="center"><b>|WEAPON.%weap.CRIT|/x|WEAPON.%weap.MULT|</td>          </tr>          </table>`

Immediately following this will be another table that contains the rest
of the weapon information (hand, range, type, size and special
properties). That portion of the weapon display would look like this:

`<table cellpadding="0" cellspacing="0" border="0" width="100%">          <tr>          <td align="center" height="15" width="15%">HAND</td>          <td align="center" height="15" width="15%">RANGE</td>          <td align="center" width="15%" height="15">TYPE</td>          <td align="center" width="15%" height="15">SIZE</td>          <td align="center" width="40%" height="15"SPECIAL PROPERTIES</td>          </tr>          <tr>          <td align="center">|WEAPON.%weap.HAND|</td>          <td align="center">|WEAPON.%weap.RANGE|</td>          <td align="center">|WEAPON.%weap.TYPE|</td>          <td align="center">|WEAPON.%weap.SIZE|</td>          <td align="center">|WEAPON.%weap.SPROP|</td>          </tr>          </table>`

We then need to end the weapons loop and jump to the other half of the
sheet to do our other equipment, so after the above tables would be the
following:

`|ENDFOR|          <!-- End Weapon Tables -->          </td>          <td valign="top" width="50%">`

Once again, we need to start a new table to contain our next group of
data. As before, we'll put a title identifying the information the
section will contain, as well as headers.

`<!-- Start Equipment Tables -->          <table cellpadding="0" width="100%" cellspacing="0" border="0">          <tr>          <td align="center">Equipment</td>          </tr>          <tr>          <td width="60%"><b>ITEM</b></td>          <td width="10%" align="center"><b>EQUIPPED</b></td>          <td width="10%" align="center"><b>QTY</b></td>          <td width="10%" align="center"><b>WT.</b></td>          <td width="10%" align="center"><b>GP COST</b></td>          </tr>`

As we did for the weapons, we need to devise a loop to go through all
the equipment we have.

We'll call our variable %eqp just so it's easy to remember what we're
using it for. Then, because the equipment arrays are 0 indexed, we want
our start number to be 0. To get the max number we will use
`COUNT[EQ.NOT.Weapon]-1` (remember the loop starts at 0 so we need to
end it one step early, hence the -1 on the end). We want it to step
through the loop one at a time so we set the step parameter to 1 and we
want it to continue through to the end of the loop, so we set the exists
parameter to 0. What once again took an entire paragraph to write out
boils down to the following:

`|FOR,%eqp,0,COUNT[EQUIPMENT.Not.Weapon]-1,1,0|`

Unlike the weapons, the equipment will all be in one table, which is a
continuation of the title and header we did above. We just need to get
the proper information to line up under the proper header. The next
section looks like this:

`<tr>          <td class="border">|EQ.NOT.Weapon.%eqp.NAME.MAGIC~<b>~</b>|<br/> |EQ.NOT.Weapon.%eqp.SPROP|</font></td>          <td class="border">|EQ.NOT.Weapon.%eqp.EQUIPPED|<br /></td>          <td class="border">|EQ.NOT.Weapon.%eqp.QTY|<br /></td>          <td class="border">|EQ.NOT.Weapon.%eqp.WT|<br /></td>          <td class="border">|EQ.NOT.Weapon.%eqp.COST|<br /></td>          </tr>`

We now need to end the equipment loop and close out the equipment table.

`|ENDFOR|          </table>          <!-- End Equipment Table -->`

Since our sheet is done at this point, we also need to close the master
table and the html page. The last bits of our character sheet should
look like this:

`</td>          </tr>          </table>          <!-- End Main Sheet Table -->          </body>          </html>`

That about covers it. More complex sheets are simply using more tables,
sometimes nesting three or four deep. If you need help, visit the PCGen
mailing list at <http://groups.yahoo.com/group/pcgen/>

------------------------------------------------------------------------



