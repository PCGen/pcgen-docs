+++
date = "2016-08-01"
title = "Priesthoods"
original_url = "/list/rules-guide/grig-priesthoods.html"

[menu.main]
    identifier = "rules-guide_grig-priesthoods"
    name = "Priesthoods"
    parent = "rules-guide"
    
+++
**Rule Description:** Deities may have more than one "Priesthood", each
with their own powers and abilities granted through the different
domains available to each priesthood.

**PCGen Version:** 5.12.1

**Gamemode/Dataset:** 35e/RSRD Complete

**File(s) Covered:** *feat.lst* , and *deity.lst*

**Tags Used:**

`      VISIBLE          ,           TYPE          ,           PREMULT          ,           PREFEAT          ,           ADD:FEAT          ,           DOMAINS     `

NOTE: In this section we will discuss only those LST tags specific to
this implementation, and how they are used to implement the subject
rule. For more general information on the associated tags, please visit
the [LST File Tag Index](/navlistindex.html) section of the PCGen
Documentation.

------------------------------------------------------------------------

Implementation Discussion
-------------------------

Implementing "Priesthoods" for deities requires entries in two lst
files. These will be entries for the priesthood feats, one for each
priesthood created, in the *feat.lst* file, and the "Deity" entry in the
*deity.lst* file where the priesthood feats are selected and applied. It
is through the selection and application of these feats that the various
"domains" are made available, and it is through these domains that the
powers and abilities that differentiate each of a Deity's priesthoods
from the others are granted.

To help you better understand these entries, we will be using a
fictitious deity called the "The Monkey God" who has four priesthoods,
each with their own selection of domains. These priesthoods, and the
domains they have access to, are listed below:

> Priesthood of Code Monkey - Domains of Knowledge, Madness, Creation,
> and Magic.\
>  Priesthood of Data Monkey - Domains of Knowledge, Madness, Creation,
> and Artifice.\
>  Priesthood of Doc Monkey - Domains of Knowledge, Madness, Artifice,
> and Magic.\
>  Priesthood of the Monkey - Domains of Knowledge and Madness.

We will discuss, below, each of the LST entries required, and the tags
that make them work, to implement these priesthoods. For assistance in
understanding how to read this page you may review the [Rules Style
Guide](/list/rules-guide/reading-instructions.html) .

------------------------------------------------------------------------

### Feat File

The specific feat entries in the *feat.lst* file are made one per line
and begin with the name of the feat. Our feats are called "Priesthood of
the Code Monkey", "Priesthood of the Data Monkey", "Priesthood of the
Doc Monkey", and the generic "Priesthood of the Monkey". For this rules
implementation these feats are used to simply identify which
"priesthood" the character belongs to. The tags used to do this are
explained below:

> **Tag Used:** `VISIBLE:EXPORT`
>
> **What it does:** Hides the feat name from PCGen but displays it on
> the character sheet.

> **Tag Used:** `TYPE:Priesthood`
>
> **What it does:** This sets the TYPE of the associated priesthood feat
> as "Prisethood".

> **Tag Used:** `PREMULT:1,[!PREFEAT:TYPE=Priesthood],[PREFEAT:1,x]`
>
> **Variables Used (x):** Text (Priesthood being granted.)
>
> **What it does:** Sets a feat requirement of already having the
> associated feat OR having no priesthood feats at all.

> **Sub-Tag Used:** `!PREFEAT:1,TYPE=Priesthood`
>
> **What it does:** Used as part of the PREMULT tag above to set a feat
> requirement of not already having a priesthood feat.

> **Sub-Tag Used:** `PREFEAT:1,x`
>
> **Variables Used (x):** Text (Priesthood)
>
> **What it does:** Used as part of the PREMULT tag above to set a feat
> requirement of already having the associated priesthood feat.

You will find the completed [Priesthood
Feats](/list/rules-guide/grig-priesthoods.html#feats) below.

------------------------------------------------------------------------

### Deity File

The specific deity entry in the *deity.lst* file is made on a single
line and begins with the name of the deity. For this implementation we
will be using the name "The Monkey God". The particular mechanism used
to implement this rule is that of the domains granted by the deity to
bestow the differing powers upon his clerics. Specifically, it is the
PRExxx tags that make the difference possible. Each preisthood will have
access to a different set of domains and it is the presence of the
preisthood feat that establishes the prerequisite. Of course the first
thing that needs to happen is the choice of the Monkey God's
preisdthoods, a choice which is made when the deity is first selected.
The tags used to do this are explained below:

NOTE: There are a number of tags used to create a deity that are not
part of this implementation guide. To get more general information on
how to create a deity you can review [Lesson \#14,
Deities](/list/lst-file-class/14-deities.html) , in the [LST File
Class](/list/lst-file-class/lst-file-class_index.html) section of these documents.

> **Tag Used:**
> `ADD:FEAT|Priesthood of the Code Monkey, Priesthood of the Data Monkey,Priesthood of the Doc Monkey,Priesthood of the Monkey`
>
> **What it does:** Will give the character a choice of one of the four
> priesthood feats listed.

> **Tag Used:** `DOMAINS:x,x|PREFEAT:1,y,y`
>
> **Variables Used (x):** Text (Domain being granted.)
>
> **Variables Used (y):** Text (Required priesthood. See priesthood feat
> list above.)
>
> **What it does:**
>
> -   This is a comma-delimited list of domains that the deity grants to
>     the members pf it's various priesthoods.
> -   The domain name MUST match the domain names listed in the domain
>     list file.
> -   The PREFEAT tag has been added at the end of the DOMAINS tag to
>     apply restrictions on which domains are allowed for the priedthood
>     selected in the ADD:FEAT tag.
> -   Multiple DOMAINS tags may be present for a deity. They will all
>     add to the list of the deity's domains.

> **Sub-Tag Used:** `PREFEAT:1,x,x`
>
> **Variables Used (x):** Text (Name of priesthood. See Feat File Entry
> above.)
>
> **What it does:** Sets a feat requirement for the DOMAINS tag granting
> domains to the deities clerics.

You will find the completed
[Deity](/list/rules-guide/grig-priesthoods.html#deity) below.

------------------------------------------------------------------------

### Known Issues

The use of the `ADD:FEAT` tag introduces a problem with the removal and
reselection of a deity.

------------------------------------------------------------------------

### LST File Entry Examples

These LST objects are being presented as examples only and are not part
of any official PCGen dataset.

<span id="feats"></span>

Feat File: Priesthoods of the "Code", "Data", and "Doc" Monkeys

> `Priesthood of the Code Monkey`
>
> `VISIBLE:EXPORT`
>
> `TYPE:Priesthood`
>
> `PREMULT:1,[!PREFEAT:1,TYPE=Priesthood],[PREFEAT:1,Priesthood of the Code Monkey]`

> `Priesthood of the Data Monkey`
>
> `VISIBLE:EXPORT`
>
> `TYPE:Priesthood`
>
> `PREMULT:1,[!PREFEAT:1,TYPE=Priesthood],[PREFEAT:1,Priesthood of the Data Monkey]`

> `Priesthood of the Doc Monkey`
>
> `VISIBLE:EXPORT`
>
> `TYPE:Priesthood`
>
> `PREMULT:1,[!PREFEAT:1,TYPE=Priesthood],[PREFEAT:1,Priesthood of the Doc Monkey]`

> `Priesthood of the Monkey`
>
> `VISIBLE:EXPORT`
>
> `TYPE:Priesthood`
>
> `PREMULT:1,[!PREFEAT:1,TYPE=Priesthood],[PREFEAT:1,Priesthood of the Monkey]`

<span id="deity"></span>

Deity File: "Monkey God"

> `The Monkey God`
>
> `ALIGN:TN`
>
> `PREALIGN:NG,LN,TN,CN,NE`
>
> `DEITYWEAP:Pile of Poo`
>
> `DOMAINS:Knowledge,Madness`
>
> `DOMAINS:Creation|PREFEAT:1,Priesthood of the Code Monkey,Priesthood of the Data Monkey`
>
> `DOMAINS:Artifice|PREFEAT:1,Priesthood of the Data Monkey,Priesthood of the Doc Monkey`
>
> `DOMAINS:Magic|PREFEAT:1,Priesthood of the Code Monkey],Priesthood of the Doc Monkey`

> `ADD:FEAT|Priesthood of the Code Monkey,Priesthood of the Data Monkey, Priesthood of the Doc Monkey,Priesthood of the Monkey`

etc.

------------------------------------------------------------------------

### Variations on a Theme

#### Additional Powers and Abilities

The example above demonstrates how to grant different domains, and their
associated powers, to a cleric based upon not only which deity he
follows, but also based upon which of that deity's priesthoods he
belongs to. It is possible, through the same "Priesthood" feats, to
grant other powers and abilities directly that effect the characters
skills, combat, spellcasting ability, and even the characters hit dice.
To get a better idea of what powers and abilities can be granted, all
you have to do is browse through the various feats and templates
distibuted with the RSRD. A few examples of such effects are listed
below:

**Examples of *feat.lst* solutions**

The following solutions can be implemnted in the priesthood feats
directly.

> Adding skill ranks is accomplished with the BONUS tag.
>
> **Tag Used:** `BONUS:SKILL|Balance,Escape Artist|2`
>
> **What it Does:** Adds two ranks each to the skills **Balance** and
> **Escape Artist** .
>
> **Source:** Taken from the feat **Agile** , *rsrd\_feats.lst* .
>
> Increasing the characters combat initiative can be accomplished with
> the BONUS tag.
>
> **Tag Used:** `BONUS:COMBAT|INITIATIVE|4`
>
> **What it Does:** Adds four to the characters initiative modifier.
>
> **Source:** Taken from the feat **Improved Initiative** ,
> *rsrd\_feats.lst* .
>
> Adding additional feats can be accomplished with the VFEAT tag.
>
> **Tag Used:** `VFEAT:Leadership`
>
> **What it Does:** Grants the **Leadership** feat to the characters.
>
> **Source:** Adapted from the feat **Leadership** , *rsrd\_feats.lst* .

**Examples of *template.lst* solutions**

The following solutions can be implemented by creating priesthood
templates and then granting the template in the priesthood feat with the
TEMPLATE tag.

> Increasing the hitdie size can be accomplished with the HITDIE tag in
> a template.
>
> **Tag Used:** `HITDIE:%up2|CLASS=Cleric`
>
> **What it Does:** Increases the characters "Cleric" hitdie size by two
> steps.
>
> **Source:** Adapted from Template **Half Hitdie** ,
> *rsrd\_templates\_type.lst* .
>
> Granting darkvision can be accomplished with the VISION tag in a
> template.
>
> **Tag Used:** `VISION:Darkvision (60')`
>
> **What it Does:** Grants to the character darkvision out to 60'.
>
> **Source:** Adapted from Template **Angel** ,
> *rsrd\_templates\_type.lst* .

**Miscelaneous Examples**

> Granting special abilities can be accomplished with the SA tag in
> either a feat or a template.
>
> **Tag Used:** `SA:Scent (Ex) - track by sense of smell`
>
> **What it Does:** Grants to the character the ability to track by
> sense of smell.
>
> **Source:** Taken from Template **Scent** ,
> *rsrd\_templates\_type.lst* .

------------------------------------------------------------------------



