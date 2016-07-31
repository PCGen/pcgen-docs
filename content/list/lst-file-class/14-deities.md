+++
date = "2016-08-01"
title = "Lesson #14: .lst - Deities"
original_url = "/list/lst-file-class/14-deities.html"

[menu.main]
    identifier = "lst-file-class_14-deities"
    name = "Lesson #14: .lst - Deities"
    parent = "lst-file-class"
    
+++
By Eric C. Smith (Maredudd) and Andrew McDougall (Tir Gwaith)

**File Covered** : \*\_deities.lst

**LST Standard** : 6.0.0

**Tags Used:**

`      DOMAINS          ,           ALIGN          ,           DEITYWEAP          ,           PANTHEON          ,           TITLE          ,           APPEARANCE          ,           WORSHIPPER          ,           DESCISIP          ,           SOURCEPAGE     `

------------------------------------------------------------------------

The deity files are used to set up and describe the deities that provide
the divine inspiration for your game setting. Unfortunately, the RSRD
does not include any deities and therefore PCGen does not provide any,
at least 'out of the box'. That means you will have to either create
your own deities within PCGen or input them from any of the many
commercial sources available in order to take advantage of the special
powers and spells granted to clerics through the various deities and the
domains they oversee. To that end, with this lesson I will be showing
you the ins and outs of deity LST coding.

The material will be broken down into three sections, the first of which
will introduce you to the basic tags required to create a useful deity
within PCGen, including some tags that are used by PCGen in files other
than the deity file. The second section will cover additional tags that
will help flesh out the detail for your deities, providing descriptive
text that will help identify what the deity is about as well as in
selecting the right one for the character. The third section will cover
the tags used to provide the proper source identification for the
encoded deities. For those of you that have gone through the previous
LST Classes, some of the global tags, especially the last section, will
be repetitive. Feel free to skip those tag descriptions if you like.
These classes are being written for the new LST-coder, so there will be
some overlap, but a student of the classes does not need to take them in
order.

### Example Deities

As I stated above, there are no deities listed in the RSRD from which to
draw examples from but there is an example in the my\_deities.lst file
which can be found inside PCGen. For additional examples, and to stay
clear of any copyright issues, I have created two completely copyright
free sample deities from which to build this class material.

------------------------------------------------------------------------

#### MoSaT {#mosat .indent2}

The CONTENTed One

Demigod

**Pantheon** : BoD

**Symbol** : A Kitten on a Keyboar

**Alignment** : Chaotic Good

**Portfolio** : PCGen Datasets

**Worshipers** : LST Monkeys

**Cleric's Alignment** : NG, CG, CN

**Domains** : Chaos, Knowledge, Animal

**Favored Weapon** : Tiger Claws

**Description** : The great content provider. He is usually seen as a
small simian stooped over a wireless keyboard typing madly as he travels
the world setting all knowledge down in the LSTs.

#### Thalia {#thalia .indent2}

The Flourishing one

Lesser Deity

**Pantheon:** Olympian

**Symbol** : A Shepherd's Crook upholding a Comic Mask

**Alignment** : Neutral Good

**Portfolio** : Comedy, Pastoral Poetry

**Worshipers** : Comedians and Pastoral Poets

**Cleric's Alignment** : LG, NG, TN, CG

**Domains** : Good, Knowledge, Poetry

**Favored Weapon** : Shepherd's Crook

**Description** : The muse of comedy and of playful and idyllic poetry,
Thalia inspires those so inclined to produce great works of comedy as
well as peaceful, and pastoral, works of poetry. She is sometimes seen
with a crown of ivy and a Shepherd's crook.

------------------------------------------------------------------------

Without further adieu, let's jump right into the lesson.

NOTE: The general conventions used within this class can be found on the
[LST File Class Style Guide](/list/lst-file-class/style-guide.html) .

------------------------------------------------------------------------

### Section 1: The Basics

This section will introduce you to the tags required to implement a
simple deity within PCGen. That is, the minimum set of tags needed to
implement a deity within PCGen.

------------------------------------------------------------------------

#### &lt;Deity Name&gt;

The deity file is currently a \*.lst file that has one deity entry per
line. The first thing on each line must be the name of the deity. There
is no tag for it as the program assumes that whatever is at the
beginning of the line is the name of a deity. This means that the
entries into our data file begin as follows:

`MoSaT` &lt;TAB&gt;

`Thalia` &lt;TAB&gt;

------------------------------------------------------------------------

#### DOMAINS

**Tag Format:** `DOMAINS:<domain list>`

This tag sets the domains the deity makes available to divine casters.
The text following the tag is a comma-delimited list of domain names
with no spaces included. It is important that the domains listed must be
defined in a <span class="lstfile"> domain.lst </span> file that has
been loaded into PCGen. When making your own deity, you may include as
many domains as you wish, though prudence may dictate limiting the
number for if a deity has all domains, which can be done by simply using
`ALL` as the sole argument, there is no need for additional deities, and
what fun would that be.

The `PRExxx` tag may be used as an optional tag added at the end of the
domain list, separated by a pipe (|). These prerequisites are checked
against the divine caster to determine if he/she is allowed to select
the domains listed in that particular `DOMAINS` tag. Typically, the
`PREALIGN` tag is used to restrict what alignments a cleric/class with
access to domains can be to have access to the domains. For more depth
on `PREALIGN` syntax and usage itself, scroll down a bit. It can be used
by itself on the line (with slightly different meaning for the user) and
is explained more in depth there.

PCGen provides some flexibility in how the `DOMAINS` tags are applied,
allowing some fairly complex application, but most usage of this tag is
fairly simple so you might just skip over the next paragraph. On the
other, if you wish to explore this flexibility, the following
explanation can get you started.

When using the `PRExxx` tags at the end of the `DOMAINS` tag, all
domains listed in that tag will be restricted if the `PRExxx` tag isn't
satisfied. Fortunately, PCGen allows the placement of multiple `DOMAINS`
tags in the same deity line, and each `DOMAINS` tag can have its own
`PRExxx` tag, or none at all. With multiple `DOMAINS` tags, the `PRExxx`
tags are applied only to the domains included in that specific `DOMAINS`
tag but all domains included in each `DOMAINS` tags are made available
to the divine caster, that is if the appropriate prerequisites have been
satisfied.

At this point we are ready to build the `DOMAINS` tags for our two
example deities.

<span class="lstobj"> MoSaT </span> is listed as having the domains of
<span class="lstobj"> Chaos </span> , <span class="lstobj"> Knowledge
</span> , and <span class="lstobj"> Animal </span> , so this tag will
appear as `DOMAINS:Chaos,Knowledge,Animal` . If we wish to restrict the
selection of the <span class="lstobj"> Chaos </span> domain to only
those divine casters who are chaotic, we can break the `DOMAINS` tag
into the following two tags: `DOMAINS:Chaos|PREALIGN:CG,CN` &lt;tab&gt;
`DOMAINS:Knowledge,Animal` .

<span class="lstobj"> Thalia </span> is listed as having the domains of
<span class="lstobj"> Good </span> , <span class="lstobj"> Knowledge
</span> , and <span class="lstobj"> Poetry </span> , so this tag will
appear as `DOMAINS:Good,Knowledge,Poetry` . If we wish to restrict the
selection of the <span class="lstobj"> Good </span> domain to only those
divine casters who are good, we can break the `DOMAINS` tag into the
following two tags: `DOMAINS:Good|PREALIGN:LG,NG,CG` &lt;tab&gt;
`DOMAINS:Knowledge,Poetry`

**Example:**

`MoSaT` &lt;TAB&gt; . . . &lt;TAB&gt; `DOMAINS:Chaos,Knowledge,Animal`
(without the `PRExxx` tags.)

`MoSaT` &lt;TAB&gt; . . . &lt;TAB&gt; `DOMAINS:Chaos|PREALIGN:CG,CN`
&lt;tab&gt; `DOMAINS:Knowledge,Animal` (With the `PRExxx` tag.)

`Thalia` &lt;TAB&gt; . . . &lt;TAB &gt; `DOMAINS:Good,Knowledge,Poetry`
(without `PRExxx` tags.)

`Thalia` &lt;TAB&gt; . . . &lt;TAB&gt; `DOMAINS:Good|PREALIGN:LG,NG,CG`
&lt;tab&gt; `DOMAINS:Knowledge,Poetry` (with `PRExxx` tags.)

------------------------------------------------------------------------

**`ALIGN`**

**Tag Format:** `ALIGN:<alignment>`

This tag identifies the alignment of the deity. The generally accepted
entries in the text field are `LG` , `NG` , `CG` , `LN` , `TN` , `CN` ,
`LE` , `NE` and `CE` representing the following alignments: Lawful Good,
Neutral Good, Chaotic Good, Lawful Neutral, True Neutral, Chaotic
Neutral, Lawful Evil, Neutral Evil and Chaotic Evil. This tag isn't
strictly necessary, but is used in `PREDEITYALIGN` tag, and a few other
places, so we are including it with the critical tags.

If you examine the stat blocks for our example deities, you will find
each lists an alignment: "Chaotic Good" for <span class="lstobj"> MoSaT
</span> , and 'Neutral Good' for <span class="lstobj"> Thalia </span> .
Using the appropriate abbreviations, we get the tag implementations
listed below.

**Example:**

`MoSaT` &lt;TAB&gt; . . . &lt;TAB&gt; `ALIGN:CG`

`Thalia` &lt;TAB&gt; . . . &lt;TAB&gt; `ALIGN:NG`

------------------------------------------------------------------------

**`PREALIGN`**

**Tag Format:** `PREALIGN:<alignment abbreviation>`

This tag establishes a restriction, based on the electing character's
alignment, on which deities may be selected. This tag, in conjunction
with the `DOMAINS` tag, replaces the functionality of the
`FOLLOWERALIGN` tag, which, as it has been deprecated, isn't being
covered in this class.

The argument for this tag is a comma-delimited list of alignments by
abbreviation. The accepted entries in the text field are `LG` , `NG` ,
`CG` , `LN` , `TN` , `CN` , `LE` , `LN` and `CE` representing the
following alignments: Lawful Good, Neutral Good, Chaotic Good, Lawful
Neutral, True Neutral, Chaotic Neutral, Lawful Evil, Neutral Evil and
Chaotic Evil. These abbreviations are defined in the <span
class="lstfile"> statsandchecks.lst </span> file in the Game Mode
section of the PCGen documentation. There is one additional 'alignment'
which can be included. That is `Deity` , which simply refers back to the
selected deity's own alignment.

If you examine the stat blocks for our example deities, you will find
each includes a "Cleric"s Alignment" listed. MoSaT's clerics must be
Neutral Good, Chaotic Good and Chaotic Neutral while Thalia's clergy
must be Lawful Good, Neutral Good, True Neutral, or Chaotic Good. Using
the syntax described above and the appropriate abbreviations, we get the
tag implementations listed below.

**Example:**

`MoSaT` &lt;TAB&gt; . . . &lt;TAB&gt; `PREALIGN:NG,CG,CN`

`Thalia` &lt;TAB&gt; . . . &lt;TAB&gt; `PREALIGN:LG,NG,TN,CG`

------------------------------------------------------------------------

`      DEITYWEAP     `

**Tag Format:** `DEITYWEAP:<favored weapon>`

This tag provides the deity's favored weapon. This entry is a
pipe-delimited (|) list of weapon proficiencies (defined in <span
class="lstfile"> weaponprof.lst </span> file, or the tag won't really do
anything.) This is included with the basic tags because, unlike purely
descriptive tags, this information is used in the game mechanics, at
least in a minor way. The easiest example is if a character is a cleric
for a deity of war, that being a deity that has the <span
class="lstobj"> War </span> domain as one of his domains, and if that
cleric has chosen the <span class="lstobj"> War </span> domain as one of
his domains, then proficiency with the deity's favored weapon is
automatically granted. Note that it is important that any favored weapon
for a deity with the <span class="lstobj"> War </span> domain must be
included in at least one of the loaded datasets. The game mechanic is
also there for other bonuses and checks to see that the character has
the Deity's favored weapon, but that is more advanced stuff, so we'll
leave that for a different class.

Examining the stat blocks for our deities, we find <span class="lstobj">
MoSaT </span> uses 'Tiger Claws' while <span class="lstobj"> Thalia
</span> uses the 'Shepherd's Crook'. The implementation of this tag for
our deities is shown below.

**Example:**

`MoSaT` &lt;TAB&gt; . . . &lt;TAB&gt; `DEITYWEAP:Tiger Claws`

`Thalia` &lt;TAB&gt; . . . &lt;TAB&gt; `DEITYWEAP:Shepherd's Crook`

------------------------------------------------------------------------

Well, this wraps up part 1 of this class. With the info above, you can
create a basic deity and give it enough functionality to bring it to
life for your cleric's, and the party's enjoyment.

------------------------------------------------------------------------

### Section 2: Filling in the Detail

In the previous section we covered the minimum set of tags required to
properly implement a deity in PCGen. In this section we will be covering
the tags that are used to flesh out your deities by providing additional
detail. The additional detail is used primarily to allow for different
ways in which to sort the deities during the character generation
procedure, as well as adding flavor to your game. No game mechanics use
these tags directly. You will also find that these tags are very simple
to implement.

------------------------------------------------------------------------

`      PANTHEON     `

**Tag Format:** `PANTHEON:<pantheon name>`

This tag establishes the pantheon to which the deity belongs. Examples
of these pantheons are the standard racial pantheons (i.e. Elven,
Dwarven, etc.), historical pantheons (i.e. Greek/Olympian, Roman,
Scandinavian/Aesir, etc) or campaign/homebrew pantheons. In practical
use, this tag is used to allow deities to be sorted during character
generation, in this case, by the pantheon that it belongs to.

The deity stat blocks above list the pantheon for <span class="lstobj">
MoSaT </span> as BoD and for <span class="lstobj"> Thalia </span> as
'Olympia', leading to the tag implementation listed below.

**Example:**

`MoSaT` &lt;TAB&gt; . . . &lt;TAB&gt; `PANTHEON:BoD`

`Thalia` &lt;TAB&gt; . . . &lt;TAB&gt; `PANTHEON:Olympia`

------------------------------------------------------------------------

**`TITLE`**

**Tag Format:** `TITLE:<descriptive title>`

This tag provides the deity's descriptive title, providing an element of
storytelling, or flavor to your game. The argument for the tag is a
simple text entry. For our two deities you will find the title listed
just beneath the deity's name, thus <span class="lstobj"> MoSaT </span>
is called 'The CONTENTed One' and <span class="lstobj"> Thalia </span>
is called 'The Flourishing One'. You can see the implementation of this
tag for each deity below.

**Example:**

`MoSaT` &lt;TAB&gt; . . . &lt;TAB&gt; `TITLE:The CONTENTed One`

`Thalia` &lt;TAB&gt; . . . &lt;TAB&gt; `TITLE:The Flourishing One`

------------------------------------------------------------------------

`      APPEARANCE     `

**Tag Format:** `APPEARANCE:<descriptive appearance>`

This tag provides the deity's descriptive appearance and implementing it
for our two deities is simple. The argument, the descriptive appearance,
is a simple text entry. For our two deities you will find the appearance
included with the general description. Its a simple matter to review the
text and extract the simplest physical description you can. You can see
the implementation of this tag for each deity below.

**Example:**

`MoSaT` &lt;TAB&gt; . . . &lt;TAB&gt;
`APPEARANCE:He is usually seen as a small simian stooped over a wireless keyboard typing madly.`

`Thalia` &lt;TAB&gt; . . . &lt;TAB&gt;
`APPEARANCE:She is sometimes seen with a crown of ivy and a Shepherd's crook`

------------------------------------------------------------------------

`      WORSHIPPERS     `

**Tag Format:** `WORSHIPPERS:<typical worshipers>`

This tag provides a list of the deity's typical worshipers; whether by
class, race, occupation, eye color, speech-pattern, etc. All text
following the tag up to the next &lt;TAB&gt; or &lt;RETURN&gt; is
assumed to be a descriptive list of these typical worshipers. This tag
is not referenced by anything; it is purely descriptive.

To implement this tag for our two deities you can find the typical
worshipers listed in the stat blocks identified by the 'Worshipers'
label . . . imagine that! You can see the implementation of this tag in
the examples below.

NOTE: The astute student will note that the `WORSHIPPERS` tag is
misspelled. That may be so but that is the way the tag is in fact
spelled within the program, so please conform to the misspelling ... at
least until we can fix it in the code base.

**Example:**

`MoSaT` &lt;TAB&gt; . . . &lt;TAB&gt; `WORSHIPPERS:LST Monkeys`

`Thalia` &lt;TAB&gt; . . . &lt;TAB&gt;
`WORSHIPPERS:Comedians and Pastoral Poets`

------------------------------------------------------------------------

This completes section 2 of this class material. You can now fully
encode any deity you desire!

------------------------------------------------------------------------

### Section 3: The Rest of the Story

If you are building homebrew data sets you can skip this section, as you
will not need the following tags. If, on the other hand, you are
planning on making lots of personal datasets for books you own they are
useful. If you are building datasets as a PCGen Data Monkey, they are
very important so please bear with me and we'll get through this as
quickly as possible.

Note: It is very likely that if you have gone through any of the other
\*.lst classes you have seen these tags before and do not need to suffer
through this particular session . . . I promise ninja228 will not come
by in the middle of your next LSTing session to exact punishment for not
reading through it . . . unless of course you violate the rules of
LSTing . . . then you're on your own!

------------------------------------------------------------------------

**`DESCISIP`**

**Tag Format:** `DESCIP:<YES or NO>`

This tag is used to identify the deity description text as either
'Product Identity' or not. What is product identity (PI)? That's a very
good questions that any lawyer can answer for you for a mere \$150 per
hour, unless of course you have abused the same PI, not recommended, in
which case you will likely have to pay a lot more.

PI, in a nutshell, is material that has not been released under the Open
Gamers License (OGL). Inclusion of any PI requires separate permission
from the publisher that owns the material. If you are coding a deity
from a source for the PCGen Project and you have PI, also called 'Closed
Content', that material needs to be identified as such within the lst
file. If you have any questions concerning the material you are lsting,
feel free to consult with any member of PCGen's Data License Team. They
can help to clarify any confusion.

As for this tag itself, it is fairly simple to implement as the argument
for the tag is a simple boolean and will take only `YES` or `NO` as
values. For our sample deities, the first created as an example in the
<span class="lstfile"> my\_deity.lst </span> file, and the other created
out-of-thin-air for this lst class, the descriptions are not PI;
therefore, we would implement this tag as `DESCISPI:NO` . Or we would if
it was really necessary for if the tag is not included PCGen defaults to
`NO` so we won't actually include the tag in our deity file.

------------------------------------------------------------------------

**`SOURCEPAGE`**

**Tag Format:** `SOURCEPAGE:<source page number>`

Simply put, this tag provides the specific page reference within the
source from which the deity information was taken. The source page text
generally takes the form of `<p.#>` with the pound sign (\#) being
replaced by the page number on which the deity information can be found
within the source material. For our sample deity <span class="lstobj">
MoSat </span> , the source material is PCGen's <span class="lstobj">
my\_deity.lst </span> file so our `SOURCEPAGE` tag will take the form of
`SOURCEPAGE:my_deity.lst` . As for <span class="lstobj"> Thalia </span>
, our invented-from-thin-air deity, there is no source page, but many
functions and filters in PCGen use it, so it is good to include it.
Therefore, we will include the tag with an `n/a` for the source page.

**Example:**

`MoSaT` &lt;tab&gt; . . . &lt;tab&gt; `SOURCEPAGE:my_deity.lst`

`Thalia` &lt;tab&gt; . . . &lt;tab&gt; `SOURCEPAGE:n/a`

------------------------------------------------------------------------

### Conclusion: The Deity File Entries

My deity entries now look like this (all on a single line and the tags
in the order that I feel makes most sense.):

`MoSaT<tab>`

`TITLE:The CONTENTed One<tab>`

`PANTHEON:BoD<tab>`

`ALIGN:CG<tab>`

`PREALIGN:NG,CG,CN<tab>`

`DOMAINS:Chaos|PREALIGN:CG,CN<tab>`

`DOMAINS:Knowledge,Animal<tab>`

`DEITYWEAP:Tiger Claws<tab>`

`APPEARANCE:He is usually seen as a small simian`

`stooped over a wireless keyboard typing madly.<tab>`

`WORSHIPPERS:LST Monkeys<tab>`

`SOURCEPAGE:my_deity.lst`

`Thalia<tab>`

`TITLE:The Flourishing One<tab>`

`PANTHEON:Olympia<tab>`

`ALIGN:NG<tab>`

`PREALIGN:LG,NG,TN,CG<tab>`

`DOMAINS:Good|PREALIGN:LG,NG,CG<tab>`

`DOMAINS:Knowledge,Poetry<tab>`

`DEITYWEAP:Shepherd's Crook<tab>`

`APPEARANCE:She is sometimes seen with a crown of ivy`

`and a Shepherd's crook.<tab>`

`WORSHIPPERS:Comedians and Pastoral Poets`

------------------------------------------------------------------------

And that's everything you need to add new deities to your campaign.

Maredudd

------------------------------------------------------------------------



