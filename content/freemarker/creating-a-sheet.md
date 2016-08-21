+++
date = "2016-08-01"
title = "Creating a FreeMarker Output Sheet"
original_url = "/freemarker/creating-a-sheet.html"

[menu.main]
    identifier = "freemarker_creating-a-sheet"
    name = "Creating a FreeMarker Output Sheet"
    parent = "freemarker"
    
+++
FreeMarker sheets are detected by PCGen by their file name suffix. A
template ending in **.ftl** will be processed by FreeMarker rather than
by PCGen's legacy output engine.

The extension of the file to be produced should be immediately before
that and preceded by a . or -. So a template to produce html output
might be named csheet-first.html.ftl or chseet-compact-html.ftl and
PCGen would pick up that it was a template to be processed by FreeMarker
template that would produce output of a html file.

Inside the sheet, the file is just a text file, with functions or
directives included when needed to produce dynamic output. It is often
simplest to start with a static file that looks like the output you want
and then gradually introduce FreeMarker tags to make the sheet show the
character info.

### FreeMarker Documentation

FreeMarker has quite thorough documentation. The main references output
sheet authors will use are:

1.  [Template Author's Guide](http://freemarker.org/docs/dgui.html)
2.  [Reference Guide](http://freemarker.org/docs/ref.html)
3.  [Main FreeMarker page](http://freemarker.org/)

In addition, see testsuite/base-xml.ftl for a fully worked example of
xml output.

### Conversion from Legacy Output Engine

A Groovy script is available to convert a legacy PCGen sheet to
FreeMarker. Get the script from
[GitHub](https://raw.githubusercontent.com/PCGen/pcgen/master/code/convfreemarker.groovy)
. You will also need to [download Groovy](http://groovy.codehaus.org/) .

The script is run using the command

    groovy convfreemarker.groovy sheetname [outputtemplatename]

where *sheetname* is the path to the sheet you wish to convert and
*outputtemplatename* is the nameof the FreeMarker template file to be
created. If an outputtemplatename is not supplied, the output template
will be the same name as the sheetname but with .ftl appended to it.
e.g. groovy convfreemarker.groovy base.xml would produce base.xml.ftl

The following are the main steps that need to be made for manual
conversion:

1.  Replace FOR loops with @loop directives. e.g.
    |FOR,%class,0,COUNT\[CLASSES\]-1,1,0| becomes &lt;@loop from=0
    to=pcvar('count("CLASSES")')-1 ; class , class\_has\_next &gt;
2.  Replace IF tests with FreeMarker if tests. This will often need the
    use of pcvar and pcboolean functions to access
    character information.
3.  Replace filters with FreeMarker if tests.
4.  Replace each old tag with a call to pcstring. e.g. |PLAYERNAME|
    becomes \${pcstring('PLAYERNAME')}
5.  Replace loop variables in tags with variable references. e.g.
    |CLASSABB.%class| becomes \${pcstring('CLASSABB.\${class}')}

Manual tidy up will then be required including extracting repeated
content to macros.

------------------------------------------------------------------------



