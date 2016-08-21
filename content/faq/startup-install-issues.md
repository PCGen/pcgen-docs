+++
date = "2016-08-01"
title = "Startup and Installation Issues"
original_url = "/faq/startup-install-issues.html"

[menu.main]
    identifier = "faq_startup-install-issues"
    name = "Startup and Installation Issues"
    parent = "faq"
    
+++
1.  <span class="underline"> Where do I download PCGen from? </span>

    You can download the latest version of PCGen from:\
    <http://pcgen.org/> , see the **"Get PCGen"** tab which will answer
    all of your questions on this!

2.  <span class="underline"> How do I unzip the zipped up files? </span>

    Some of the install packages are zipped up. Those types of downloads
    **must** be unzipped to **the same directory / folder** . Unzipping
    is done differently on different platforms (don't ya hate that?).

    **Windows** users should download a zip utility such as
    [WinZip](http://www.winzip.com/) . Here are some sample instructions
    for WinZip. After WinZip has been installed, double-click the file.
    This will open the file in WinZip. On the menu-bar, click the
    "Extract to..." button, and enter the location where you want to
    have PCGen (Example: `c:\tools\pcgen` ). Make sure you have the
    "Include Subfolders" option checked!!

    **Mac OS X** users can simply double-click the file which unzips it.
    Then it is simply (we FAQ authors \_love\_ that word) a case of
    moving the new folder somewhere (preferably in the
    Applications folder).

    **Linux/Unix** users should use Gzip. Unix/Linux users by there
    nature should know what they are doing by now ;-)

    Or, as an alternative to the 3 above, you can download one of the
    platform-specific installer-files. \_Most\_ of these will do all the
    work for you if you just download them, and then double-click on
    whatever came down.

3.  <span class="underline"> How do I start PCGen? </span>

    -   In **Windows** , simply double-click **PCGen.bat** or
        **PCGen.Jar** .
    -   In **Mac OS 10.1+** , simply double-click **PCGen.jar** file, if
        you d/l'd the zipped file. If you installed PCGen from the Mac
        Install file you will simply doule-click on the PCGen
        application file copied to your hard-drive.
    -   In **Unix/Linux** , you need to execute `java -jar pcgen.jar` .\

4.  <span class="underline"> What do I need besides the zip-files to get
    the program running? </span>

    Glad you asked, because for many of you the instructions failed
    didn't they? Well here's why.

    Make sure that have the Java 2 v1.6.x or above Runtime Environment
    (or the SDK) installed on your machine. It's available from:
    <http://java.com/en/download/> .

    Mac users should note that Apple does not, and will not, support
    Java 2 v1.7.x or greater for Mac OSX 10.6.8 or earlier.

5.  <span class="underline"> Will PCGen run on my machine? </span>

    That depends. The one thing that decides if you can run PCGen or
    not, is whether you have at least JAVA 1.6+ installed. If you do,
    then it should run. If not, it won't. It really is that simple.

    However, some might want to check here, so here is a small list:

      -------------------------- --------------------------------------------------------------------------------------------------------------
      **OS**                     **Does it Work?**
      Mac OS 7.x - 9.x           No. (Actually, it might. As a work-around, you can install VirtualPC (or some such) and run PCGen in there.)
      Mac OSX 10 to 10.4         No
      Mac OSX 10.5+              Yes (Running Windows XP, Vista, or 7 on Boot Camp)
      Mac OSX 10.5.2 to 10.6.8   Yes (64bit Only)
      Mac OSX 10.7+              Yes (JRE 1.7+ required)
      Win 98                     No
      Win 98 SE                  No
      Win NT                     No
      Win 2000                   Yes (32bit Only)
      Win XP                     Yes
      Win Vista                  Yes
      Unix                       Yes
      Linux                      Yes
      -------------------------- --------------------------------------------------------------------------------------------------------------

    Not all of these configurations have been tested.

6.  <span class="underline"> Mac OSX telling me "PCGen can't be opened
    because . . . " </span>

    Starting with Mac OSX 10.7 Apple added an anti-malware application
    called the **Gatekeeper** . The purpose of this addition to the Mac
    OS was to restrict applications downloaded from the Internet
    from launching. Initially Gatekeeper had no teeth, requiring the
    user to "opt-in" as it's default startup settings were to allow
    everything to run. Starting with Mac OSX 10.8, Gatekeeper's default
    setting was changed to restrict everything that was not downloaded
    either from the App Store or from an otherwise
    "identified" developer. Fortunately Apple did provide for a
    workaround which is described below:

    **Gatekeeper Bypass Instructions**

    1.  Open System Preferences by choosing it from the Apple menu.
    2.  Select the "Security & Privacy" control panel and go to the
        "General" tab.
    3.  Under "Allow applications downloaded from:" click the radio
        button next to "Anywhere".
    4.  On the dialog box that pops up select the "Allow From Anywhere"
        button to change the setting and close the Preferences window.
    5.  Launch PCGen and verify that it is working. (If PCGen still
        doesn't launch please drop by the PCGen forum and provide
        a report.)
    6.  Relaunch System Preferences and change Gatekeeper's settings
        back to the original setting.

    \* - There are several different messages that can be seen as part
    of this issue including the following:\
     a. *"PCGen x.xx.xx" can't be opened because it is from an
    unidentified developer.*\
     b. *"PCGen x.xx.xx" is damaged and can't be opened. You should move
    it to the Trash.*

    The installed version of PCGen will now run without the need to
    change Gatekeeper's setting.

7.  <span class="underline"> Why is the Source "Load" tab all grey?
    </span>

    This might be because your machine have a problem finding the files
    PCGen refers to. There is no easy way to fix this (there never is).
    There are machine-specific releases of PCGen available, but unless
    you choose to use one of these, you'll have to manually change the
    addressing in the files you're to access. Normally this is a case of
    changing a `/` to a `\` or the other way round. Also make sure that
    you don't try to access something like `c:/program files/pcgen/`
    when you should be accessing `c:/program~1/pcgen/` , or vice versa.

    Note that on Windows, enclosing the entire path in double quotation
    marks is an acceptable way to accessing the directory, i.e.
    `"c:\program files\pcgen\"` .

8.  <span class="underline"> Why can't I make a new character? The "New"
    menu-item is grayed out. </span>

    This is probably the most asked question so far. The answer is this:
    Before you can make a character, you must tell PCGen which rule
    books it should use. In other words, you must load one or more
    source books or modules listed under the "Source Material"-tab
    before you can make a new character. Make sure that at least one
    module is marked by a "Y" instead of a "N".

    You might wonder why PCGen doesn't do this automatically. This is
    because PCGen is made to be a RPG-generator. As it stands now, you
    may choose to load a Fantasy, Sci-Fi or Contempory module instead.
    Had PCGen automatically loaded a module, say the Fantasy module, it
    would have been the wrong one and you would then grumble about our
    stupid defaults while you unloaded that module so you could then
    load the module you wanted, the Sci-Fi RPG-character.

    There are options to load sources on start up or as you open a PC,
    take your pick, we don't mind ;-).

9.  <span class="underline"> What values can be passed in on the command
    line? </span>

    When runing pcgen form the command line, the following options
    are recognised. Please note that the options are expected to
    formatted as -Doption=value

    -   **pcgen.filepaths** - Specify the location of the filepaths
        file, which lists where the other settings files are expected.
    -   **pcgen.options** - Specify the location of the options file,
        which lists what options have been selected, mainly in the
        preferences section.
    -   **pcgen.filter** - Specify the location of the filter file,
        which lists what filters were last selected for each tab.
    -   **pcgen.templatefile** - Specify the character sheet template
        file to be used for automatically generating a character sheet.
    -   **pcgen.inputfile** - Specify the PCG file of the character to
        be used for automatically generating a character sheet.
    -   **pcgen.outputfile** - Specify the name of the output file in
        which the automatically generated character sheet will
        be stored.

    When a value is specified for pcgen.inputfile, the program runs in
    command line only mode and does not display the gui, but instead
    generates a character sheet and exits.

    In addition you can provide any number of character or party files
    for PCGen to load on startup by just listing them on the
    command line.

------------------------------------------------------------------------



