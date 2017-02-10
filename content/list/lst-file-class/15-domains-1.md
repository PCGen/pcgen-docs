+++
date = "2016-08-01"
title = "Lesson #15: .lst - Domains ( Part 1, The Basics)"
original_url = "/list/lst-file-class/15-domains-1.html"

[menu.main]
    identifier = "lst-file-class_15-domains-1"
    name = "Lesson #15: .lst - Domains"
    parent = "lst-file-class"
    
+++
By Eric C Smith (Maredudd) and Andrew McDougall (Tir Gwaith)

**File(s) Covered:** \*\_domains.lst

**LST Standard** : 6.0.0

**Tags used:**

`      DESC          ,           SPELLLEVEL:DOMAIN           SOURCEPAGE          ,`

------------------------------------------------------------------------

The domain file is a simple text file with one 'Domain' per line. There
is only one domain specific tag in PCGen so most of the heavy work in
building domains is in the global tags you will use. In this class I
will go over both the domain specific tag as well as a few of the global
tags, organized into two lessons: The Basics, Lesson 15, covering the
tags required to create the basic functionality of a domain, and The
Domain Powers, Lesson 16, that will cover the more advanced tags that
will be used to add the 'Domain Powers' to your domains. Unfortunately,
there are so many variations of global tags that can be used in any data
file, including the domain file, that it is impractical to go over them
all, but I believe that the examples I will be using in these two
lessons, in conjunction with the PCGen documentation, will give you a
jump start on building your own domains.

For those of you that have gone through the previous LST Classes, some
of the global tags will be repetitive. feel free to skip those portions
if you like. These classes are being written for the new LST-coder, so
there will be some overlap, but a student of the classes does not need
to take them in order.

To help you better understand how to put this file together, I will be
using several domains as examples, three drawn from the Revised Standard
Reference Document (RSRD) and one I have made up for this class in order
to more completely demonstrate a few specific global tags. The domains
we'll look at from the RSRD are ***Law*** , ***Trickery*** and ***War***
, as well as the new domain of 'Poetry'. Our new domain is presented
below in the standard RSRD format so you can follow along.

### Example Domain

#### Poetry Domain {#poetry-domain .indent1}

**Granted Powers:** You add all ***Perform*** skills to your cleric
class skills and automatically gain the ability to ***Scribe Scrolls***
at 3rd level ***.*** You cast mind-affecting spells at +1 caster level.
and is graced by ***Great Intelligence*** every four levels to a maximum
of 20th level. If you have a charisma score of 12 or greater you may use
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

The Poetry Domain is a little overdone, but I wanted to demonstrate a
number of global tags. I would not recommend using the Poetry Domain in
your campaign, unless of course you believe the pen is mightier than the
sword . . .

------------------------------------------------------------------------

Without further adieu, lets jump right into the lesson.

NOTE: The general conventions used within this class can be found on the
[LST File Class Style Guide](/list/lst-file-class/style-guide.html) .

------------------------------------------------------------------------

`      <Domain Name>     `

This is the name used for the domain. There is no specific tag
associated with this entry and it must be the first entry on the domain
line. So, our example domains lines will begin simply enough with the
following entries:

**Example:**

`War` &lt;tab&gt;

`Poetry` &lt;tab&gt;

------------------------------------------------------------------------

`      DESC     `

Now we are getting to the 'fun stuff'. This tag is a global tag and is
used to provide a simple explanation, or as Professor Baraks calls it,
the 'flavor text', of the powers granted to the cleric by the domain.
These powers can range anywhere from granted feats, spell-like
abilities, or enhancements to any number of skills and abilities. If you
are creating a domain based upon your favorite source book, you can
generally find this information identified as the 'Granted Powers' in
the domain block. For the Poetry Domain listed above and the War Domain,
found in the RSRD, the `DESC` tags are reproduced below:

**Example:**

> `War`
>
> `DESC:Free Martial Weapon Proficiency with deity’s favored weapon (if necessary) and Weapon Focus with the deity favored weapon.`

> `Poetry`
>
> `DESC:You add all Perform skills to your cleric class skills and automatically gain the ability to Scribe Scrolls at 3rd level. You cast mind-affecting spells at +1 caster level. and is graced by Great Intelligence every four levels to a maximum of 20th level. If you have a charisma score of 12 or greater you may use Ventriloquism once a day as a spell-like ability.`

------------------------------------------------------------------------

`      SPELLLEVEL:DOMAIN     `

In the domain file this tag provides a list of bonus spells, and their
levels, that the cleric is granted access to by the domain.

There are two types of argument regularly used with this tag, used in
pairs in a pipe (|) delimited list. These arguments are the domain spell
level slot, appearing as `<domain name>=<spell level>` , and the name of
the spell that fills that level slot. Together, the string of arguments
will look like this:
`|<domain name>=<spell level 1>|<spell name 1>|<domain name>=<spell level 2>|<spell name 2>|<domain name>=<spell level 3>|<spell name 3> . . .`

Using this format, and looking at the spell list for the War domain, we
would code the first level War domain spell this way: &lt;War=1|Magic
Weapon&gt;, with the complete list of spells codded as seen in the
complete example below.

Looking at our sample domain as defined above, the second example below
shows how we would code the domain spells for the domain of Poetry.

Oh, and one more thing. When listing a spell you MUST use the name used
at the beginning of its entry in the spell.lst file and NOT its output
name. The Poetry domains 3rd level spell, ***Geas, Lesser*** is a good
example. The rsrd\_spells.lst file has 'Geas (Lesser)' as the name of
the spell with its output name being ***Geas, Lesser*** . Other
incarnations of the `SPELLLEVEL` tag use comma-delimited data and
including a comma in the domain's spell list will cause PCGen to ignore
the spell reference, thereby not granting access to that spell as a
domain spell.

**Example:**

> `War` &lt;tab&gt; . . . &lt;tab&gt;
> `SPELLLEVEL:DOMAIN|War=1|Magic Weapon|War=2|Spiritual Weapon|War=3|Magic Vestment|War=4|Divine Power|War=5|Flame Strike|War=6|Blade Barrier|War=7|Power Word Blind|War=8|Power Word Stun|War=9|Power Word Kill`
>
> `Poetry` &lt;tab&gt; . . . &lt;tab&gt;
> `SPELLLEVEL:DOMAIN|Poetry=1|Hypnotism|Poetry=2|Suggestion|Poetry=3|Geas (Lesser)|Poetry=4|Modify Memory|Poetry=5|Song of Discord|Poetry=6|Irresistible Dance|Poetry=7|Hold Person (Mass)|Poetry=8|Charm Monster (Mass)|Poetry=9|Hold Monster (Mass)`

------------------------------------------------------------------------

**`SOURCEPAGE`**

This tag is as simple as it looks. It identifies the page within the
source material where you can find the specific description, powers, and
spells for the domain you are creating. It takes free-form text but most
often you will find it in one of two forms. If your source material is
an OGL book the format is usually `SOURCEPAGE:p.<#>` . If you are
working from an online source, such as the RSRD, you would use the
filename, so your tag would look like `SOURCEPAGE:<filename>.`

Since I have created the Poetry Domain from scratch there is no
'source', so there is no `SOURCEPAGE` tag required, but many functions
and filters in PCGen use it, so it is good to include it. Therefore, I
will include the tag with an N/A for the source page. I will skip it.
The War Domain on the other hand comes from the RSRD and therefore would
use the `SOURCEPAGE` tag per the example below.

Note: There are three other `SOURCExxx` tags ( `SOURCELONG` ,
`SOURCESHORT` and `SOURCEWEB` ) that will be covered in a separate class
so we will not be covering them here.

**Example:**

`War` &lt;tab&gt; . . . &lt;tab&gt; `SOURCEPAGE:SpellListI.rtf`

`Poetry` &lt;tab&gt; . . . &lt;tab&gt; `SOURCEPAGE:N/A`

------------------------------------------------------------------------

### Conclusion: The Domain File Entry

My domain entry now looks like this (all on a single line.):

> `Poetry`
>
> `DESC:You add all Perform skills to your cleric class skills and automatically gain the ability to Scribe Scrolls at 3rd level. You cast mind-affectng spells at +1 caster level and is graced by Great Inteligence every four levels to a maximum of 20th level. If you have a charisma score of 12 or greater you may use Ventriloquism once a day as a spell-like ability.`
>
> `SPELLLEVEL:DOMAIN|Poetry=1|Hypnotism|Poetry=2|Suggestion|Poetry=3|Geas (Lesser)||Modify Memory|Poetry=5|Song of Discord|Poetry=6|Irresistible Dance|Poetry=7|Hold Person (Mass)|Poetry=8|Charm Monster (Mass)|Poetry=9|Hold Monster (Mass)`
>
> `SOURCEPAGE:SpellListI.rtf`
>
------------------------------------------------------------------------

Well, that's everything you need to add new domains to your campaign,
albeit, only the most basic of functionality will exist. You may have
noted a number of abilities are included in the `DESC` tag that this
domain entry doesn't implement. To see how to implement these abilities
we will move to the [LST File Class \#16, Domain
Powers](/list/lst-file-class/16-domains-2.html) .

Maredudd

------------------------------------------------------------------------



