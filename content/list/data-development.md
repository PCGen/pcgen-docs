+++
date = "2016-08-01"
title = "New Source Development"
original_url = "/list/data-development.html"

[menu.main]
    identifier = "list_data-development"
    name = "New Source Development"
    parent = "list"
    
+++
This is the process for developing datasets for inclusion in PCGen.
Those familiar with how this process has worked in the past will note
that it is essentially unchanged with the exception that the point at
which a review of the source for OGL compliance and Publisher permission
needed before the source can be entered into the SVN repository is now
handled on an internal issue by the Publisher Liaison, Data License and
Content Silverbacks.

Initial Development
-------------------

It begins as always with our volunteers creating the datasets. The style
of this stage of development is entirely up the individual monkey who is
developing the set, they are free to upload the work to
pcgen\_experimental for review or not. Smaller sources being done by
individually monkeys should ideally be complete or near complete before
being submitted for entry into SVN. Larger projects, such as core
sources or SRD additions that are being developed by several monkeys
which could benefit from the cooperative nature of SVN do not have to be
complete but should be a good ways towards this point. It will be the
Lead Data Monkeys call when it should be submitted.

Resources
---------

The following resources are available to aid volunteers learn to create
LST files. The first place to go is the Documentation, which you are
reading now. There are a variety of pages dealing with LST files
designed to help get you up and running. For beginners we have a growing
section of lessons in the [LST file
Class](/list/lst-file-class/lst-file-class_index.html) . If you are creating datasets
for inclusion in PCGen you should pay close attention to the section on
[Official Release LST standards](/list/lst-standards.html) especially to
the section on [OGL Compliance](/list/lst-standards.html#ogl) . The docs
are also available
[online](http://pcgen.sourceforge.net/autobuilds/pcgen-docs/index.html)
on our [autobuild site](http://pcgen.sourceforge.net/autobuilds/) and
are updated periodically.

In addition to the main [PCGen Yahoo
group](http://groups.yahoo.com/group/pcgen/) we have several other lists
to aid in data development.
[pcgen\_experimental](http://groups.yahoo.com/group/pcgen_experimental/)
is used for development. You can get in touch with other data monkeys
here and upload your files for others to review. It is a good place to
coordinate activity if multiple monkeys are working on a source.
Additionally it is the place where new LST syntax and new tags are
developed.
[PCGenListFileHelp](http://groups.yahoo.com/group/PCGenListFileHelp/) is
the place to go for help with specific how-to problems with LST files.
[LSTFileClass](http://groups.yahoo.com/group/LSTfileclass/) is a group
set up to publish lessons on how to create LST files. The LST File
Classes here in the docs were originally published there.

Inclusion in SVN
----------------

When a source has been completed and is ready for inclusion in the
program it may be submitted in one of several ways. Data sets can be
uploaded to
[pcgen\_experimental](http://groups.yahoo.com/group/pcgen_experimental/)
to the appropriate folder and, along with a shout out to your friendly
neighborhood tracker monkey, they will be picked up for review. Once
submitted the data must pass an internal review before it can be
included in the SVN repository.

When a new source is submitted for inclusion in PCGen an internal issue
is opened for the Source. This is a special issue for tracking New
Source Development and will be the repository for all permission and OGL
status reports concerning the source. This issue will only contain
permission and OGL status reports, bug reports and the like will be
entered in separately in the regular issues. It will be closed when it
has passed all the required reviews and is checked in to the SVN
repository.

New submission issues will be opened by the Content Silverback or the
Chief Data Monkey. The dataset will be checked for obvious errors that
would prevent it from running in PCGen as well as for completeness.
Basically we are checking for show stoppers and not much more. If we
find a major problem we will contact the author to get it resolved.

If the dataset meets these minimum requirement it is zipped up and
attached to the issue. The issue is then reassigned to the Open Game
License (OGL) personnel. If problems are found the issue is reassigned
back to Data who will work to resolve the issue. Once resolved issue is
again reassigned to OGL.

When OGL passes the Source it is reassigned to Publisher Liaison (PL)
who will attach publisher permission to the issue, though the PL need
not wait for this step and may attach permissions at any time he
receives them.

When the source has passed OGL and PL the issue is reassigned to the
Lead Data Monkey who will SVN the dataset in the appropriate directory.
The issue is then closed.

Alpha Development
-----------------

At this point the dataset author will be invited to continue development
and be granted SVN access to continue work on the set. QA should be
informed that a new set is in SVN which needs to be reviewed. The
author, the QA team and the Tracker Monkey team will then work together
to bring the set up to release quality. Once the Dataset has been though
the QA process and all known issues have been resolved it is moved into
a permanent location in the data directory.



