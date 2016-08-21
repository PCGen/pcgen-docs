+++
date = "2016-08-01"
title = "Upgrading PCGen"
original_url = "/installation/upgradepcgen.html"

[menu.main]
    identifier = "installation_upgradepcgen"
    name = "Upgrading PCGen"
    parent = "installation"
    
+++
If you have PCGen Currently installed on your system, you can overwrite
it with a newer version to maintain your settings and the location of
your characters. This will unfortunately, unless you have taken
precautions against it, also overwrite your homebrew datasets and
gamemode folder. This page provides some guidance in how best to avoid
these problems by helping you prepare your homebrew and custom data for
transfer into an updated version of PCGen.

NOTE: Additional information about upgrading PCGen versions may be
available in the [Release
Notes](http://sourceforge.net/docman/display_doc.php?docid=104618&group_id=25576)
.

------------------------------------------------------------------------

Important Files To Know About before the Upgrade
------------------------------------------------

The <span class="lstfile"> options.ini </span> and <span
class="lstfile"> filter.ini </span> files, see below, are automatically
stored in the users home directory and are picked up automatically when
PCGen is upgraded. If the old files are not desired, the new <span
class="lstfile"> filepaths.ini </span> file can be deleted. PCGen will
then ask for where the new files are to be placed.

<span class="lstfile"> filepaths.ini </span>

This file tells PCGen the location of the other ini files so you can
change the <span class="lstfile"> filepaths.ini </span> to point to the
folder which contains the <span class="lstfile"> options.ini </span> and
<span class="lstfile"> filter.ini </span> that you want to use.

<span class="lstfile"> options.ini </span>

This file holds your PCGen Preferences, such as file paths, so if you
are going to point to your old one you may need to correct various paths
to things such as the location of the output sheets.

WARNING: Installing a new version of PCGen over an old version may cause
the new version to not run well. If you experience some unexpected
behavior after upgrading, please try deleting the <span class="lstfile">
options.ini </span> file, or you may choose to rename it in order to
preserve the file. The <span class="lstfile"> options.ini </span> file
contains information on structure and contents that may have changed
with the new version, rendering it useless if different implementations
become mixed in the file.

<span class="lstfile"> filter.ini </span>

This file holds the various filters on each of the tabs. (See the filter
button in the docs)

See [Migrating Custom Data Sets](/installation/upgradepcgen.html#custom)
below.

Upgrading on the Windows Platform
---------------------------------

The steps for upgrading PCGen on the Windows platform are included
below:

1.  Create a new PCGen directory. e.g. *C:\\PCGen\\PCGen\_x.x.x* .
2.  Unzip the pcgenXXX\_full.zip into the new folder. (We recommend that
    you use the Windows install file for best results.)
3.  Copy the old <span class="lstfile"> \*.ini </span> files, custom
    datasets, homebrew datasets, and homebrew gamemode files, as
    required, back to your PCGen directory.

Note: Using the Windows installer automatically installs PCGen in a new
folder.

Upgrading on the Macintosh Platform
-----------------------------------

The steps for upgrading PCGen are included below:

1.  Download and mount the latest *pcgenXXX\_mac\_install.dmg* file.
2.  Locate the PCGen directory. e.g. *Applications/PCGen\_x.x.x* .
3.  Drag and drop *PCGen X.X.X.app* from the dmg file into the
    PCGen folder.
4.  Copy the old custom datasets, homebrew datasets, and homebrew
    gamemode files, as required, to the appropriate folders inside the
    PCGen application package. The package contents can be accessed by
    Command-Clicking (Right-Click) on the application package and
    pulling down to **Show Package Contents** .

<span id="custom"></span> Migrating Custom Data Sets
----------------------------------------------------

PCGen provides two simple ways of adding your own data, these are the
built-in LST Editors and the starter data set my\_dataset. Both of these
need some attention when upgrading PCGen.

WARNING: The data syntax for the old version of PCGen may be incorrect
for the new version so before you start up PCGen you should verify your
data's compatibility with the new version of PCGen. You can check with
the PCGen community forums to find out what tools may be available to
help you with this task.

### Migrating Data Created in the LST Editor

If, as is recommended, you install PCGen into a new directory each time
you upgrade, you will need to copy over the data created using the LST
Editors. To do this follow these steps.

1.  Stop PCGen, if it is currently running. PCGen must not be running
    when you copy the files, as PCGen writes a new copy of these files
    on exit.
2.  Copy the data/customsources folder and all of its contents from your
    old PCGen install directory to the new install directory.
3.  Start the new version of PCGen and verify that your custom data
    is present.
4.  If you install PCGen in the same directory as your previous install,
    your LST editor data will still be present in the new version.

### Migrating Data Created Using the My\_Dataset Files

PCGen ships with an example set of data files ready to go to create you
own data. This is in the data/homebrew/my\_dataset folder. As the
example files ship with PCGen, it is very important to note that these
can be overwritten by a new PCGen install if you have not renamed the
data set and install the new version of PCGen in the same location as
the old one.

As a result, we strongly recommend that when using the my\_dataset
example files, you create a copy in a new folder and work with that
copy, rather than editing the example files directly.

If you install PCGen into a new directory each time you upgrade, you may
need to copy over the data you have created. If you cannot see your
custom data, simply copy over the folder with your custom data to the
same location in the new PCGen install. The data should then be visible
when you restart PCGen.

If you are installing PCGen into the same directory, backup your custom
data first, then make sure it does not use the default my\_dataset
folder name. Once you are sure your data is safe, then proceed with the
upgrade of PCGen.

------------------------------------------------------------------------



