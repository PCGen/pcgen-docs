+++
date = "2016-08-01"
title = "Lesson #7: .lst - Spell Basics"
original_url = "/list/lst-file-class/07-spells.html"

[menu.main]
    identifier = "lst-file-class_07-spells"
    name = "Lesson #7: .lst - Spell Basics"
    parent = "lst-file-class"
    
+++
By Professor Andrew McDougall (Tir Gwaith).

**File(s) Covered:** \*spells.lst

**PCGen LST Standard:** PCGen 6.00.x

**GameMode:** 3.5e (RSRD)

**Tags used:**

`      SCHOOL          ,           SUBSCHOOL          ,           DESCRIPTOR          ,           CLASSES          ,           DOMAINS          ,           TYPE          ,           COMPS          ,           CASTTIME          ,           RANGE          ,           TARGETAREA          ,           DURATION          ,           SAVEINFO          ,           SPELLRES          ,           DESC          ,           VARIANTS          ,           COST          ,           XPCOST     `

Please notice the **order** of the tags I put them in. That is how I
enter spells into LST format. I use this order mainly because it is
order in which the information is provided in the spell blocks found in
most sources. For my example, I'll be using **Blasphemy** from the RSRD.
This spell covers most of the tags I'll be covering in this class. I'll
use other spells as examples of the tags that **Blasphemy** doesn't use.

<span class="lstfile"> spells.lst </span> is probably the most "data"
like of all the different file types. This lesson is going to cover the
basics on that data entry. Parts for Temporary bonus information
(applying a spell to a character) will come later.

------------------------------------------------------------------------

### Part 1: Schools of Magic

**Tags covered:**

`SCHOOL, SUBSCHOOL, DESCRIPTOR`

The line below the spell name is usually in this format: **School
(Subschool) \[Descriptors\]**

Note that I mention "Descriptors" in plural. There generally is only one
School and Subschool, but many spells have more than one descriptor.
`DESCRIPTOR` can contain a pipe-delimited (|) list of descriptors, so
put a pipe between more than one descriptor.

Blasphemy has **Evocation \[Evil, Sonic\]** so it has a School and 2
descriptors.

> `SCHOOL:Evocation            DESCRIPTOR:Evil|Sonic`

Animal Trance has all 3 tags:

**Enchantment (Compulsion) \[Mind-Affecting, Sonic\]**

> `SCHOOL:Enchantment            SUBSCHOOL:Compulsion            DESCRIPTOR:Mind-Affecting|Sonic`

The tag associated with Descriptor is VARIANTS, but I normally enter it
when doing DESC, since this field usually comes from the body of the
spell description, but is usually linked with the DESCRIPTOR.

------------------------------------------------------------------------

### Part 2: Linking to a spell list:

**Tags covered:**

`CLASSES, DOMAINS, TYPE`

This is only part of the way of linking. If adding a new spell, this is
the method used. When adding a new class and linking an old spell, the
SPELLLEVEL tag is used.

The first two are easy. TYPE is then based on the first two tags. Our
example from **Blasphemy:**

> **Blasphemy**\
>  Level: Clr 7, Evil 7

Would translate into:

> `Blasphamy            CLASSES:Cleric=7            DOMAINS:Evil=7`

Since both of these are for Divine spellcasters, it would get:

> `TYPE:Divine.`

Both tags are pipe (|) and comma (,) delimited. As an example:

> **Antimagic Field**\
>  Level: Clr 8, Magic 6, Protection 6, Sor/Wiz 6

Which would translate into:

> `Antimagic Field            CLASSES:Cleric=8|Sorcerer,Wizard=6            DOMAINS:Magic,Protection=6`

Now, because the above list has both Arcane and Divine spells, the next
tag would be:

> `TYPE:Arcane.Divine`

There are a lot more aspects to linking spells, castability, etc. but
those are global tags not normally used in a <span class="lstfile">
spells.lst </span> , and we can cover those later.

------------------------------------------------------------------------

### Part 3: Spell Components and Casting time

**Tags covered:**

`COMPS, CASTTIME`

This section is easy, especially for those people that like to cut and
paste. For the following spell information:

> Components: V\
>  Casting Time: 1 standard action

Is coded as:

> `COMPS:V            CASTTIME:1 standard action`

Exact entry into the tag field. Easy.

------------------------------------------------------------------------

### Part 4: Range, Duration, and Target / Area / Effect

**Tags covered:**

`RANGE, DURATION, TARGETAREA`

Ok, the first two are easy.

1\) **Range** - We have a nice bit of code that auto-calculates the Close
/ Medium / Long ranges for spells, which is done through a GameMode file
so you can add more if you wish, so whenever you see one of those, you
merely need to put in the word for the range.

2\) **Duration** - We have a nice bit of code that will do math
functions. Such math functions must be encapsulated within a set of
parentheses (). The character casterlevel can be used in these
calculations by using the variable `CASTERLEVEL` as part of the math
function. Everything in the parentheses is reduced to a number. For
normal parentheses, like those used for "(D)" where spellcaster can end
the spell sooner than the listed duration, we use the square-brackets
\[\].

3\) **Target** / **Area** / **Effect** - I have only once or twice seen a
spell that had more than one of these three. Hence we combine them into
one tag.

Here is a example of these spell info items and how they are coded in
PCGen:

> **Range: 40 ft.\
>  Area: Nonevil creatures in a 40-ft.-radius spread centered on you\
>  Duration: Instantaneous**

Is coded as:

> `RANGE:40 ft.            TARGETAREA:Nonevil creatures in a 40-ft.-radius spread centered on you            DURATION:Instantaneous`

Another example (from **Antipathy** spell):

> **Range: Close (25 ft. + 5 ft./2 levels)\
>  Target: One location (up to a 10-ft. cube/level) or one object\
>  Duration: 2 hours/level (D)**

Is coded as:

> `RANGE:Close            TARGETAREA:One location [ up to (CASETERLEVEL*10) cubes] or one object            DURATION:(CASTERLEVEL*2) hours [D]`

------------------------------------------------------------------------

### Part 5: Saving Throws and Spell Resistance

**Tags covered:**

`SAVEINFO, SPELLRES`

Again, this is easy copy/paste stuff.

Example:

> Saving Throw: None or Will negates; see text\
>  Spell Resistance: Yes

Is coded as:

> `SAVEINFO:None or Will negates; see text            SPELLRES:Yes`

------------------------------------------------------------------------

### Part 6: Description and Variants, and extra costs.

**Tags covered:**

`DESC` , `VARIANTS` , `COST` , `XPCOST`

These tags are from the spells description, and require some judgment
calls.

1\) `DESC` is usually pulled from the "one-liners" in spell descriptions,
such as those found in the RSRD <span class="lstfile"> SpellListI.rtf
</span> etc. Otherwise, reducing a paragraph into something that will
fit on a character sheet (and will require the user to still own the
book the item came from) becomes an editing call. We try to keep these
descriptions to less than 50 characters long.

2\) `VARIANTS` are taken from the description, where the caster makes a
decision on how a spell works when casting, such as Fire Seeds, where
the caster uses either acorns or berries. This also applies to things
like **Energy Resistance** , where the energy type is decided at
casting.

3\) `COST` gives the specific cost of material components, usually listed
at end of the spell description.

4\) `XPCOST` gives the xp cost, when one exists, when casting the related
spell. As with the material component cost, the xp cost is typically
listed at the end of the spell description.

Example from **Blasphemy** :

> `DESC:Kills, paralyzes, weakens, or dazes nonevil subjects.`

Per <span class="lstfile"> SpellListI.rtf </span> , **Blasphemy** does
not have any listed variants, material component cost, or xp
cost.(Copy/Paste from SpellListI.rtf)

Example from **Clone** :

> Clone M F: Duplicate awakens when original dies.\
>  Material Component: The piece of flesh and various laboratory
> supplies (cost 1,000 gp).\
>  Focus: Special laboratory equipment (cost 500 gp).

Is coded as:

> `DESC:Duplicate awakens when original dies.            COST:1500`

Now, adding the cost of the Focus may not be the right thing to do here
(I just used the example from the RSRD, so I could find one for the
field...). The deciding factor on that would be how the cost of the
Focus would be added into the creation of an item based on this spell
(Material component costs are added into item creation costs).

The XPCOST example is easier (from **Commune** )

> XP Cost: 100 XP.

> `XPCOST:100`

------------------------------------------------------------------------

Throw in a `SOURCEPAGE` tag, and basically, that is a spell, minus any
Temp bonus tags for applying spell effects to characters.

Tir Gwaith\
 LST Chimp

------------------------------------------------------------------------



