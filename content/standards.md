+++
date = "2016-08-01"
title = "Documentation Standards"
original_url = "/standards.html"

[menu.main]
    identifier = "_standards"
    name = "Documentation Standards"
    parent = ""
    weight = 20
    
+++
This page will be used to provide standards to follow in the creation of
documentation pages for PCGen.

General Documentation Standards
-------------------------------

1.  Each page should have information commented in the page which should
    contain the names of those contributing to the creation and
    maintenance of the page. There should also be a brief description of
    the purpose of the page and in the case of LST File Tag Pages, a
    basic to how to create the specific LST Objects covered by
    that page.
2.  The documentation should, in general, document what PCGen, with its
    LST Tags and OS Tokens, DO. Instances of documenting what PCGen WONT
    do should be minimized.

LST Tag Documentation Standards
-------------------------------

The following is a generic example of the format to be used when
documenting LST tags. You can copy the code and use it as a starting
point for new entries if you wish. Following the entry will be a
detailed explanation of how the format is should be used.

------------------------------------------------------------------------

\*\*\* New

**<span id="taganchor"></span> Tag Name:** TAG:x

**Variables Used (x):** Text (Explanation)

**Variables Used (x):** Number (Explanation)

**Variables Used (x):** Property (Explanation)

**What it does:**

Explanation of what this tag does and how to use it.

**Example:**

`TAG:EXAMPLE`

Description of what this example tag does.

**Deprecated Syntax:**

`TAG:EXAMPLE`

Identify deprecated syntax.

**Where it is used:**

Explanation of where this tag may be used in terms of lines and files.

------------------------------------------------------------------------

### Anchors

If you examine the source code you will see that the first line of the
entry contains a named anchor next to the horizontal rule. This is so
the entry can be linked to from the index and other relevant entries.
The anchor name should match the tag name up to the first variable minus
any symbols used. See the source code for examples

### State of the entry

Some entries are labeled " <span class="lstnew"> New </span> "/" <span
class="lststatus"> New </span> ", " <span class="lstupnew"> Updated
</span> "/" <span class="lststatus"> Updated </span> ", or " <span
class="lstdep"> Deprecated </span> ". When the state of a tag entry has
changed in the current or immediately previous development cycle the
state will appear in <span class="lstnew"> red </span> . Entries whose
state has gone unchanged through at least one full stable release cycle
will have their state displayed in " <span class="lststatus"> black
</span> ". Tag entries marked for deprecation will marked in " <span
class="lstdep"> red </span> " until they are removed from the PCGen Tag
Dictionary.

CSS styles used:\
 " <span class="lstnew"> New </span> " tag doc entry states marked in "
<span class="lstnew"> red </span> " use the **CSS** style "lstnew".\
 " <span class="lstupnew"> Updated </span> " tag doc entry states marked
in " <span class="lstupnew"> red </span> " use the **CSS** style
"lstupnew".\
 " <span class="lststatus"> New </span> " or " <span class="lststatus">
Updated </span> " tag doc entry states marked in " <span
class="lststatus"> black </span> " use the **CSS** style "lststatus".\
 " <span class="lstdep"> Deprecated </span> " tag doc entry states use
the **CSS** style "lstdep".

### Tag Name

The tag name is entered with the whole structure and syntax
demonstrated. The variables are indicated using the letter x, y and z.
You can use u, v, w and other letters if needed.

### Variables Used

All the variables that can be used are explained. Number variables can
be standard numbers or formulas or other variables if the tags accepts
them. Text variables accept text strings, names and other text forms.
Property variables indicate that the variable must be one of several
properties hardcoded into the program. These properties are usually
presented in a list following the variable.

### What it does

A complete explanation of the tag and its uses.

### Example

Examples of the tag in as many variations as needed to demonstrate the
variety of uses of the tag.

### Deprecated Syntax

Obsolete LST tag syntax is included here. When the deprecated syntax
represents a complete LST tag entry, a link to the deprecated listing is
provided. Were applicable, the version in which the syntax was
deprecated should be included as per the 'State of the Entry'
information listed above.

### Conversion Example

Obsolete LST tag conversion examples are included here. The form of the
example generally takes the form of:\
`old lst code` becomes `new lst code` .

### Where it is used

Some times it may be helpful to indicate exactly where the tag may be
used. Most times this is indicated by the page the entry is found on.

------------------------------------------------------------------------

LST Tag Documentation Style Guide
---------------------------------

The LST Tag Documentation Style Guide will be placed here.

------------------------------------------------------------------------



