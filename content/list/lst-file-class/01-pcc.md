+++
date = "2016-08-01"
title = "Lesson #1: PCC - Campaign Info.."
original_url = "/list/lst-file-class/01-pcc.html"

[menu.main]
    identifier = "lst-file-class_01-pcc"
    name = "Lesson #1: PCC - Campaign Info.."
    parent = "lst-file-class"
    
+++
By Professor Chris Chandler (Barak).

**File(s) Covered:** \*.pcc (basic creation)

**Tags used:**

`      CAMPAIGN          ,           GAMEMODE          ,           RANK          ,           TYPE          ,           SOURCELONG          ,           SOURCESHORT          ,           SOURCEWEB          ,           ISOGL          ,           COPYRIGHT          ,           INFOTEXT     `

This lesson will discuss what a PCC is, and what it uses to tell PCGen
about itself. This will get a Campaign to show up in PCGen's source tab,
and allow it to load (though it won't load anything till [lesson
2](/list/lst-file-class/02-pcc.html) ).

------------------------------------------------------------------------

PCC - what it is, and what it does.
-----------------------------------

A PCGen Campaign Configuration file (PCC) is a text document which PCGen
reads to gather what source files to load, and other information about
itself (the 'campaign') and it's associated files. Without these types
of files, PCGen would not be able to load the data files.

So, I've created my own world with lots of feats, classes, skills, etc.
I want to create a new 'Campaign' in PCGen so I can easily make up
characters and monsters for my world. I'm going to call it 'My stuff'
since it is going to be stuff I'm making for myself.  :)

First I need to create a home for my PCC and the data files associated
with it. I'm going to place it in a subdirectory of /data/ in the PCGen
folder.  This is the standard practice, although you may certainly
create it elsewhere if you wish. I'm going to make a new folder in
/data/ called /mystuff/ just to make it easy to keep these files
separate, and so I'll know where things are.

Next, I'm going to start up my favorite text editor and create and save
an empty file.  I'll call it "mystuff.pcc".  Notice the .pcc - PCGen
looks for that particular extension when first starting for the list of
campaigns it can load.  This has to be the \_final\_ extension.  If you
accidentally save it as mystuff.pcc.txt, PCGen will not "see" it and you
won't be able to load your data.

Now I'm ready to start telling PCGen what my Campaign is and which files
it needs to load.

------------------------------------------------------------------------

`      CAMPAIGN:     ` The name used for the set of sources in the PCC

The first step is to name this campaign for PCGen. (PCGen \*does not\*
use the PCC file name for that). Since it needs to create a memory
object, and then define parts of it, we HAVE to name the campaign for
PCGen on the FIRST LINE of the file. No other tag lines can come before
it. We tell PCGen the name of the campaign by using the CAMPAIGN tag. So
I put " `CAMPAIGN:My Stuff` " right at the very top. When PCGen lists my
campaign, it will display 'My stuff' in the source tab.

------------------------------------------------------------------------

**`GAMEMODE:`** what game mode the campaign is designed for.

The next thing I need to do is to tell PCGen what GameMode I want this
campaign to run in. We use the GAMEMODE tag to tell PCGen which GameMode
to run in. Since I want to run it in the normal gamemode that comes with
PCGen, I'm going to use '3e' So I put " `GAMEMODE:3e` " on my second
line. Note that this MUST be the second line in the file.

------------------------------------------------------------------------

**`RANK:`** Loading order.

Moving on, the next step in the process is determining what priority the
data files associated with this PCC have related to other sources, and
what order PCGen should load things in.  To do this we use the RANK tag.
Choosing the rank can get complicated, because it effects what happens
when you use .MOD tags and other things. But, since this is the "basic
PCC" lecture, we'll go the simple route for the moment. :)

I am making this my primary campaign file because I want to load this
one \_only\_ so I don't have to think about the other sources in PCGen
(and make it easier for my group to load the same stuff). I'm going to
make it `RANK:1` . It should now load before any other source with a
higher RANK number.

Currently, you can only have a RANK between 1 and 9, which limits how
many things can be on different levels. If 2 PCCs are the same Rank, it
loads them in whatever order it has them stored internally... That's
going a bit deep, and we can cover that in depth in another lesson...

------------------------------------------------------------------------

`      TYPE:     ` Displaying on the Source tab.

Now, I need to set up the tree of sources for this PCC that you see when
you first start up PCGen. This is done by using a TYPE tag. This is a
"." delimited list. Each "." creates a sub-level. The typical method of
doing the TYPE tag is to list publisher, and then type of book, and then
anything else necessary. So I'll enter "TYPE:PCGenLstMonkey.Campaign
Setting.My World".

My file now looks like this (between the `-----` lines is the actual
file):

> `-----------            CAMPAIGN:My Stuff            GAMEMODE:3e            RANK:1            TYPE:PCGenLstMonkey.Campaign Setting.My World            -----------`

What you'll see on the source screen when you start PCGen up now if you
expanded the tree fully would be:

> **PCGenLstMonkey\
>  \^---Campaign Setting\
>  \^---My World\
>  \^---My Stuff**

------------------------------------------------------------------------

`      SOURCExxx:     ` Identifying the source material.

Now we come to several tags that are very important if you're putting in
somebody else's material (or perhaps even your own if you hope to
publish some day). The first three give information on who
created/published the material. Those tags are "SOURCELONG" which is
used to give the publishers full name. Next is "SOURCESHORT" which is
used to give an abbreviation to be used for the publisher and finally is
"SOURCEWEB" which is used to put in the URL of the publishers web site.
My entries for these tags will be:

> `SOURCELONG:PCGenLstMonkey      ``SOURCESHORT:PCGLM      ``SOURCEWEB:http://www.mystuffcampaign.com`

------------------------------------------------------------------------

**`ISOGL`** and `      COPYRIGHT:     ` OGL Section 15 information.

Next up is another important bit at least if you want to share your
files, either with friends or with the rest of the PCGen community, the
ISOGL tag. This is used to indicate whether or not the source falls
under the OGL license (most do... It's really hard work for it not to). 
So we'll enter it this way: " `ISOGL:YES` ". This will trigger the
program to insert the information from the next tag we cover into the
OGL (Open Gaming License) that we display on startup.

The next tag is the COPYRIGHT tag. We use this tag to enter our
copyright information, or the publisher's copyright information. When
entering others copyright information, it must be entered exactly as
they have, mis-spellings and all. For my set the tag will look like
this:

> `COPYRIGHT:PCGenLstMonkey Copyright 2003`

------------------------------------------------------------------------

**`INFOTEXT:`** further information for the user.

Now, I'd like people who look at my data set in PCGen to know what it's
for, so I'll use the INFOTEXT tag to give them a little information
about it. What you enter here will appear in the lower left pane of the
PCGen UI with a heading of "INFO". My tag will read like this:

> `INFOTEXT:This data set contains all the information necessary to create a character for the mystuff campaign world`

That is everything you need to tell PCGen about the Campaign itself.
[Part II](/list/lst-file-class/02-pcc.html) will be actually linking up
the PCC with LST files....

Barak\
 LST Chimp



