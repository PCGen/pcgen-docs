+++
date = "2016-08-01"
title = "Installing PCGen Manually"
original_url = "/installation/pcgen.html"

[menu.main]
    identifier = "installation_pcgen"
    name = "Installing PCGen Manually"
    parent = "installation"
    
+++
If you have PCGen currently installed on your system, you can either
install the new version into a new directory or overwrite the old
version on your system. The PCGen team recommends strongly that you
install new versions into a new directory.

Windows Users
-------------

We recommend that you use the Windows installer.

Mac Users
---------

We recommend that you use the OSX Mac Installer,
*pcgenXXX\_mac\_install.dmg* .

This configuration of the program includes all the necessary files
included with the program package, or app file. You can still access the
files by right clicking the program and choosing **Show Package
Contents** . See the notes included in the installer for all the
details.

Other System (or Advanced) Users
--------------------------------

Pick the package with the features you want and unzip it. It is highly
recommended that you use a new directory for every new release. Once the
package is unzipped, see *docs\\index.html* for the full documentation.

Note: Installing a new version over an old version of PCGen may not run
well. See [Upgrading PCGen](/installation/upgradepcgen.html) for further
info.

A fresh install is best performed by *unzipping pcgenXXX\_full.zip* to a
desired folder on your computer. To run the application, run either
*pcgen.jar* (the Java executable) or *pcgen.bat* (Windows, which will
also open a debug window which will display any errors during the run)
or pcgen.sh (UNIX and Linux).

To transfer characters from one version of PCGen to the new version of
PCGen, copy the pcg files from the "characters" directory from the old
version of PCGen to the new version.

NOTE: If you copy PCGen from one location to another you must delete the
*options.ini* file. This file holds directory locations that will no
longer be valid! Deleting the options.ini file will reset PCGen to all
its default settings. As such, note your current settings before
proceeding. A new file will be created when PCGen is started if
necessary.

------------------------------------------------------------------------



