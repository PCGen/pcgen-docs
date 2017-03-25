+++
date = "2016-08-01"
title = "Out of Memory Issues"
original_url = "/faq/out-of-memory-and-java-issues.html"

[menu.main]
    identifier = "faq_out-of-memory-and-java-issues"
    name = "Out of Memory Issues"
    parent = "faq"
    
+++
How do I increase my memory?
----------------------------

### For Windows Users:

You increase the memory allotment by editing the *pcgen.bet* file.

-   Open the *pcgen.bat* file
-   Find and change the following code:
    -   **From:**
        `java -Xms128m -Xmx256m -jar pcgen.jar`
    -   **To:**
        `java -Xms256m -Xmx512m -jar pcgen.jar`
-   **Note:** `-Xms256` assigns starting memory for PCGen to 256Mb of
    RAM and should be enough memory for pcgen to run with lots of
    sources loaded.
-   **Note:** `-Xmx512` assigns a maximum of 512Mb of RAM to PCGen and
    should be enough memory for pcgen to run with lots more sources and
    characters loaded.

### For Mac Users:

You increase the memory allotment by editing the *info.plist* file,
which can be found in the 'Contents' folder inside of the PCGen app
package.

1.  Right-click, or commend-click, on the PCGen app and select 'Show
    Package Contents'.
2.  Double click on the 'Contents' folder. (If in Columns view, single
    click on the Contents folder.)
3.  Right-click, or command-click, on 'info.plist', selecting 'Open
    with' and then the application you wish to use to edit the file.
    Text Editor will work but if you have Property List Editor, things
    will work out better.
4.  Look for the following text: `-Xms128m -Xmx256m`
    1.  If you have 512MB of ram, you can change the text to the
        following: `-Xms256m -Xmx512m`
    2.  If you have 1GB of ram, you can change the text to the
        following: `-Xms512m -Xmx1024m`

5.  Save the file and relaunch PCGen.

### For Unix Users:

You can make the following change to the *pcgen.sh* file.:

1.  Open the *pcgen.sh* file.
2.  Find the following line: `java -jar ./pcgen.jar` . . .
3.  Replace it with the following line:
    `java -Xms256m -Xmx512m -jar ./pcgen.jar` . . .
4.  The values "256" and "512" are the "Minimum" and "Maximum" memory
    allocated to PCGen when it is run.
5.  The line of replacement code may also be run at the command line.

### Advice For All Users:

The following are a set of recommendations for all users irrespective of
what platform they are using:

-   Don't load sources that you don't need.
-   In Preferences, don't turn on the "Auto Create Equipment" feature.
    Use the provided equipment and custom create equipment as needed. To
    create custom equipment, right click on the basic equipement in the
    "Inventory/Gear" tab and add the desired enhancements to it.

------------------------------------------------------------------------

Java Issues
===========

What Java do I need?
--------------------

The following are the versions of Java required for PCGen (by PCGen
version)

 PCGen 6.x.x and above 
:   Java 8 or above

------------------------------------------------------------------------

How do I find out what version of Java I am running?
----------------------------------------------------

#### For Windows Users:

Go the command prompt and type:

`java -version`

You should get some kind of a response like:

`java version "1.8.0_112"
`Java(TM) SE Runtime Environment (build 1.8.0_112-b16)
`Java HotSpot(TM) 64-Bit Server VM (build 25.112-b16, mixed mode)

#### For Windows Vista Users:

If above does not work:

Open Control Panel:

Double click on the Java Icon

Open Java Page.

Open "Java Application Runtime Setting"

Open "User"

Click the Enabled button on any Java version other than 1.8.0\_00

Open "System"

Only have one in mine and its not selectable

#### For Unix/Mac Users:

Open a terminal window and enter:

`java -version`

You should get some kind of a response like:

`java version "1.8.0_112"
`Java(TM) SE Runtime Environment (build 1.8.0_112-b16)
`Java HotSpot(TM) 64-Bit Server VM (build 25.112-b16, mixed mode)

------------------------------------------------------------------------

Miscelaneous Error Messages
---------------------------

 **Bad command or file name** 
:   A common cause for this error is not having java installed. Go to
    <http://java.sun.com/> and download and install the latest java
    8 JRE. You'll then be able to run PCGen.

------------------------------------------------------------------------

Operating System Issues
=======================

#### For Vista and XP 64 Bit Users:

Question: Why doesn't Windows Vista/XP 64 run the *pcgen.bat* file?

Answer1: PCGen should be installed in the C:\\Program Files (x86)
folder.

Answer2: The other most common cause of this problem is that Windows is
not pointing the command "java" to the *java.exe* file.

Solution \#1: Create a new file called *PCGen.cmd* and then put the
following into it:

1.  `<Path to Java> -Dswing.aatext=true -Xms<Minimum Memory>m -Xmx<Maximum Memory>m -jar <Path to PcGen>`
    <div style="margin-left: 2em">

    `Example Vista: "C:\Program Files (x86)\Java\jre1.6.0_01\bin\java.exe" -Dswing.aatext=true -Xms256m -Xmx512m -jar "C:\Program Files (x86)\PCGen\PCGen5102\pcgen.jar"`

    </div>

2.  Put your paths and memory limits in as appropriate. If the path has
    a space in it, you need the quotes.
    1.  Sample Path to Java: "C:\\Program Files
        (x86)\\Java\\jre1.6.0\_01\\bin\\java.exe"
    2.  Minimum Memory: 768, Maximum Memory: 1024
    3.  Sample Path to PCGen: "E:\\PCGen5102\\"
    4.  Note: "Quotes" are required in path names that include spaces.

3.  Launch PCGen by running the *PCGen.cmd* file.

Solution \#2: Add the bin directory from your java install to the path.:

1.  Open the control panel.
2.  Open the system item.
3.  Select the advanced tab.
4.  Select "Continue" on the User Account Control.
5.  Click on the button marked environment variables.
6.  On my system "Path" is listed under the system variables.
7.  Click on the button marked EDIT....
8.  Look at Path for something similiar to what is in Solution \#1
    &lt;Path to Java&gt. If you have it, do nothing else, if you
    don't: proceed.
9.  Edit the path item. At the end of the Path statement, click and add
    the following ";&lt;Path to Java&gt;" i.e. ;"C:\\Program Files
    (x86)\\Java\\jre1.6.0\_01\\bin\\java.exe"
10. Then Restart the computer
11. Note: The path is a semi-colon (;) separated list.
12. See if you can launch PCGen by running the icon on the desktop from
    the program, If you can, you don't need the *pcgen.bat* file from
    Solution \#1.
13. Launch PCGen by running the *pcgen.bat* file.

#### For Fedora Users:

Question: Pcgen crashes on Fedora 7 just after the options directory
selection.

Answer: PCGen does not run under licgcj (GNU's Java library) because it
is incomplete (it is not a complete implementation of Java, especially
with respect to Swing (the UI)). You will need to download a complete
Java implementation, such as that from [Sun
Microsystems](http://java.sun.com/)

#### For Ubuntu Users:

The \#1 issue for PCGen users running on Ubuntu is that you need to use
the Sun Java implementation, not the default that ships with Ubuntu.

-   Check the version of Java being used: `$ java -version`
-   If not using Sun's JRE, you will need to install it. (see the Ubuntu
    wiki for help)
-   If Sun's Java is installed but not running, update the default java
    by using:
    -   `$ sudo update-alternatives --config java`\
         or
    -   `$ sudo update-alternatives --set \java /usr/lib/jvm/java-1.5.0-sun/jre/bin/java`\
         Note: Both command do the same thing (with the first command
        you get a list of possible java's and are asked to choose).
-   WARNING: Manually moving files and placing symbolic links might get
    the job done but is probably bad for the long-term health of
    your system. I think things might break with an update.

------------------------------------------------------------------------



