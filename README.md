[![Actions Status](https://github.com/tbrowder/PDF-Labelmaker/workflows/test/badge.svg)](https://github.com/tbrowder/PDF-Labelmaker/actions)

NAME
====

PDF::Labelmaker - Provides a tool to print one or more labels on a standard sheet of stick-on labels

**THIS IS A WORK IN PROGRESS AND IS CURRENTLY NOT USABLE**

**Continued work will depend on user interest as shown by issues filed or comments on IRC #raku.**

SYNOPSIS
========

```raku
use PDF::Labelmaker;
$ make-labels ignore-colrows=1:1-3;2:3-4 <list-file>
See output file '<list-file>-labels.pdf'.
```

DESCRIPTION
===========

`PDF::Labelmaker` is the module which provides the Raku binary program `make-labels` to create one or more labels to print on a standard sheet of labels.

Currently the only standard sheet supported is ... but more sheets can be supported as interest occurs.

A user config file, in TOML format, will be supported to enable easy user customization.

The format for the input file will be a text file with each line as the source for a line on a label, with each label ended by a blank line or the end of the file. Comments, beginning with a '%' character, are ignored as are all following characters to the end of that line.

Another comment character can be chosen in the user's configuration file or on the command line.

BACKGROUND
==========

The existing label maker program, in its current state on the author's local host, has been used to generate mailing labels Christmas cards for over 20 years, and the labels have been seen by Raku experts @lizmat and @jmerelo.

That program creates the labels as a PostScript file which is then converted to PDF. The planned version for this module will create the output file in PDF only by using David Warring's `PDF::Lite` module.

AUTHOR
======

Tom Browder <tbrowder@cpan.org>

COPYRIGHT AND LICENSE
=====================

Copyright © 2021 Tom Browder

This library is free software; you can redistribute it or modify it under the Artistic License 2.0.

