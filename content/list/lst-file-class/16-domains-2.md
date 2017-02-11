+++
date = "2016-08-01"
title = "Lesson #16: .lst - Domains (Part 2, Advanced Topics)"
original_url = "/list/lst-file-class/16-domains-2.html"

[menu.main]
    identifier = "lst-file-class_16-domains-2"
    name = "Lesson #16: .lst - Domains"
    parent = "lst-file-class"
    
+++
By Eric C Smith (Maredudd) and Andrew McDougall (Tir Gwaith)

**File(s) Covered:** \*\_domains.lst

**LST Standard** : 6.0.0

**Tags used:**

`      CSKILL          ,           BONUS:CASTERLEVEL          ,           PREALIGN          ,           SPELLS          ,           VFEAT          ,           PREALIGN     `

------------------------------------------------------------------------

This is a continuation of the material presented in [LST File Class
\#15, Domain Basics](/list/lst-file-class/15-domains-1.html) . In this
lesson I will go over a handful of global tags needed to implement the
domain powers as described in our sample domains. As with the previous
lesson on domains, I will be using several domains as examples. Four
drawn from the Revised Standard Reference Document (R/SRD) and one I
have made up for this class in order to more completely demonstrate a
few specific global tags. The domains we'll look from the RSRD are
***Animal*** , ***Law*** , ***Trickery*** and ***War*** , as well as the
new domain of 'Poetry'. Our new domain is presented below in the
standard RSRD format so you can follow along.

### Example Domain

#### Poetry Domain {#poetry-domain .indent1}

**Granted Powers:** You add all ***Perform*** skills to your cleric
class skills and automatically gain the ability to ***Scribe Scrolls***
at 3rd level. You cast mind-affecting spells at +1 caster level, and are
graced by ***Great Intelligence*** every four levels to a maximum of
20th level. If you have a charisma score of 12 or greater you may use
**Ventriloquism** once a day as a spell-like ability.

**Poetry Domain Spells**

1.  ***Hypnotism*** **:** Fascinates 2d4 HD of creatures.
2.  ***Suggestion* :** Compels subject to follow stated course
    of action.
3.  ***Geas (Lesser)*** **:** Commands subject of 7 HD or less.
4.  ***Modify Memory* :** Changes 5 minutes of subject’s memories.
5.  ***Song of Discord* :** Forces targets to attack each other.
6.  ***Irresistible Dance*** **:** Forces subject to dance.
7.  ***Hold Person, Mass* :** As hold person, but all within 30 ft.
8.  ***Charm Monster, Mass* :** As charm monster, but all within 30 ft.
9.  ***Hold Monster, Mass* :** As hold monster, but all within 30 ft.

**NOTE:** The Poetry Domain is a little overdone, but I wanted to
demonstrate a number of global tags. I would not recommend using the
Poetry Domain in your campaign, unless of course you believe the pen is
mightier than the sword . . .

### Granted Powers

Before we begin we must first identify which 'Granted Powers' need to be
implemented. Our source for these powers is the text following the
`DESC` tag. Looking at the Poetry domain listed above, we get the
following powers:

> Add all ******Perform****** skills to your cleric class skills.\
>  You may automatically ***Scribe Scrolls*** at 3rd level.\
>  You cast mind-affecting spells at +1 caster level.\
>  Graced by ***Great Intelligence*** every four levels to a maximum of
> 20th level.\
>  May use **Ventriloquism** once a day as a spell-like ability (If you
> have a charisma score of 12 or greater)

------------------------------------------------------------------------

Without further adieu, lets jump right into the lesson.

NOTE: The general conventions used within this class can be found on the
[LST File Class Style Guide](/list/lst-file-class/style-guide.html) .

------------------------------------------------------------------------

`      CSKILL     `

This tag is used to add skills to the cleric's list of class skills. The
new class skills may include a single skill or may be a pipe (|)
delimited list of skills to be added. An example of this is the
***Trickery*** domain which adds the three skills of ***Bluff*** ,
***Disguise*** , and ***Hide*** to the Cleric's list of class skills.
The first example below gives the form of this tag.

The skills being added may also be designated by `TYPE` , taking the
form of `TYPE.<skill type>` . Our new domain is a good example of this
as the domain adds all ***Perform*** type skills to the Cleric's class
skills list. See the example below to see the tag in action.

**Example:**

`Trickery <tab> . . . <tab> CSKILL:Bluff|Disguise|Hide`

`Poetry <tab> . . . <tab> CSKILL:TYPE.Perform`

------------------------------------------------------------------------

`      BONUS:CASTERLEVEL     `

This tag grants a bonus to the character's caster level. This bonus is
dependent upon specific qualifying parameters, which are identified
within the tag itself. The tag only requires two arguments, the
qualifying tag and the number of levels the caster level is increased,
with a third optional argument in the form of a `PRExxx` tag. The
general form this tag and its argument take as follows:

`BONUS:CASTERLEVEL|<qualifying tag>|<level bonus>|PRExxx`

There are several different types of qualifying tags, including the
class name, a spell `DESCRIPTOR` , a `DOMAIN` , a `RACE` , a `SCHOOL` ,
a `SPELL` , a `SUBSCHOOL` , and a `TYPE` . Each of these tags, except
for the class name, take the form of `<TAG>.text` , with the text being
appropriate for the tag, i.e. `RACE.Elf%` , `SCHOOL.Abjuration` ,
`TYPE.Arcane` , etc. The class name is a simple text entry giving the
name of the appropriate class, i.e. `Cleric` . Looking at the Domain of
Law in the RSRD, the *rsrd\_domains.lst* file, we find, that a divine
spell caster with this domain receives a bonus when casting lawful based
spells. The specific spell descriptor of 'Lawful' is used in this tag
taking the form: `DESCRIPTOR.Lawful` . Examining the list of granted
powers for the Domain of `Poetry` above, we see a divine spell caster
with this domain receives a bonus when casting 'Mind-Affecting' spells.
The qualifying tag for the bonus takes the following form:
`DESCRIPTOR.Mind-Affecting` .

The second argument in our tag is the level bonus. This is a number,
variable, or formula that represent the number of levels that is added
to the divine casters level for the purposes of determining the effects,
DC, etc. In both the domain of ***Law*** and the domain of ***Poetry***
, the bonus level is '1'.

Finally, this tag can take `PRExxx` tags, with the most common tag being
the `PRERULE` tag which checks the state of rule as set in PCGen's
'House Rule' preferences. The rule must be defined in the
***rules.lst*** file in the 'system/gameModes' folder within PCGen. The
particular rule we are interested in for the BONUS: `CASTERLEVEL` tag
applies Casterlevel Bonuses from Domains to all Spells and is referenced
by the `VAR:SYS_DOMAIN` tag, as defined in the ***rules.lst*** file.

Taking all of this together, the `BONUS:CASTERLEVEL` tag for our two
sample domains take the form shown below.

**Example:**

`Law <tab> . . . <tab> BONUS:CASTERLEVEL|DESCRIPTOR.Lawful|1|PRERULE:SYS_DOMAIN`

`Poetry <tab> . . . <tab> BONUS:CASTERLEVEL|DESCRIPTOR.Mind-Affecting|1|PRERULE:SYS_DOMAIN`

------------------------------------------------------------------------

`      PREALIGN     `

The **PRExxx** tags are global tags that apply specific prerequisites to
the character before granting the selected domain and its granted powers
and spells. You may include as many of these tags as you like and each
of them will be applied to the domain as a whole. If the character does
not meet ALL `PRExxx` tags, the domain cannot be selected.
Unfortunately, there are too many `PRExxx` tags to go over in this class
so I will restrict my coverage to the most likely tag. That is the
`PREALIGN` tag.

The `PREALIGN` tag applies an alignment requirement to the cleric. The
form this tag takes is:

`PREALIGN:<alignment list>` .

The alignment list is a comma-delimited list of alignment abbreviations
as follows: Lawful Good= `NG` , Lawful Neutral= `LN` , Lawful Evil= `LE`
, Neutral Good= `NG` , True Neutral= `TN` , Neutral Evil= `NE` , Chaotic
Good= `CG` , Chaotic Neutral= `CN` , and Chaotic Evil= `CE` . An
additional identifier is `Deity` , representing the alignment of the
characters deity.

Note: The alignments have been assigned specific numbers, which can also
be used. The numbers are: 0=LG, 1=LN, 2=LE, 3=NG, 4=TN, 5=NE, 6=CG,
7=CN, 8=CE, and 10=Deities alignment. These values can be used instead
of the abbreviations

An example of this usage can be seen below for the domain of Law. As
there are no restrictions to be applied, either for alignment or by any
other cr criteria, for the domain of ***Poetry*** , we will not be
including a `PRExxx` tag in our ***Poetry*** domain line.

As a final note, this tag provides prerequisites that are separate from
the prerequisites used in conjunction with the
[`DOMAINS`](/list/data/deities/domains.html) tag.

**Example:**

`Law <tab> . . . <tab> PREALIGN:LG,LN,LE`

------------------------------------------------------------------------

`      SPELLS     `

This tag grants the cleric spell-like abilities. This tag has a number
of arguments that we will explain below but first, the general form of
this tag and its many arguments are as follows:

`SPELLS:<spellbook>|TIMES=<number or formula>|CASTERLEVEL=<number          of formula>|<spell name>,<spell DC>|<PRExxx tag>`

The first argument in the `SPELLS` tag is the name of the spellbook that
the spell-like ability will be displayed in within PCGen and on the
character sheet. This may include any name you can imagine, though the
several examples of this tag in the RSRD use either 'Innate' or the name
of the domain granting the ability as can be seen in the ***Animal***
domain example given below. It is very important though that the
spellbook name NOT be the same as any Class names, i.e. 'Cleric',
'Sorcerer', etc. Using an existing class name will cause PCGen to throw
an exception and it will not function properly. For our purposes, the
spell book entered is the domain name and takes the form of
`<domain name> Domain` . For the poetry domain we would enter
`Poetry Domain` .

The `TIMES` tag is an optional tag that identifies the number of times a
day the spell-like ability may be used. If it's not included in the
domain line, PCGen will default to 1 time per day. You may enter a
specific value, a variable, or a formula in this tag. It is important to
note that within the domain file the `SPELLS` tag is not associated with
any specific class, therefore, the variable `CL` will not work. (For
more information about formulas within PCGen, see the [Math Operators
and Formulas](/list/global/formulas.html) section in the PCGen
Documentation.) A special value that may be entered is the value '-1',
which will cause an output on the character sheet of 'At Will'. Both the
Animal and Poetry domains grant spell-like abilities that are usable
once per day so both domain entries will include the `TIMES=1` tag.

`CASTERLEVEL` is an optional tag that sets the level at which the
spell-like ability is cast. As with the `TIMES` tag, you may enter any
value, variable, or formula as desired. If it is not included, PCGen
will default to 1. Only one `CASTERLEVEL` tag is allowed in each
`SPELLS` tag entry. For the ***Animal*** and ***Poetry*** domains, we
base the caster level on the total level of the character, including the
PC, NPC, and Monster levels but not including any level adjustments, so
we will be using the `TL` variable as the basis for the caster level.
Unfortunately, there may be circumstances where the total level is
reduced to zero or below, i.e. with the application of a template that
applies negative levels. In this case, we still want the spell-like
ability to function, even if at a minimum level. Therefore, we will use
the `max()` formula tag. The entry for the casterlevel for both of our
example domains becomes `CASTERLEVEL=max(TL,1)` , setting the caster
level of the spell-like ability to the character's total level with a
minimum level of 1.

Besides the spell book, the `<spell name>` is the only other mandatory
argument for the `SPELLS` tag as it provides, as the tag implies, the
name of the spell being granted as a spell-like ability. This spell must
exist in the loaded datasets and must appear exactly as it does in the
first position on the spell line in the spell file. The optional
`<spell DC>` value may be a number, variable, or formula. I will
establish the DC for the ***Poetry*** domain as `12+WIS` , meaning a
base score of twelve (12) plus the wisdom modifier. The RSRD gives the
DC value for the ***Animal*** domain as `11+WIS` , being a base score of
eleven (11) plus the wisdom modifier.

The last argument to discuss is the global `PRExxx` tag. These are used
to set prerequisites for the spell-like ability such as alignment
requirements or minimum stat requirements. If a `SPELLS` tag requires
multiple `PRExxx` statements they are included as a pipe (|) delimited
list at the end of the `SPELLS` tag. Some of the `PRExxx` statements
have pipe (|) delimiting in them, in which case you simply put that
`PRExxx` statement in a separate `SPELLS` tag by itself. The ***Speak
with Animals*** ability granted by the ***Animal*** domain does not
carry a prerequisite so you will not find a `PRExxx` tag attached to the
`SPELLS` tag. The ***Poetry*** domain, on the other hand, does require a
minimum wisdom before the ***Ventriloquism*** ability is granted. This
prerequisite is coded using the `PRESTAT` tag which takes two arguments;
1) the number of stats which must qualify, one in our case, and 2) the
stat and its value, identified by the stat abbreviation defined in the
***statsandchecks.lst*** file and a numeric value representing the
minimum stat value. Our `PRESTAT` tag takes this form:
`PRESTAT:1,WIS=12`

Ok, so we've gone over all the arguments allowed in the `SPELLS` tag.
The only thing left to do is put them al together so we can see the
final tag, and this we have done below.

**Example:**

`Animal <tab> . . . <tab>          SPELLS:Animal Domain|TIMES=1|CASTERLEVEL=max(TL,1)|Speak with Animals,11+WIS`

`Poetry <tab> . . . <tab>          SPELLS:Poetry Domain|TIMES=1|CASTERLEVEL=max(TL,1)|Ventriloquism,12+WIS|PRESTAT:1,WIS=12`

------------------------------------------------------------------------

### `      VFEAT     `

The `VFEAT` tag grants a feat, or a list of feats, to a character, even
if the character would not normally meet the requirements for that feat.
The tag takes a pipe-delimited list and can be as long as desired, but
must contain at least one feat. The feats included in the feat list must
exist and you should NOT use the feats `OUPUTNAME` , if one exists for
the feat you are granting. Also keep in mind that some feats have a
`CHOOSE` built into them, such as ***Weapon Focus*** , while most don't.
***Weapon Focus*** , when applied, calls a chooser to allow the player
to choose which weapon the focus will apply to. Let us assume the
character selects the ***Longsword*** , which will be displayed as
***Weapon Focus(Longsword)*** . This causes some confusion when it comes
to listing a feat with a parenthetical element, i.e. ***Armor
Proficiency (Heavy)*** , which is a unique feat with no `CHOOSE`
command, and the afore mentioned ***Weapon Focus(Longsword)*** . PCGen
differentiates between these two cases by the inclusion, or exclusion,
of a space between the 'open' parentheses and the preceding
alpha-character. For a feat with a built in `CHOOSE` command, there is
NO intervening space while a unique feat with a parenthetical element
has an intervening space.

As stated before, the `VFEAT` tag applies a feat irrespective of the
prerequisites for that feat, but the `VFEAT` tag also allows the
application of new prerequisites through the use of the `PRExxx` tag.
The new prerequisite will be applied to all feats listed in the `VFEAT`
tag. This could cause a problem if you wanted to apply two feats, each
with their own prerequisites, but fortunately, not only can we include
as many feats in the `VFEAT` tag as we need, we can also include as many
`VFEAT` tags in the domain line as we need, each with its own `PRExxx`
tag. If you browse through the `PRExxx` section of the global tag
documentation, you will find many tags that can be used when applying
virtual feats, but I will be going over only one of them here. That is
the `PRELEVEL` tag.

The `PRELEVEL` tag establishes a prerequisite for a character to have a
minimum number of levels. Its form is simple, having as a single
argument the minimum level required. The tag takes the following form:
`PRELEVEL:<minimum level>`

With all of this in mind, the form the VFEAT tag takes in this file,
with our selected PRExxx tag, is as follows:

`VFEAT:<feat list>|PRELEVEL:<minimum level>`

For the ***Poetry*** domain, we are applying two feats: the ***Scribe
Scolls*** feat, which is granted a third level, and the ***Great
Intelligence*** feat, which normally requires that the character have at
least 21 levels. Additionally, we will apply the ***Great
Intelligence*** feat several times, specifically when the character is
at 4th, 8th, 12th, 16th, and 20th levels. Fortunately, the ***Great
Intelligence*** feat is stackable so our application of the feat five
times as the character advances from 1st to 20th level can be
accommodated by simply including five `VFEAT` tags, each with an
appropriate `PRELEVEL` tag, five time. See our example below for the
final `VFEAT` tag entries.

**Example:**

`Poetry <tab> . . . <tab>          VFEAT:Scribe Scrolls|PRELEVEL:3 <tab>          VFEAT:Great Intelligence|PRELEVEL:4 <tab>          VFEAT:Great Intelligence|PRELEVEL:8 <tab>          VFEAT:Great Intelligence|PRELEVEL:12 <tab>          VFEAT:Great Intelligence|PRELEVEL:16 <tab>          VFEAT:Greater Intelligence|PRELEVEL:20`

------------------------------------------------------------------------

### Conclusion: The Domain File Entries

My domain entry for the Domain of Poetry, adding the tags discussed
above to those discussed in lesson 14, now looks like this (all on a
single line.):

> `Poetry <tab>            CSKILL:TYPE.Perform <tab>            BONUS:CASTERLEVEL|DESCRIPTOR.Mind-Affecting|1|PRERULE:SYS_DOMAIN <tab>            SPELLS:Poetry Domain|TIMES=1|CASTERLEVEL=max(TL,1)|Ventriloquism,12+WIS|PRESTAT:1,WIS=12 <tab>            SOURCEPAGE:SpellListI.rtf <tab>            VFEAT:Scribe Scrolls|PRELEVEL:3 <tab>            VFEAT:Great Intelligence|PRELEVEL:4 <tab>            VFEAT:Great Intelligence|PRELEVEL:8 <tab>            VFEAT:Great Intelligence|PRELEVEL:12 <tab>            VFEAT:Great Intelligence|PRELEVEL:16 <tab>            VFEAT:Great Intelligence|PRELEVEL:20 <tab>            DESC:You are graced by Great Intelligence and gain the ability             to Scribe Scrolls at 3rd level. You may use Ventriloquism once a day as a             spell-like ability and add all Perform skills to your cleric             class skills. You cast mind-affectng spells at +1 caster level. <tab>            SPELLLEVEL:DOMAIN|             Poetry=1|Hypnotism|             Poetry=2|Suggestion|             Poetry=3|Geas (Lesser)|             Poetry=4|Modify Memory|             Poetry=5|Song of Discord|             Poetry=6|Irresistible Dance|             Poetry=7|Hold Person (Mass)|             Poetry=8|Charm Monster (Mass)|             Poetry=9|Hold Monster (Mass)      `

------------------------------------------------------------------------

And that's everything you need to know to add new, full feature, domains
to your campaign.

Maredudd

------------------------------------------------------------------------



