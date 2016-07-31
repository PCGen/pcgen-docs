+++
date = "2016-08-01"
title = "Important Things to Know"
original_url = "/list/important-to-know.html"

[menu.main]
    identifier = "list_important-to-know"
    name = "Important Things to Know"
    parent = "list"
    
+++
There are a number of important things to remember when list editing, as
well as a number of tricks that one can do to get the desired results.
The following sections include the important stuff to know about list
file editing, some are just informational use, some are requirements for
turning in list files for the official releases. So if you've read this
page AND the previous page, then the next couple of pages you should
wade through before we get to the nitty gritty stuff.

Terms Used
----------

The following terms are tossed about readily and easily, some
interchangeably when talking to any list monkey, so make sure you are up
on the latest lingo and how it's used!

-   <span class="underline"> ***Source Material*** </span> - The gaming
    information provided by a publisher.

-   <span class="underline"> ***PCC (pcc) File*** </span> - this is the
    extension used for the file that tells PCGen what list files to
    load, this is a text editable file.

-   <span class="underline"> ***LST (lst or list) File*** </span> -
    Refers to a text editable file containing the specific entries read
    by PCGen to make a character (Feats, Skills, etc), and the .lst
    refers to the (commonly accepted and used) extension to save
    the files.

-   <span class="underline"> ***Tag*** </span> - A specific word used in
    list files that PCGen reads and recognizes as having an effect on
    a character.

-   <span class="underline"> ***Source*** </span> - Refers to the Source
    information specifically, as in, what source book, what page.

-   <span class="underline"> ***Campaign*** </span> - Refers to a
    collection of Source Material that is loaded as a group.

-   <span class="underline"> ***TL*** </span> - Total Level. This is
    used in a lot of formulas for the tags.

What you Need
-------------

You need only 2 things to get going, a text-editing program and
patience.

Editing or creating a list file can be a hardy experience and not one to
take on lightly, but neither is it impossible to do. Paying attention to
the syntax of how a tag works will save a lot of headaches when it comes
time to test your modifications/creations within PCGen.

Using existing list files as a reference can help you to understand how
to construct anything you want to, from classes to feats, to spells, if
you need an example, there is something in there for you to look at.

Syntax
------

This covers two areas, first, creating list files. PCGen does not care
what you call your created files, whether it is .txt, .lst, .doc, or
anything else for an extension. As long as you have the correct file
name in the .pcc file, it will load. Second, the syntax of the tags used
in the list files. the sections with the list file tags contain correct
syntax to use for each tag. PCGen DOES care about this, if your syntax
is wrong, then the tag you are working on will not work and PCGen will
return errors.

***\*IMPORTANT*** - The other item of note, any line, in any list file,
that begins with the pound sign (\#), is a comment line. PCGen will
ignore reading this line completely. (The purpose of this is to let
others know what something is/does, what items are outstanding and need
to be completed, or just notes on how something is working).

***\*CRITICAL*** - There can \_NEVER\_ be a space between fields. Always
use a TAB between fields, as a space between fields will cause the list
file to not load and/or return errors trying to load

Directory Structure
-------------------

While the directory structure is changeable, there are some common
practices to make it easier on everyone.

Currently, all the Source Material list files are kept in the
\\pcgen\\data directory, and they are then sorted by company name,
usually the long name, but some "high profile" companies are generally
shortened (Can we say SRD? I knew you could!).

There is a custom directory provided to locate your own personal list
files in, and by no means are you required to put them there, it is,
after all, your computer, put them where you are comfortable with.

When PCGen is installed, the basic directory structure will look like
this (Assume you are installing on your C drive (C:\\);

-   **C:\\pcgen** &lt;-- This is the root directory for PCGen

-   **C:\\pcgen\\characters** &lt;-- Default directory where PCGen saves
    characters to

-   **C:\\pcgen\\data** &lt;-- Base starting spot for the list files

-   **C:\\pcgen\\data\\&lt;company\_name** &gt; &lt;-- The root folder
    for the company's list files. There are too many sub-folders in this
    directory to list here. But taking a quick look at them, will show
    the suggested structure for setting up a company's list files.

-   **C:\\pcgen\\doc** &lt;-- Where all the documentation on how to use
    and customize PCGen are located

-   **C:\\pcgen\\system** &lt;-- This is where PCGen's system wide used
    files are stored at

-   **C:\\pcgen\\system\\bio** &lt;-- This is where the list files for
    randomly determining characters features are located (Hair, Skin,
    Eye color, Traits)

-   **C:\\pcgen\\system\\bio\\names** &lt;-- This is where the list
    files for random name determination are located

-   **C:\\pcgen\\system\\specials** &lt;-- This is where the list files
    for determining what bonuses stack and what special abilities are
    granted at various levels is located

-   **C:\\pcgen\\templates** &lt;-- This is where all the character &
    party sheets are located. These sheets are set up to accept
    information directly from PCGen to print out

Giving Credit where Credit is Due
---------------------------------

Giving credit to the proper source from which a specific class, feat,
spell, race, etc. came from is crucial.

It not only gives the creator credit for their work, but it also lets
the user know where it came from.

Hopefully PCGen will be used as a sort of marketing tool by both gaming
companies and by users - you can load sources based on material you
don't own, and can generate characters based on that information, but
you don't quite get enough information to use it accurately or
completely without actually buying the source material.

This way PCGen can whet your appetite for the kinds of options that are
available if you purchase book xyz.

My hope is that users will not have given much thought to purchasing
some book until they decided to play with it in PCGen, and discovered
that they really liked what they saw and went out and bought that book.

Since PCGen doesn't give all the details about the various options, it's
important that it be easy to look up for those who do own the books.

Giving credit to the creators and letting users know where the option
came from if they want to look it up is all accomplished via the SOURCE:
tag which is available in all the main lst files.

The SOURCE tag in all list files and comes in 3 varieties;

-   <span class="underline"> ***SOURCELONG*** </span> - This is for the
    full company and source material name\
     e.g. SOURCELONG:Dominant Game Publisher - System Reference Document

-   <span class="underline"> ***SOURCESHORT*** </span> - This is the
    books 3-10 letter short name\
     e.g. SOURCESHORT:SRD

-   <span class="underline"> ***SOURCEWEB*** </span> - Is the URL of the
    publisher/source material\
     e.g. SOURCEWEB:HTTP://www.rpgpublisher.com/

All 3 of these tags <span class="underline"> **MUST** </span> appear in
<span class="underline"> **ALL** </span> pcc and lst files\*.

In the PCC file, the `SOURCExxx` tags must be on separate lines:

`SOURCELONG:Dominant Game Publisher - System Reference Document`

`SOURCESHORT:SRD`

`SOURCEWEB:HTTP://www.rpgpublisher.com/`

In LST files, the `SORCExxx` tags must be on one line, separated by a
tab delimiter:

> `SOURCELONG:Dominant Game Publisher - System Reference Document`
> &lt;tab&gt; `SOURCESHORT:SRD` &lt;tab&gt;
> `SOURCEWEB:HTTP://www.rpgpublisher.com/`

------------------------------------------------------------------------



