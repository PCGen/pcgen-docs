+++
date = "2016-08-01"
title = "Game Rules Reading Guide"
original_url = "/list/rules-guide/reading-instructions.html"

[menu.main]
    identifier = "rules-guide_reading-instructions"
    name = "Game Rules Reading Guide"
    parent = "rules-guide"
    
+++
This page provides guidance in reading and understanding the game rules
implementation examples contained in the [Game Rules Implementation
Guide](/list/rules-guide/rules-guide_index.html) .

<span id="conventions"></span> Style Conventions
------------------------------------------------

Because HTML formatting cannot exactly replicate what you would see in a
LST file we are going to use certain conventions to convey these ideas.

 *&lt;TAB&gt; Delimiting* 
:   Tags in LST files are &lt;TAB&gt; delimited, that is, the tags are
    separated by TABs. Because this is difficult to show, the LST
    examples will have their tags separated by simple line breaks with
    no additional indentation.

 *LST Code* 
:   Text meant to display LST code will be in the `code font` .

 *LST Objects* 
:   LST objects will be displayed the <span class="lstobj"> LST object
    font </span> .

 *LST Variables* 
:   LST variables will be displayed the <span class="lstvar"> LST
    variable font </span> .

 Source Text 
:   Text taken from source will be indicated in **bold** .

 *Extended LST Lines* 
:   To improve readability, long LST tags will be formated with
    line-breaks with the subsequent lines indented.

<span id="template"></span> Rules Implementation Page Template
--------------------------------------------------------------

> **Rule Description:** A brief description of the rule being
> implemented.
>
> **PCGen Version:** The version of PCGen used to develop this
> implementation.
>
> **Gamemode/Dataset:** The gamemode/datasets used by the author to
> implement this rule.
>
> **File(s) Covered:** The files modified during this implementation.
>
> **Tags Used:**
>
> Links to the LST FIle Index for the tags used in this implementation
>
> NOTE: In this section we will discuss only those LST tags specific to
> this implementation. For more general information on the associated
> tags, please visit the [LST File Tag Index](/navlistindex.html)
> section of the PCGen Documentation.
>
> **Implementation Description:** A detailed description of the
> implementation, including a summary of the LST files (i.e. feat.lst,
> class.lst, etc.) and LST objects (i.e. feats, spells, deities, etc.),
> that will be required. If the rule being implemented has been
> incorporated into a PCGen distributed set, this sub-section will also
> include instructions for using the rule in new LST objects.
>
> **LST File Entry:** Discussion of each LST file being modified is
> provided and includes an explanation of each tag used for the specific
> implementation of the required LST objects. The information presented
> here is similar to that found in the [LST File Tag
> Index](/navlistindex.html) , but is tailered to the specific
> requirements of the implementation.
>
> > **Tag Used:** The LST tag in its specific form as used in this
> > implementation.
> >
> > **Variables Used:** The variables used and what they represent. This
> > information will only be provided if the "Tag Used" includes
> > variables.
> >
> > **What it Does:** A brief explanation of what the "Tag Used" will
> > do, including specific information on allowable values for
> > variables.
> >
> > **Sub-Tag Used:** The LST tag in its specific form that is used as
> > part of the "Tag Used". This entry is otherwise treated as the "Tag
> > Used" entry above, including descrption of the variables used and
> > what it will do.
>
> **Known Issues:** Any issues or quirks with the LST code are briefly
> mentioned. This may involve specific user instructions or simple
> "things to remember".
>
> **LST File Entry Examples:** An example of each of the LST objects
> recuired to implement the subject rule is provided and includes all
> tags covered in the rule implementatin page. Simple objects are
> presented using the minimum tags required to make a functional LST
> object.
>
> **Variations on a Theme:** Hints may be provided on how to expand the
> scope of the specific rule being described.

------------------------------------------------------------------------



