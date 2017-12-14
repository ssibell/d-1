---
layout: post
title:  "dCache Book Compiling Instructions!"
date:   2017-03-03 10:27:23
author: Mathias de Riese
excerpt: This is a test website for dCache.org. You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. 
category: posts
---

## Introduction
------------

The dCache Book is based on the DocBook/XML vocabulary and Norman
Walsh's XSLT Stylesheets.  For some output, the stylesheets transform
the source XML files either directly to the final format (HTML,
Man-pages).  The PDF output uses an intermediate format (XSLT-FO) and
the text output is generated from the single-page HTML.

XSLT-FO (.fo) files are still XML, but more closely represent the
final output.  Software is needed to convert the XSLT-FO files into
the final output (e.g., PDF, PostScript).  Amongst other things, this
software does the text-layout, pagination, laying out tables, etc.
The recommended software is fop, from the Apache foundation.

To generate the text output, the single-page HTML file is converted to
text.  There is no support for converting DocBook directly to text and
support for converting XSLT-FO files to text (using fop) is currently
not very good.

FOP can use LaTeX-derived hyphenation patterns to break words at the
end-of-line.  However, due to a licensing issue wrangle, these rules
are not include with FOP.  Instead, the rules are available from the
Objects For Formatting Objects (OFFO) SourceForge project.  A single
.jar file must be installed for hyphenation to work; this
straight-forward process is described below.


### What you will need:

To build the dCache Book you will need:
1.  a copy of the DocBook stylesheets (a set of XSLT files)
2.  an XSLT processor (xsltproc is used in the Makefile)
3.  an XSLT-FO processor (the latest version of fop should be used.)
4.  a text-based web-browser: any of (w3m, links, lynx) should work.
    w3m is the default.

You are recommended to get:
1.  the hyphenation rules.


Currently, you must install these packages manually.  The previous
system (that downloaded and installed the XSLT files, a version of
fop, etc) is not supported.  Hopefully we can document this process so
it's easy.



### Where to get things

Many distributions package the bare essentials.  Some caveats: make
sure the version of FOP is fairly recent: 0.9x is a requirement.  For
DocBook, make sure you get DocBookXML support (i.e., the stylesheets).
DocBook is (or "used to") come with SGML support, but we're using pure
XML so the SGML version of DocBook is of no use.

*   SF download page for [DocBook
    XSLT](http://sourceforge.net/project/showfiles.php?group_id=21935).
    You want "docbook-xsl" package.

*   FOP [download mirror
    selection](http://www.apache.org/dyn/closer.cgi/xmlgraphics/fop);
    downloadt latest version:

*   Download page for OFFO hyphenation rules.  You will want the
    [offo-hyphenation-fop-stable.zip](http://sourceforge.net/project/showfiles.php?group_id=116740)
    file:

*   Download page for the [w3m text-mode web
    browser](http://sourceforge.net/project/showfiles.php?group_id=39518)

### Installing the hyphenation rules

Here's a step-by-step method of installing the fop hyphenation rules
for all users (requires root access).

    unzip offo-hyphenation-fop-stable.zip
    sudo mkdir -p /usr/local/share/java
    sudo cp offo-hyphenation-fop-stable/fop-hyph.jar /usr/local/share/java
    cat > /etc/fop.conf << EOF
    FOP_HYPHENATION_PATH=/usr/local/share/java/fop-hyph.jar
    EOF

A guide to installing the hyphenation rules as a normal user:

    unzip offo-hyphenation-fop-stable.zip
    mkdir -p ~/local/share/java
    cp offo-hyphenation-fop-stable/fop-hyph.jar ~/local/share/java
    cat > ~/.foprc << EOF
    FOP_HYPHENATION_PATH=$HOME/local/share/java/fop-hyph.jar
    EOF

**N.B.** we assume that `$HOME` is expanded to your home directory by
the shell; if this doesn't happen, it should happen within the fop
wrapper shell.  If it doesn't happen in either place, you're very
unlucky and must substitute the value in ~/.foprc yourself.


### Using the Makefile rules

Do `make` (equiv. to `make info`) to see a summary of what targets are
available.  Here are a few useful options:

<dl>
<dt>make all</dt>
<dd>builds everything,</dd>
<dt>make pdf</dt>
<dd>builds all PDF,</dd>
<dt>make html</dt>
<dd>builds all HTML output,</dd>
<dt>make test-deploy</dt>
<dd>builds and deploys on the web-server at the test location,</dd>
<dt>make deploy</dt>
<dd>builds and deploys on the web-server at the live location,</dd>
<dt>make clean</dt>
<dd>remove backup files,</dd>
<dt>make distclean</dt>
<dd>remove all generated files.</dd>
</dl>

The HTML output has `.shtml` and contains the server-side includes
needed for integration within `www.dcache.org`.  However, the HTML
should be valid, so you can view the web-pages without having to
deploying them.

Deploying to the webserver will try to copy the files using `scp`.  If
you account on www.dcache.org is not the same as your local account,
use your ~/.ssh/config file to specify this.  For example:

    Host www.dcache.org
      User fred


### Some notes on XML catalogues

XML Catalogs are how a global reference (e.g.,
`http://docbook.sourceforge.net/release/xsl/current/fo/docbook.xsl`)
is redirected to a local file.

If you want an easy life, use an RPM installation.  If the stylesheets
have been properly packages, they will register themselves with the
machine's global catalogue (which usually starts at
`/etc/xml/catalog`) and the Makefile will just work.

If you do not (or cannot) install the catalogues, the next best option
is the provide your own (private) XML catalog, which includes your
locally-installed DocBook stylesheets.  This allows you to process the
dCache book (and generating output) without editing the location of
DocBook stylesheets within the dCache book.

The `XML_CATALOG_FILES` environment variable controls this behaviour:

    export XML_CATALOG_FILES=/some/suitable/catalog

For example, on Solaris with docbook-xsl installed under the
`/usr/local/share` directory.

    XML_CATALOG_FILES=/usr/local/share/docbook-xsl-1.68.1/catalog.xml
    export XML_CATALOG_FILES

TODO: a quick how-to on writing your own catalog files.  In the
mean-time, just Google and/or read the spec.
