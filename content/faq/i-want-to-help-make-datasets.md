+++
date = "2016-08-01"
title = "I Want to Help to Make Datasets"
original_url = "/faq/i-want-to-help-make-datasets.html"

[menu.main]
    identifier = "faq_i-want-to-help-make-datasets"
    name = "I Want to Help to Make Datasets"
    parent = "faq"
    
+++
<span class="underline">How do I get started?</span>

1.  First do you have the current version of PcGen running on
    your system. If you do then you have Java installed and are ready
    for fun. If you need help, open a command box and type:

    `java -version`

    And you should get something like:

    `java version "1.5.0_06"`

    `Java(TM) 2 Runtime Environment, Standard Edition (build 1.5.0_06-b05)`

    `Java HotSpot(TM) Client VM (build 1.5.0_06-b05, mixed mode, sharing)`

    If you don't, you need to get it from Sun Systems.
    [**http://www.sun.com/java/**](http://www.sun.com/java/)

    If you're having problems with the operation of PCGen you likely
    have a "less-than-complete" version of Java and need to replace it,
    see above.

    Java comes in two variety's, the JRE that you need and the JDK that
    you don't unless you are planning on coding the PCGen
    program itself.

2.  Secondly you should have a look at what is in your library at home
    and compare that against what is listed in
    [Sources](/credits/publishers-and-sources.html#sources) and see if
    we already have that product in PCGen. If not then check the
    [Publisher
    Permissions](/credits/publishers-and-sources.html#publishers)
    section to see if we have permission to create a dataset for
    that publisher.

3.  This next section no longer holds true, we are working on removing
    this information and putting it into these docs instead.

    The wiki is at: [**http://wiki.pcgen.org/**](http://wiki.pcgen.org/)

    Find the link marked Publishers, that's the list of "The following
    publishers have either Supported Datasets, Alpha Datasets or have
    been requested as part of New Data set Wishlist."

    What the separations mean:

    Supported Datasets - Been thrown in the mill and tested and used and
    we think they are right.

    Alpha Datasets - Fully tested as we can, now its time for the users
    to use them and figure what's wrong and tell us all about it.

    Click the link 'New Data set Wishlist", there is everything that
    someone wants that we have permission to do.

    Click on the "SourcesInDevelopment" and that's one of the two places
    to find out who is working on what. If you are working on something
    list it here. The other is at [**the JIRA
    issue tracker.**](http://jira.pcgen.org/)

    This is a look but don't mess with place.

    The three/four newsgroups you might want to monitor:

    1.  PcGen main discussion - pcgen@yahoogroups.com at
        [**http://games.groups.yahoo.com/group/pcgen/**](http://games.groups.yahoo.com/group/pcgen/)
    2.  PcGen Tag discussion - PcGen\_Experimental@yahoogroups.com at
        [**http://groups.yahoo.com/group/pcgen\_experimental/**](http://groups.yahoo.com/group/pcgen_experimental/)
    3.  PcGen Lst File Help - PCGenListFileHelp@yahoogroups.com at
        [**http://groups.yahoo.com/group/PCGenListFileHelp/**](http://groups.yahoo.com/group/PCGenListFileHelp/)
    4.  For Developers -
        [**https://lists.sourceforge.net/lists/listinfo/pcgen-devel**](https://lists.sourceforge.net/lists/listinfo/pcgen-devel)
    5.  For International -
        [**http://tech.groups.yahoo.com/group/pcgen\_international**](http://tech.groups.yahoo.com/group/pcgen_international)

4.  Ok so we have figured out that you have PcGen and a book to code, so
    how to make a dataset. Open the PcGen directory, open the docs
    directory, down at the bottom are a bunch of .html files:

    -   `greetings.html` - just that a greeting from us to the user.
        Used in index.html
    -   `index.html` - combination of help and documentation. This is
        the same help file accessed from inside the program. It tells
        new/old users all they need to know. Check often it does change.
        I'll probably put this up there somewhere.
    -   `navlistindex.html` - Documents all of the lst tags that we
        know of. This is the one that you want.
    -   `navtokenindex.html` - this is the output sheet tags (they call
        then tokens), if you need to make a output sheet this is the
        instructions and index.html has a section on output sheets, the
        making of.
    -   `navtree.html` - the is the selector part of index.html.

5.  Ok you know where the tags are located (navlistindex.html), you have
    a book, now you need an editor to work in. You can use the built in
    editor if it saves as text only, with no special formatting, or you
    can try a special editor with syntax coloring.

    Windows Systems:

    Notepad

    Notepad++
    [**https://notepad-plus-plus.org/**](https://notepad-plus-plus.org/)

    Wordpad

    Crimson Editor:
    [**http://www.crimsoneditor.com/**](http://www.crimsoneditor.com/)

    TextPad:
    [**http://www.textpad.com/index.html**](http://www.textpad.com/index.html)

    UltraEdit:
    [**http://www.ultraedit.com/**](http://www.ultraedit.com/)

    Mac OS X, OS/2, Unix, VMS and Windows:

    jEdit: [**http://www.jedit.org/**](http://www.jedit.org/)

    PSPad: [**http://www.pspad.com/**](http://www.pspad.com/)

    Vim: [**http://www.vim.org**](http://www.vim.org)

    Mac OS X

    TextMate: [**http://macromates.com/**](http://macromates.com/)

    BBEdit:
    [**http://www.barebones.com/products/bbedit/**](http://www.barebones.com/products/bbedit/)

6.  Go over to Experimental
    [**http://groups.yahoo.com/group/pcgen\_experimental/**](http://groups.yahoo.com/group/pcgen_experimental/)
    , go into the files, (err you do have a yahoo account don't you,
    their free and I keep being asked my password to get in so.) and
    down towards the bottom is the folder Application Support, this
    holds most of the editors that we have syntax modules for. If you
    want to use one and need help, just ask on PcGen if you can't find a
    thread about it in the archives. While you are there download a copy
    of prettylst\_1-35\_ build-561.zip or whatever prettylst.zip that
    is there.

    While you are there look in the files marked:

    Step 1 - WORK IN PROGRESS, INCOMPLETE DATASETS GO HERE

    New datasets and work in progress (Once completed move to Step 2 and
    the senior data monkeys will begin the review process)

    This will have the partial datasets that the developer ran out of
    time to do. You might check and see if someone did some work
    on yours.

    Go ahead and look through the rest of them, they basically tell you
    the way the submission process goes.

7.  Ok now you have all the bits and pieces that you need. Almost. Did
    you close your docs directory, well you need to go up one level and
    open the data directory.

    alpha directory - Remember the Alpha Datasets, this is where they
    are placed.

    customsources directory - No young Grasshopper, this is not for you,
    this is where PcGen places custom items it creates inside
    the program. Unless its code is in the character it never looks at
    this directory for any reason.

    d20ogl directory - Remember the Supported Datasets, this is where
    they are placed.

    homebrew directory - This is where you will find a directory with a
    blank starter dataset, both titled <span
    class="lstfile">my\_dataset</span>, for you to play with. One thing
    to keep in mind when using this dataset is that you will need to
    move this set to the next version of the program when you upgrade.

    permissioned directory - Remember the New Data set Wishlist, this is
    where they are placed. After they are passed threw Step 2 and later.
    Until then...

    Either make a new directory and drop the starter set in it and copy
    as needed, or as a lot of other people are doing and moving the
    datafile directory outside PcGen directory structure. To just right
    off the drive root,

    Inside the program is the Preferences screen (do you still have the
    docs directory open? Double click on the index.html, click on the
    Menu Items -&gt; Settings Menu -&gt; Preferences Menu -&gt; PCGen
    Menu -&gt; Location ). You are now looking at the configuration
    screen for darn near everything. Please note one thing, there is no
    reset to factory button. You mess this up and its reinstall time,
    including the homebrew directory if you don't take steps to
    protect it.

    What I am pointing out is two fields only at this time:

    The Custom Directory - This is where the list files for custom
    source files generated by the list editors are located. Point this
    at where you put your now custom directory.

    The Vendor Data Directory - This is where the list files for
    additional source files produced by third parties of the users
    are located.

    You may not have found out yet, but PcGen has a total removal built
    in to the program, with no verify that you mean to remove the whole
    thing, the next thing you know everything, including the files that
    you spent six months on are gone. So get that directory clear of the
    program and pit it just off the root of the drive, you need it there
    in the future.

    All this reading, downloading, and snooping and no coding yet. Nope
    still some other things first.

    Go to the directory that you made, go in and make a copy of the
    homebrew directory and name the directory (in abbreviated form)
    after your book. See the data directory for ideas. I'm coding the
    d20 Weapons Locker by Wizard of the Coast. That's a long name,
    shortened to d20WL.

    Now open the copy of the directory and stick the shortened name in
    front of the files in there (go from my\_\_campaign.pcc
    to d20WL\_my\_\_campaign.pcc). Don't get attached, the publisher
    gets final say on the product I do believe.

    Now your ready to dive in and start coding the dataset. Did you
    close the index.html, if you did, reopen it, if you didn't close
    everything and open the List Files -&gt; LST File Class (My goodness
    someone did some classes) -&gt; Lesson \#1: PCC - Campaign Info..
    The information may be old, but its still useful and if you want to
    get the new classes as they come out:

    [**http://groups.yahoo.com/group/lstfileclass**](http://groups.yahoo.com/group/lstfileclass)

    There is a bunch of new tags out, so there is a rewrite of old
    classes and new classes for not yet covered items.

    Have questions about how to setup a tag, ask on
    [**PCGenListFileHelp**](http://groups.yahoo.com/group/PCGenListFileHelp),
    remember don't ask about the non-OGL, but feel free to ask about
    anything else including Foo items. A food item might sound a lot
    like a non-OGL item, but since its not using the Product Identity
    name (PI) that can't be used its permitted, Besides I don't have a
    certain book that is non-OGL that is sold over at [**Code Monkey
    Publishing**](http://www.codemonkeypublishing.com/) in a dataset
    format that we can almost use (you need their core rule set as well
    to use their datasets) but I have feats that come out of it,
    inflicted on me by the GM. So I know the name and the effects. I
    just call it a food feat that gives me a capability to move
    underwater and someone comes back with the appropriate combination
    of tags to give me the movement underwater that I lack and the
    movement rate.

    So you have a bunch of files in a directory to be checked (either
    for your own use or for inclusion in the repository). A month or two
    later do you really think you remember where you put the
    prettylst.zip that I had you download. I'll tell you right now that
    the version of prettylst that I have hates two part words, so if the
    word Program Files (or any other phrases that have a space in them)
    is between prettylst and your custom directory, its time to move the
    directory to where I told you.

    There is one more file that you need to find, download and install.
    Get Perl. It is necessary to run prettylst. You can use Active Perl
    from http://www.activestate.com/Products/ActivePerl/ or find another
    distribution at http://www.cpan.org/ports/index.html. Just install
    Perl and you are ready to go.

    Ok open a command line box and type

    perl prettylst.pl -h

    ===========================

    Microsoft Windows XP \[Version 5.1.2600\]

    © Copyright 1985-2001 Microsoft Corp.

    C:\\Documents and Settings\\Owner&gt;cd C:\\prettylst

    C:\\prettylst&gt;perl prettylst.pl -h

    prettylst.pl version: 1.35 (build 561) -- 2006.03.14

    Usage:

    \# parse all the files in PATH, create the new ones in NEWPATH

    \# parse all the files in PATH, create the new ones in NEWPATH

    \# and produce a report of the TAG in usage

    perl prettylst.pl -inputpath=&lt;PATH&gt;
    -outputpath=&lt;NEWPATH&gt; -report

    perl prettylst.pl -i=&lt;PATH&gt; -o=&lt;NEWPATH&gt; -r

    \# parse all the files in PATH and write the error messages in
    ERROR\_FILE

    \# without creating any new files

    perl prettylst.pl -inputpath=&lt;PATH&gt;
    -outputerror=&lt;ERROR\_FILE&gt;

    perl prettylst.pl -i=&lt;PATH&gt; -e=&lt;ERROR\_FILE&gt;

    \# parse all the files in PATH and write the error messages in
    ERROR\_FILE

    \# without creating any new files

    \# A compilation of cross-checking (xcheck) errors will not be
    displayed and

    \# only the messages of warning level notice or worst will
    be outputed.

    perl prettylst.pl -noxcheck -warninglevel=notice
    -inputpath=&lt;PATH&gt;

    -output error=&lt;ERROR\_FILE&gt;

    perl prettylst.pl -nx -wl=notice -i=&lt;PATH&gt;
    -e=&lt;ERROR\_FILE&gt;

    \# parse all the files in PATH and created new ones in NEWPATH

    \# by applaying the convertion pcgen5713. The output is redirected

    \# to ERROR\_FILE

    perl prettylst.pl -inputpath=&lt;PATH&gt;
    -outputpath=&lt;NEWPATH&gt; \\

    -outputerror=&lt;ERROR\_FILE&gt; -convert=pcgen5713

    perl prettylst.pl -i=&lt;PATH&gt; -o=&lt;NEWPATH&gt;
    -e=&lt;ERROR\_FILE&gt; -c=pcgen5713

    \# display the usage guide lines

    perl prettylst.pl -help

    perl prettylst.pl -h

    perl prettylst.pl -?

    \# display the complete documentation

    perl prettylst.pl -man

    \# generate and attemp to display a html file for

    \# the complete documentation

    perl prettylst.pl -htmlhelp

    C:\\prettylst&gt;

    =================================

    You don't get the == but you get the rest. Its the
    short instructions.

    I use command lines saves to a word document. The first:

    perl prettylst.pl
    -i=c:\\prettylst\\my\_customfiles\\d20\_weapons\_locker

    -o=c:\\prettylst\\sort -e=c:\\prettylst\\error\\d20wl\_error.txt

    and what it means:

    perl prettylst.pl

    Calls the perl oerating system and tells it to start rettylsy.pl

    -i=c:\\prettylst\\my\_customfiles\\d20\_weapons\_locker

    This is the line that tells it where the input directory is at

    -o=c:\\prettylst\\sort

    This tells it where to put the output, prettylst will create new
    files that it works on and this is where it is it. Rettylst not only
    tell you the wrong tags that you are using, but it also reformats it
    according to someone's standards

    -e=c:\\prettylst\\error\\d20wl\_error.txt

    This is the error report. Lets take a close-up look at one of mine:

    ================================================================

    List of files that are not referenced by any .PCC files

    ----------------------------------------------------------------

    \\Helpful Hints.txt

    \\OGL.txt

    \\d20WL\_equip.lst

    \\d20WL\_equip\_weap\_antimaterial.lst

    \\d20WL\_equip\_weap\_machine\_guns.lst

    \\d20WL\_equip\_weap\_submachine\_guns.lst

    \\d20WL\_equipmods.lst

    These are files in the directory that are not active in the
    d20WL.pcc

    ================================================================

    Messages generated while parsing the .LST files

    ----------------------------------------------------------------

    c:\\prettylst\\my\_customfiles\\d20\_weapons\_locker\\d20WL\_equip\_weap\_pistols.lst

    (Line 33): The tag "CONTAINS" should not be used more than once on
    the same EQUIPMENT line.

    (Line 33): The tag "CONTAINS" should not be used more than once on
    the same EQUIPMENT line.

    (Line 35): The tag "CONTAINS" should not be used more than once on
    the same EQUIPMENT line.

    (Line 36): The tag "CONTAINS" should not be used more than once on
    the same EQUIPMENT line.

    (Line 39): The tag "CONTAINS" should not be used more than once on
    the same EQUIPMENT line.

    (Line 40): The tag "CONTAINS" should not be used more than once on
    the same EQUIPMENT line.

    (Line 51): The tag "CONTAINS" should not be used more than once on
    the same EQUIPMENT line.

    I was trying to use two CONTAINS per some weapon, one for the
    ammunition, one for the attachments. Up at the very top just before
    the first error is:

    c:\\prettylst\\my\_customfiles\\d20\_weapons\_locker\\d20WL\_equip\_weap\_pistols.lst

    this is the file involved. The (Line 51): is the line number of the
    file, to make it easier, get an editor that has line
    number capability.

    I got a similar read out on assault rifles, sniper rifles, along
    with some other errors:

    (Line 316): The tag "YPE" from

    "YPE:Weapon.Ranged.Standard.Firearm.Longarm.Assault.GrenadeLauncher.Container.
    Ballistic.Military.Automatic.Semiauto.Projectile" is not in the
    EQUIPMENT tag list

    Oops should have been TYPE. Imagine if this didn't have the line
    number and I didn't line up all of my columns of tags.

    ================================================================

    List of files that were created in the directory

    c:\\prettylst\\sort

    ----------------------------------------------------------------

    \\d20WL.pcc

    \\d20WL\_equip\_weap.lst

    \\d20WL\_equip\_weap\_ammo.lst

    \\d20WL\_equip\_weap\_grenade\_launchers.lst

    \\d20WL\_equip\_weap\_melee.lst

    \\d20WL\_equip\_weap\_pistols.lst

    \\d20WL\_equip\_weap\_rifles.lst

    \\d20WL\_equip\_weap\_sniper.lst

    \\d20WL\_weaponprofs.lst

    This is a list of the files that it looked at and filed a error
    report on and created new versions in the /SORT directory

    ================================================================

    ================================================================

    Invalid tags found

    ----------------------------------------------------------------

    Line Type: EQUIPMENT

    YPE 1

    Total:

    YPE 1

    Lists the show stoppers.

    When you get a no errors found, that's the time to try it in PcGen
    to find all of the other errors.

    Lets take a look at some of the other errors and what they mean:

    (Line 51): Invalid save check name "Willpower" found in
    "BONUS:CHECKS|BASE.Willpower|(((CL+1)\*5)/13)+1"

    We changed from Willpower to Will

    \*=&gt;(Line 12): The tag "." is missing a value (or you forgot a
    : somewhere)

    (Line 12): The tag "." from "." is not in the FEAT tag list

    There is an extra period somewhere on line 12

    (Line 12): The tag "VISIBLE:.CLEAR" from "VISIBLE:.CLEAR.NO" is not
    in the FEAT tag list

    (Line 12): Invalid value ".CLEAR.NO" for tag "VISIBLE"

    (Line 12): The tag "VISIBLE" should not be used more than once on
    the same FEAT line.

    Can't do this.

    (Line 17): Forgot to use var()? Dubious use of Jep variable
    assignation near "AreaCovered=" in "SA:Area Effect- The area is
    figured by taking your constitution score and dividing it by 4 to
    get the total number of yards in the area. % area
    covered.|AreaCovered=4\*CON"

    (Line 55): No SKILL entry for "CSKILL:Concentration"

    (Line 55): No SKILL entry for "CSKILL:Craft"

    (Line 55): No SKILL entry for "CSKILL:Listen"

    (Line 55): No SKILL entry for "CSKILL:Profession"

    (Line 55): No SKILL entry for "CSKILL:Read/Write Language"

    Loading the campaign with out the core.

    c:\\prettylst\\mycustomfiles\\stargate\\stargate.pcc

    (Line 4): Invalid GAMEMODE "Stargate" in "GAMEMODE:Stargate"

    \*=&gt;(Line 106): The tag "FEATAUTO:" is missing a value (or you
    forgot a : somewhere)

    \*=&gt;(Line 107): The tag "FEATAUTO:" is missing a value (or you
    forgot a : somewhere)

    \*=&gt;(Line 108): The tag "FEATAUTO:" is missing a value (or you
    forgot a : somewhere)

    Oh well you get the notion. Hopefully this has not scared you into
    the next state over. Just remember we're from all over the world.
    Whereever you go we're already there.

------------------------------------------------------------------------

[![Valid HTML 4.01
Strict](../images/system/valid-html401.png)](http://validator.w3.org/check?uri=referer)

