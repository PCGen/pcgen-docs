+++
date = "2016-08-01"
title = "PCGen Source Help"
original_url = "/source/index.html"

[menu.main]
    identifier = "source"
    name = "PCGen Source Help"
    weight = 70
+++
This section will provide information on how to use specific datasets.
It is not intended to detail every aspect of the dataset but is
specifically focused on features and aspects of the dataset which are
hidden, obscure, counter intuitive or simply unimplemented. When it is
not obvious how a particular feature from a source book is handled by
PCGen we will include that information here. If a feature can not
currently be supported in PCGen we will use this section to let you know
and include suggestions on how to work around the problem. For more
general instructions on how to use the program you should read the
[Character Creation Walkthrough](/walkthrough/walkthrough_index.html) section which
includes a step by step tutorial on how to create a character.

An example of a feature which would be included in this section is the
Arcane Archer. The Arcane Archer has the ability to enchant any
non-magical arrow he notches in his bow, this feature is not easily done
within PCGen data and there is no way to have it accounted for
automatically. The current solution is a special equipment modifier
created for this purpose. To use this feature you must customize a
non-magical arrow and add this equipment modifier to it, it costs
nothing and only grants bonuses to an Arcane Archer but when used by an
Arcane Archer the appropriate bonuses appear on the character sheets.
Because of the unusual (and some what obscure) way this feature is
implemented it is detailed here.

Another example is a class ability of the Archmage. As the Archmage
gains levels he is given the option to choose a spell he knows and
thereafter use it as a spell-like ability. PCGen at this time does not
have the capability to choose a spell from the characters spell list and
display it within the SA text. The suggested work around is to record
your spell choices in a note in the description tab.



