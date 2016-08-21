+++
date = "2016-08-01"
title = "Lesson #10: .lst - Languages"
original_url = "/list/lst-file-class/10-languages.html"

[menu.main]
    identifier = "lst-file-class_10-languages"
    name = "Lesson #10: .lst - Languages"
    parent = "lst-file-class"
    
+++
By Professor Chris Chandler (Barak).

**File(s) Covered:** \*languages.lst

**PCGen LST Standard:** PCGen 6.00.x

**GameMode:** 3.5e (RSRD)

**Tags used:**

`      TYPE     `

------------------------------------------------------------------------

This lesson is intended to cover creating your own "Languages".

This LST file defines the languages that may be spoken, written or read
by a character. It is even simpler than the <span class="lstfile">
weaponprofs.lst </span> file in that it consists of just the language
name and a TYPE tag for each one.

The language LST files are where the `CHOOSE:LANG` tag generates its
list from when it is invoked. This file also tells PCGen, in conjunction
with the `LANGBONUS` tag, what languages are available for races to
choose from as bonus languages based on their primary language stat.

------------------------------------------------------------------------

#### &lt;Language Name&gt;

The language file is a lst file that has one language entry per line.
The first thing on each line is the name of the language. There is no
tag for it, the program assumes that whatever is there at the beginning
of the line is the name of a language.

------------------------------------------------------------------------

**`TYPE`**

The `TYPE` tag is used to set the type/group of the language. It may
take multiple types delimited by periods. The types used are usually
Spoken, Read, and Written. Some examples:

> `English TYPE:Spoken.Read.Written            Sign Language TYPE:Spoken.Read            Trade Pidgin TYPE:Spoken`

------------------------------------------------------------------------

That's really all there is to those simple .lst files.

Barak\
 LST Chimp

------------------------------------------------------------------------



