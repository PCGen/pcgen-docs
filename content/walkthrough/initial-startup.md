+++
date = "2016-08-01"
title = "Initial Start Up"
original_url = "/walkthrough/initial-startup.html"

[menu.main]
    identifier = "walkthrough_initial-startup"
    name = "Initial Start Up"
    parent = "walkthrough"
    
+++
Standard Startup
----------------

Whether you use <span class="lstfile"> pcgen.exe </span> or <span
class="lstfile"> pcgen.jar </span> to start up PCGen, the first thing
you will see is the splash screen with Da Vinci's Vitruvian Man logo and
the words PCGen written above it.

![Man & Machine DaVinci Image](../images/system/pcgen_main_logo.jpg)

From there, PCGen will load and take you to the Source Material Screen
where you can get started making your characters!

------------------------------------------------------------------------

<span id="cli"></span> Command Line Startup
-------------------------------------------

With the release of PCGen 5.17.11 PCGen added a new **Command Line
Interface** . To access the new command line interface you will use your
computer's **Terminal** program/application just as you would for any
command line interface. You will also need to change the current
directory to the pcgen directory.

The features included with the new Command Line interface are as
follows:

**Command Syntax:** pcgen \[-G\] \[-V\] \[-D
\[&lt;character\_sheet&gt;\]\] \[-v\] \[-s &lt;settings\_dir&gt;\] \[-m
&lt;campaign&gt;\] \[-p &lt;party\_file&gt;\] \[-c
&lt;character\_file&gt;\] \[-E \[&lt;character\_sheet&gt;\]\]

**Option:** -V (Print Version and exit)

**Option:** -G (Start in GMGen Mode)

**Option:** -D &lt;character\_sheet&gt; (Start in Character Sheet Mode.
Will use default character sheet if not specified.)

**Option:** -v (Set Logging Level to debug)

**Option:** -s &lt;settings directory&gt; (Use alternate settings
directory instead of the default)

**Option:** -m &lt;campaign mode&gt; (Load specified Campaign)

**Option:** -o &lt;file name&gt; (Output to specified file. If not
specified a default file name will be generated.)

**Option:** -p &lt;party file&gt; (Loaded specified PCGen Party)

**Option:** -c &lt;character file&gt; (Loaded specified PCGen Character)

**Option:** -E &lt;character sheet&gt; (Export character or party and
exit. Will use default character sheet if not specified.)

**What it does:**

-   Alters PCGen's initial configuration and launches as per the
    Standard Startup method, taking you to the Source Material Screen,
    unless the following options are used:
    -   If **-E** or **-V** are included PCGen will process the request
        and exit without starting the user interface.
    -   If **-G** or **-m** are specified PCGen will bypass the Source
        Material Screen.
-   All parameters are optional.
-   Allows PCGen to be used as a batch character sheet generator.
-   Both **-D** and **-E** require that either **-c** or **-p**
    be included.
-   When providing file names with an option, the file-path should begin
    in the pcgen folder.

**Example:**

`pcgen -E outputsheets/d20/fantasy/pdf/csheet_fantasy_std_blue.xslt -c "characters/Test Bard.pcg"`

Output the character <span class="lstfile"> characters/Test Bard.pcg
</span> to a PDF file using the <span class="lstfile">
csheet\_fantasy\_std\_blue.xslt sheet </span> .

`pcgen -E outputsheets/d20/fantasy/htmlxml/psheet_fantasy_std_PFRPG.htm -p "characters/The Testers.pcp"`

Output the listed party to html.

`pcgen -v -m "Pathfinder RPG for Players - Advanced"`

Startup with debug logging and load the **Pathfinder RPG for Players -
Advanced** set.

**Linux System Example:**

`pcgen.sh -- -v -m "Pathfinder RPG for Players - Advanced"`

Startup with debug logging and load the **Pathfinder RPG for Players -
Advanced** set.

------------------------------------------------------------------------



