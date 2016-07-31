+++
date = "2016-08-01"
title = "Index : FreeMarker Output Support"
original_url = "/freemarker/index.html"

[menu.main]
    identifier = "freemarker_index"
    name = "Index : FreeMarker Output Support"
    parent = "freemarker"
        weight = -1
+++
Starting from version 6.03.00, PCGen has introduced support for the
[FreeMarker](http://freemarker.org/) template engine. FreeMarker is a
tool to allow the generation of text files based on templates.

FreeMarker brings a powerful, rich language for the creation of output
sheets to PCGen. It has far greater capabilities than were provided by
PCGen's venerable output sheet language. These include the ability to
define macros and methods to include repeated content as well as
understandable looping and logic commands.

The initial implementation of FreeMarker for PCGen provides all of the
capabilities of the old output sheet system with a series of functions
to access the old output sheet tokens. In the future we will also
provide an object based means of interacting with a character being
output. This will allow more flexible and data driven output.

------------------------------------------------------------------------



