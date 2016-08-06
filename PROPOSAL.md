PCGen Documentation 2.0
=======================

Hi all;

I have been working on converting the PCGen documentation into a new system.

* Convert documentation from HTML (hard to edit) into Markdown (easy to edit)
* Use [Hugo](http://gohugo.io), the static site generator, to compile
  the Markdown into a static site.
  
I have a working proof of concept which shows the benefits. I am now seeking
comments and assistance to get this into production.

Below:
* Technical benefits
* Benefits to the project
* Proof of concept (includes download links)
* Technical Aspects
* Where to now?
* Where can I discuss this?

Below I talk about the benefits of this approach - both technical benefits
and benefits to the project. I have a working proof of concept you
can download from my Github. You can look at the Markdown source,
use Hugo to compile it, and look at the compiled HTML output.

I also talk about the work still remaining - mainly integration with
the existing PCGen build processes. There's also a bit of manual editing
needed to complete the automated conversion, which was mostly done using
single-use text processing scripts.

Technical Benefits
==================

 1. The old HTML documentation is hard to edit. (I should know: I just
    spent ~40 hours editing it.)
 
    Markdown is **very easy to read** and **very easy to edit**. You can learn
    Markdown in about 10 minutes: see http://commonmark.org/help/. Also see the
    [source code for this document](https://raw.githubusercontent.com/LiaungYip/pcgen-docs/master/PROPOSAL.md)
    as an example.
    
    Markdown is also used by people on some of the world's most popular
    websites.
    
    * Reddit posts and comments are written in Markdown.
    * Stack Overflow questions and answers are written in Markdown.
    * The [Discourse](http://discourse.org) forum software, which is being
      rapidly adopted in place of phpBB, vBulletin, etc. uses Markdown
      for all posts.
    * Github issues, comments, README files, etc. are in Markdown.
    
    So Markdown is much easier to write than HTML, and a lot of people
    already know how to write it. This lowers the bar to participation.

 2. The old HTML documentation relies on hand-coded menus and indexes for
    navigation.
 
    The new Markdown + Hugo system automatically generates indexes, so the
    indexes are always accurate, and free of broken links.

 3. We are using a (modified version of) a very pretty off-the-shelf web
    template. Appearance-wise, this is miles ahead of the old documentation.
    
    Aesthetics aren't the top priority - the content is more important, 
    of course.
    
    However, attractive documentation gives users a good impression!
    
 4. The generated site is plain HTML. No server-side application is required.
    No databases are required.

    No PHP, no Python/Django, no Rails/Ruby On Rails, etc.
    
    No MySQL, no PostgreSQL, etc.
 
    We get all the benefits of a modern website, **without exposing any
    security attack surfaces.**
    
    Hugo websites don't need security updates, database administration, etc.
    
 5. I have broken the existing documentation pages (some of them over
    100 kB long) into much smaller pages.
    
    This makes the documentation much easier to edit - particularly for new
    contributors.
    
Benefits to the Project
=======================

 1. Lots more people can contribute to the documentation, because it's much
    easier than before.
    
    In help threads, it's possible to ask users to help write documentation,
    like this:
    
    > Hi, Bob!
    >
    > I'm glad we were able to solve your problem.
    >
    > Can you write up a summary of how we solved it?
    >
    > We have a plain-text file template you can use.
    >
    > We'll post it on the main documentation site to help others in the
    > future.
    >
    > Thanks!"
    
    Every user we help, has a chance to contribute to the permanent
    documentation of the project - i.e. tutorials and guides - freeing up
    resources for other tasks.
    
    BONUS: If the existing phpBB forums and Yahoo! mailing lists are migrated
    to the next-generation Discourse forum software - all Discourse posts are
    written in Markdown. So good information can be copy-pasted directly from
    a Discourse forum into the formal documentation!
    
 2. It's easy to review changes to the Markdown documentation.
 
    When the HTML documentation changes, a lot of HTML markup changes, which
    makes it hard to look at the git diffs/commits and proofread them.
    
    In markdown, the diffs are very easy to read. So it's much easier to
    spot spelling / grammar errors, broken links, and the like, before
    they get committed.
    
 3. Hugo websites don't need any server-side software or database. There's
    pretty much nothing to break. So the sys-admin overhead is very low.
    
 4. The new documentation format gives a good foundation for updating the
    older (more obsolete) parts of the documentation. The effort required
    will be greatly reduced.
    
 5. Currently, some documentation is on the PCGen Wiki (because that was
    easier to edit.) This documentation didn't make it into the HTML docs,
    because the HTML is hard to edit.
    
    Once the documentation is in Markdown, it becomes easy to write documentation
    into the Markdown docs, directly. So the documentation can be written once,
    saving effort.
    
Proof of concept
================

* I have converted the existing HTML documentation into Markdown.

    * The conversion scripts are on my GitHub - very hacky. But they only need
      to be used once, so the hacky-ness is fine.
      
* I can use Hugo to compile it into HTML suitable for distribution.

* I have spent some time refining the navigation experience - particularly
  the navigation menus, and the automatically-generated indexes of the
  list file tags (alphabetical, and categorised by the list file they are used in.)
  
* HOWEVER. The conversion was automated. This means:

    * Any typographical errors, weird formatting, strange grammar, etc. will
      be faithfully reproduced in the new documentation.
      
    * Pages were broken up into sub-pages. So there will be headings with
      no content underneath them, the content having being moved to a new page.
      There will also be text like "See above for details..." which will
      refer to text that has moved.
      
      These kinds of issues will require some manual editing to resolve.
      
    * The automatic conversion leaves a few rough edges. Some duplicate
      headers, some extra `<hr>` horizontal rules, etc. Again, this
      will require some manual editing.
    
Technical aspects
=================

 1. The Markdown source files compile into HTML. That HTML can be served from
     the internet (just like now), and also distributed with every copy of
     PCGen (again, just like now.)

 2. The compiled HTML is large (~80 MB.) This compresses to ~1 MB. So there is
    no impact on the size of the distribution. There is an increase on the disk
    space used for installation.
    
 3. It takes about 20 seconds to compile the site, on my PC. This is actually
    quite a long time for Hugo.
    
    RAM usage is a reasonable 60 MB (peak). Evidently Hugo is quite good at
    keeping the RAM usage down during compilation.
    
Where to, now?
==============

Firstly, the new Markdown + Hugo compiler needs to be incorporated into
the PCGen build process. A copy of the compiled HTML should ship with
every copy of PCGen.


Secondly, the website needs to be set up on a public website. Similar
to the existing http://pcgen.org/autobuilds/pcgen-docs/ . This is
easy to do using git hooks and a cron job (I deploy a Hugo website this
way already - penwatch.net/ingress_guide.)

I would suggest http://docs.pcgen.org/.


Thirdly, some effort will be required to clean up after the automated conversion.
Resolving the formatting glitches, etc. discussed above.

Where can I check this out?
===========================

See http://github.com/LiaungYip/pcgen-docs .

You can download a copy of the documentation source, use Hugo to
compile it, and see the compiled HTML website.

You can also look at the raw Markdown source, and see how easy it
is to edit.

I've also prepared a ready-made zip of the compiled HTML, for those
who don't have time to install Hugo. See:

* [7zip format - 13,948 kB](http://www.penwatch.net/files/pcgen-docs/pcgen-docs-compiled.7z)
* [zip format - 25,104 kB](http://www.penwatch.net/files/pcgen-docs/pcgen-docs-compiled.zip)
* [7zip format - no images - 818 kB](http://www.penwatch.net/files/pcgen-docs/pcgen-docs-compiled-no-images.7z)
* [zip format - no images - 10,708 kB](http://www.penwatch.net/files/pcgen-docs/pcgen-docs-compiled-no-images.zip)


Where can I discuss this?
=========================

Reply email to the _exp list is fine.

I'm also holding court in the "Documentation Process" room on Hipchat
(which is my preferred method of communication.)

----

I hope you're all as enthusiastic about this as I am.

I've long thought that PCGen's documentation is a clear area for
improvement, and I'm happy to be contributing to the project!

Regards, Lewis.

