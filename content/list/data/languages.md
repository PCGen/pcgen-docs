+++
date = "2016-08-01"
title = "Language Files"
original_url = "/list/data/languages.html"

[menu.main]
    identifier = "data_languages"
    name = "Language Files"
    parent = "data"
    
+++
\*\*\* Updated 5.13.6

Most languages contain only two fields, the 'name' field which has no
tag label and the TYPE tag. The Languages list file is used with the
xxxskills.lst file for the CHOOSE:Language(&gt;list of names&lt;) tag.
This file also tells PCGen what languages are available for races to
choose from with their bonus languages based on their primary language
stat (usually Intelligence). Languages, like many other objects in
PCGen, can be qualified with PRExxx tags. For example the Druidic
language may only be learned by Druids so the Druidic entry contains a
`PREVARGTEQ:DruidicLanguage,1` tag which prevents the language from
appearing in chooser lists for the language skill or bonus languages.
Any Class or Race which grants Druidic as a bonus language must place a
`DEFINE:DruidicLanguage|1` tag in it to meet the prerequisite. This is
not needed if the language is granted automatically by the LANGAUTO tag
because it bypasses any prerequisites on the language.

`Terran`

The language named "Terran" is to be created.

`Celestial.MOD`

The language named "Celestial" is to be modified.

`Common.FORGET`

The language named "Common" is to be forgotten.

------------------------------------------------------------------------



