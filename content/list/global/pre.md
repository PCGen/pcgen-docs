+++
date = "2016-08-01"
title = "PRExxx Tags"
original_url = "/list/global/pre.html"

[menu.main]
    identifier = "global_pre"
    name = "PRExxx Tags"
    parent = "global"
    
+++
With these tags you can restrict access to a class, feat, deity, domain
or any other object in a lst file. The same PRExxx tags are used in
every lst file to make crafting restrictions as easy as possible.

### Usage

PRExxx tags are used in two different manners:

1.  A PRExxx tag can be used is as a stand-alone tag to qualify an
    entire line. Thus, if a character does not meet the prerequisites of
    a stand-alone PRExxx tag, he will not be able to select the lst
    object containing the PRExxx and therefore shall not gain the
    benefits granted by the lst object.
2.  BONUS tags, and certain other tags, can be qualified by appending a
    PRExxx tag to the end of it. If the character does not meet the
    prerequisites, he will not gain the BONUS but is not restricted from
    any other benefits he may receive from the line. PRExxx tags are
    usually added to BONUS tags with an additional pipe (|) followed by
    the PRExxx statement. There are, on the other hand, a few tags that
    use a different syntax, such as enclosing the PRExxx statement in
    square brackets (\[\]). Also note that all tags that will take
    PRExxx tags are clearly marked as such. Review the tag
    documentations to verify the syntax for adding prerequisites and to
    see which tags will take PRExxx tags.

There are a few additional rules to keep in mind when using PRExxx tags.

1.  When using PRExxx tags as part of a class, the level will be tested
    before any new level is fully applied. This means that
    `PREPCLEVEL:MAX=1` will pass when adding a second level to a first
    level character as that character is not yet level 2.
2.  Any PRExxx tag may be prefixed with a "!" character (i.e., !PRExxx)
    in order to invert the requirement logic. The PRExxx tag will be
    evaluated like normal, then the result inverted (meaning you CAN NOT
    have the things listed in this tag) when determining whether the
    prerequisite is passed or not.
3.  There is a `PRE:.CLEAR` tag. Be aware that it will clear all PRExxx
    tags from an object and you will need to re-enter those PRExxx tags
    that you want to keep.

General notes
-------------

### Boolean logic

#### NOT

Logical negation of any pre-requisite is obtained by pre-pending an
exclamation mark, `!` , to the `PRE` tag.

-   `PREALIGN:LG` , **without** the `!` , requires that the character's
    alignment **is** lawful good.
-   `!PREALIGN:LG` , **with** the `!` , requires that the character **is
    not** lawful good.

#### OR

Use `PREMULT:1,[sub_prereq1],[sub_prereq2]...` to require **at least
one** of the sub-prerequisites `[sub_prereq1]` , `[sub_prereq2]` , ...
to be true.

-   2-variable OR: `PREMULT:1,[PREALIGN:LG],[PREGENDER:M]`

    Must have lawful good alignment OR male gender.

-   3-variable OR: `PREMULT:1,[PREALIGN:LG],[PREGENDER:M],[PREATT:10]`

    Must have lawful good alignment OR male gender OR a base attack
    bonus of at least 10.

#### AND

Use `PREMULT:N,[sub_prereq1],[sub_prereq2]...` , where `N` is the number
of sub-prerequisites, to require that **all** of the sub-prerequisites
`[sub_prereq1]` , `[sub_prereq2]` , ... are true.

-   2-variable AND: `PREMULT:2,[PREALIGN:LG],[PREGENDER:M]`

    Must have lawful good alignment AND male gender.

-   3-variable AND: `PREMULT:3,[PREALIGN:LG],[PREGENDER:M],[PREATT:10]`

    Must have lawful good alignment AND male gender AND a base attack
    bonus of at least 10.

#### NOR and NAND

The `NOR` ( `not OR` ) and `NAND` ( `not AND` ) functions are produced
by prefixing `!` , giving the `!PREMULT` tag.

-   2-variable NOR: `!PREMULT:1,[PREALIGN:LG],[PREGENDER:M]`

    Must NOT have (lawful good alignment OR male gender).

-   2-variable NAND: `!PREMULT:2,[PREALIGN:LG],[PREGENDER:M]`

    Must NOT have (lawful good alignment AND male gender).

#### Nested functions

It is possible to nest the `PREMULT` tag within other `PREMULT` tags,
allowing logic functions like `(A OR B) AND (C OR D)` to be realised.

### Comparison Operators

Tags which deal with numbers or ordered sequences (i.e. creature sizes -
small, medium, large ...) allow the following comparison operators.

-   `EQ` - equals
-   `GT` - greater than
-   `GTEQ` - greater than or equal to
-   `LT` - less than
-   `LTEQ` - less than or equal to
-   `NEQ` - not equal to

The tags which use this syntax include:

-   `PREBASESIZE`
-   `PREHANDS`
-   `PRELEGS`
-   `PREREACH`
-   `PRESIZE`
-   `PRESR`
-   `PREVAR`

The comparison operator is written **as a part of the tag name** . i.e.
`PREVARNEQ` or `PREREACHLTEQ` .

(Not as `PREVAR:EQ` or `PREREACH:LTEQ` .)

------------------------------------------------------------------------

------------------------------------------------------------------------

Misc PRExxx Stuff
-----------------

------------------------------------------------------------------------

**<span id="preclear"></span> Tag Name:** PRE:.CLEAR

**Variables Used:** .CLEAR

**What it does:**

Clear all prerequisites.

**Example:**

`PRE:.CLEAR`

Clears all prerequisites.

------------------------------------------------------------------------

**<span id="prexxxqdata"></span> Tag Name:** PRExxx:Q:data

**Variables Used:** Q

**What it does:**

This is a variation on any PRE tag listed above. Adding a Q: between the
tag and it's data will cause it to take precedence over the QUALIFY tag.
Thus allowing QUALIFY to null out some but not all prereqs.

**Example:**

`QUALIFY:Whirlwind Attack` (In Template)

`PRESTAT:Q:1,DEX=13` (In Whirlwind Attack Feat)

If you have QUALIFY:Whirlwind Attack in a template (which means the
character ignores all the prereqs), but you still want the DEX prereq to
be enforced, you would edit the PRE in the Whirlwind Attack feat to read
as above.

------------------------------------------------------------------------



