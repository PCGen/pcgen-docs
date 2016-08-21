+++
date = "2016-08-01"
title = "NPC Generator Data Files"
original_url = "/menu/file/npcgen-datafiles.html"

[menu.main]
    identifier = "file_npcgen-datafiles"
    name = "NPC Generator Data Files"
    parent = "file"
    
+++
The NPC generator uses XML formated data to establish the character
options, class data, and treasure data. The data files are located in
the *system/npcgen.options* , *system/npcgen/classdata* , and
*system/npcgen/treasure* folders respectively. Though the data files
that are used to support NPCGen may be modified by the user, requireing
a familiarity with XML, they were not designed to be extensible as the
LST file structure and tags were.

Class Data Files
----------------

The data-structure of the "class data" is defined in the file named
*classdata.xsd* while the actual data is contained in the file named
*classdata.xml* . Each gameMode will have its own XML file to establish
its own class data, though all gameModes will use the same
data-structure.

Options Data Files
------------------

The data-structure of the character "options" is defined in the file
named *options.xsd* while the actual data is contained in the file named
*optionsdata.xml* . Each gameMode will have its own XML file to
establish its own character options, though all gameModes will use the
same data-structure.

Treasure Data Files
-------------------

The data-structure of the "treasure" data is defined in the file named
*treasure.xsd* while the actual data is contained in the file named
*treasure.xml* . Each gameMode will have its own XML file to establish
its own treasure data, though all gameModes will use the same
data-structure.

------------------------------------------------------------------------



