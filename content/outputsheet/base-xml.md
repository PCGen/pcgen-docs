+++
date = "2016-08-01"
title = "base.xml File"
original_url = "/outputsheet/base-xml.html"

[menu.main]
    identifier = "outputsheet_base-xml"
    name = "base.xml File"
    parent = "outputsheet"
    
+++
The base.xml file contains the intelligence for the xslt PDF output
sheets and is the first file processed before passing it's output to the
final selected xslt sheet. The primary base.xml file can be found at the
root of the outputsheets directory.

<span class="new"> \*\*\* New 5.10 </span>

Mutiple gameMode specific base.xml files are now supported. If a
base.xml file is found in the root gameMode directory that file will be
used for xslt output. If no base.xml file is found in the gameMode
directory PCGen will default to the standard file found in the
outputsheets directory.

------------------------------------------------------------------------



