+++
date = "2016-08-01"
title = "PCC files"
original_url = "/list/data/pcc.html"

[menu.main]
    identifier = "data_pcc"
    name = "PCC files"
    parent = "data"
    
+++
The PCGen Campaign Configuration files are where you specify what you
want included in your campaign. It is the PCGen team's recommended
practice that your pcc files be located in the same directory as your
list files with the notable exception being if you have many files
spread between multiple directories. In this situation you should locate
a "master" pcc file in the main directory.

This page is divided into two sections:

**[Campaign File Building 101](/list/data/pcc.html#campaignbuilding)**

This section covers a few basic points to keep in mind when building
your own PCC file.

**[PCC File Tag List](/list/data/pcc.html#taglist)**

This section covers the syntax and function provided by the tags used in
the PCGen Campaign (PCC) files.

------------------------------------------------------------------------

<span id="campaignbuilding"></span> Campaign File Building 101
--------------------------------------------------------------

#### Notes on File Loading Order

LST file loading order is enforced by PCGen's loading system so it is
important to keep the following issues in mind when building a custom
PCC file:

-   PCC files will be loaded in the order of their appearance.
-   All LST files (e.g. Ability, Deity, Equipment, etc., but excluding
    embedded PCC files.) will be loaded in the order listed in the PCC
    file with the exception that Ability Category files will be loaded
    before Ability files.
-   Embedded PCC files, i.e. those contained within other PCC files,
    will be loaded after the files contained in the embedding PCC file.
    As an example:
    -   Given two PCC files, <span class="lstfile"> a.pcc </span> and
        <span class="lstfile"> b.pcc </span> , each containing an
        embedded PCC file <span class="lstfile"> aa.pcc </span> and
        <span class="lstfile"> ba.pcc </span> respectively, the order of
        processing is as follows:
        -   All LST files contained in <span class="lstfile"> a.pcc
            </span> are loaded with any Ability Category files being
            loaded before Ability files.
        -   All LST files contained in <span class="lstfile"> aa.pcc
            </span> are loaded with any Ability Category files being
            loaded before Ability files.
        -   All LST files contained in <span class="lstfile"> b.pcc
            </span> are loaded with any Ability Category files being
            loaded before Ability files.
        -   All LST files contained in <span class="lstfile"> ba.pcc
            </span> are loaded with any Ability Category files being
            loaded before Ability files.

#### Global Bonuses in PCC Files

Global `BONUS` tags can be included within a PCC file and will apply the
relevant bonus to every character created while that PCC file is loaded,
but it should be noted that this is the case only if the PCC is loaded
directly. Bonuses contained within embedded PCC files will **NOT** be
applied.

**Note:** You cannot use a colon (:) in the PCC file anywhere other than
immediately after LST tags, e.g. `CAMPAIGN:` , etc. Doing so will cause
PCGen to report errors and not load correctly.

Additional information on building your own Campaign files can be found
in LST File Classes [Lesson \#1: The PCC File: Campaign
Information](/list/lst-file-class/01-pcc.html) and [Lesson \#2: The PCC
File: Basic File Types](/list/lst-file-class/02-pcc.html) .

------------------------------------------------------------------------

<span id="taglist"></span>PCC File Tag List
-------------------------------------------

This section is divided into three sub-sections:

### <span id="datasettags"></span>Data Set and Campaign Information Tags

These tags provide information about the dataset.

The first two tags in the PCC file should be `CAMPAIGN` and `GAMEMODE` .
These are presented below out of alphabetical order to emphasize that
they are required tags which must be the first two lines in a PCC file.

-   [CAMPAIGN](/list/data/pcc/campaign.html)
-   [GAMEMODE](/list/data/pcc/gamemode.html)
-   [BOOKTYPE](/list/data/pcc/booktype.html)
-   [COPYRIGHT](/list/data/pcc/copyright.html)
-   [DESC](/list/data/pcc/desc.html)
-   [GENRE](/list/data/pcc/genre.html)
-   [HELP](/list/data/pcc/help.html)
-   [INFOTEXT](/list/data/pcc/infotext.html)
-   [ISMATURE](/list/data/pcc/ismature.html)
-   [ISOGL](/list/data/pcc/isogl.html)
-   [ISLICENSED](/list/data/pcc/islicensed.html)
-   [LICENSE](/list/data/pcc/license.html)
-   [PRECAMPAIGN](/list/data/pcc/precampaign.html)
-   [PUBNAMELONG](/list/data/pcc/pubnamelong.html)
-   [PUBNAMESHORT](/list/data/pcc/pubnameshort.html)
-   [PUBNAMEWEB](/list/data/pcc/pubnameweb.html)
-   [RANK](/list/data/pcc/rank.html)
-   [SETTING](/list/data/pcc/setting.html)
-   [SHOWINMENU](/list/data/pcc/showinmenu.html)
-   [SOURCELONG](/list/data/pcc/sourcelong.html)
-   [SOURCESHORT](/list/data/pcc/sourceshort.html)
-   [SOURCEWEB](/list/data/pcc/sourceweb.html)
-   [SOURCEDATE](/list/data/pcc/sourcedate.html)
-   [STATUS](/list/data/pcc/status.html)
-   [TYPE](/list/data/pcc/type.html)
-   [URL](/list/data/pcc/url.html)

### <span id="mainbodytags"></span>Main Body Tags

Loads the specific .lst files which make up the dataset.

The function of all main body tags is to tell PCGen to load a specific
file as part of that campaign file. There are three ways of doing this,
each dependant on where the file to be loaded can be found relative to
the *PCC* file.

#### Direct Loading

The first and most common is by a relative file path assuming a starting
point in the folder where the *PCC* file is stored. If the file to be
loaded and the *PCC* file that calls it are in the same directory then
all that is needed is the name of the file.

**Examples:**

`CLASS:fhbclasses.lst`

Loads the file fhbclasses.lst which is in the same directory as the .pcc
file calling it.

#### Absolute Loading

The second method is a special absolute path which is useful if you need
to call a specific file from a known location in the data or vendor
folder.

-   Using the 'at' symbol (@) and a file path will direct PCGen to look
    for the file in the *DATA* folder using the path specified.
-   Using the ampersand (&) and a file path will direct PCGen to look
    for the file in the *VENDOR* folder using the path specified.
-   Using the asterisk (\*) and a file path will direct PCGen to first
    attempt to locate the file in the *VENDOR* folder and then will look
    in the *DATE* folder.

**Examples:**

`SPELL:@/d20ogl/srd/srdspells.lst`

Loads the file from a path relative to the data folder.

`CLASS:&/complete_monkey/complete_monkey_classes.lst`

Loads the file from a path relative to the vendor data folder.

`EQUIPMENT:*/d20ogl/srd35/basics/rsrd_equip.lst`

Loads the file from a path relative to the vendor data folder and if
that does not exist, uses a path relative to the data folder.

#### Internet Loading

The third method is by loading data files over the internet. To do this
you must set PCGen's [Preferences](/menu/settings/pcgen/sources.html) to
allow this. You can then create a *PCC* file which uses a web address
instead of a file path to load source files.

**Examples:**

`CLASS:http://www.foogames.com/fhandbook/fhbclasses.lst`

Loads the source file from a web site.

**NOTE:** Do not use backslashes (\\) for directory separators in file
paths, use only forward slashes (/). backslashes work correctly on
Windows systems but cause problems on Unix flavored systems such as
Linux and Max OS X.

#### Multiple Files Per Object

The tags in this section can, and it is recommended for equipment, have
multiple lines. The names of the list files in the example column are
also only suggestions. To include the same type of files from the same
directory on the same line as a pipe-delimited (|) list of files, e.g.
`fhbarmorshields.lst|fhbequip|etc` . Sometimes, not all of these tags
are required by a source material. If a tag is not required, it cannot
be left blank, it must be commented out or deleted entirely. These tags
only tell PCGen where to go to get the information it needs, it points
it to the right spot. Each list file will be fully explained below,
separated by the list file name, with a full list of the tags that can
be used in each one.

#### Prerequisites on Main Body Tags

The `PRECAMPAIGN` tag can be appended to the end of any main body tag to
either include or exclude the loading of LST files, either in whole or
in part.

Examples:

`FEAT:source_feats_apg.lst|!PRECAMPAIGN:1,APG`

The <span class="lstfile">source\_feats\_apg.lst</span> file will be
loaded only if the APG Campaign file is not loaded.

`FEAT:source_feats_um.lst|!PRECAMPAIGN:1,UM`

The <span class="lstfile">source\_feats\_um.lst</span> file will be
loaded only if the UM Campaign file is not loaded.

`FEAT:source_feats_apg.lst|(INCLUDE:foo|bar)|PRECAMPAIGN:1,APG`

The <span class="lstfile">source\_feats\_apg.lst</span> file will be
loaded only if the APG Campaign file is not loaded.

`EQUIPMENT:../ultimate_combat/pfuc_equip_armor.lst|!PRECAMPAIGN:1,INCLUDES=Paizo - Pathfinder Roleplaying Game Ultimate Combat`

The <span
class="lstfile">../ultimate\_combat/pfuc\_equip\_armor.lst</span> file
will be loaded only if the loaded campaign files includes the *Paizo -
Pathfinder Roleplaying Game Ultimate Combat* campaign file.

-   [ABILITYPCC](/list/data/pcc/abilitypcc.html)
-   [ABILITYCATEGORY](/list/data/pcc/abilitycategory.html)
-   [ARMORPROF](/list/data/pcc/armorprof.html)
-   [BIOSET](/list/data/pcc/bioset.html)
-   [CLASS](/list/data/pcc/class.html)
-   [COMPANIONMOD](/list/data/pcc/companionmod.html)
-   [COVER](/list/data/pcc/cover.html)
-   [DEITY](/list/data/pcc/deity.html)
-   [DOMAIN](/list/data/pcc/domain.html)
-   [EQUIPMENT](/list/data/pcc/equipment.html)
-   [EQUIPMOD](/list/data/pcc/equipmod.html)
-   [KIT](/list/data/pcc/kit.html)
-   [LANGUAGE](/list/data/pcc/language.html)
-   [LOGO](/list/data/pcc/logo.html)
-   [PCC](/list/data/pcc/pcc.html)
-   [RACE](/list/data/pcc/race.html)
-   [SKILL](/list/data/pcc/skill.html)
-   [SHIELDPROF](/list/data/pcc/shieldprof.html)
-   [SPELL](/list/data/pcc/spell.html)
-   [TEMPLATE](/list/data/pcc/template.html)
-   [WEAPONPROF](/list/data/pcc/weaponprof.html)

### <span id="otherpcctags"></span>Other .pcc file tags

The tags below do not provide information about the dataset nor do they
load files by themselves but instead provide additional functionality.

-   [LSTEXCLUDE](/list/data/pcc/lstexclude.html)
-   [ALLOWDUPES](/list/data/pcc/allowdupes.html)
-   [INCLUDE](/list/data/pcc/include.html)
-   [EXCLUDE](/list/data/pcc/exclude.html)
-   [FORWARDREF](/list/data/pcc/forwardref.html)
-   [HIDETYPE](/list/data/pcc/hidetype.html)
-   [OPTION](/list/data/pcc/option.html)
-   [REQSKILL](/list/data/pcc/reqskill.html)

------------------------------------------------------------------------

