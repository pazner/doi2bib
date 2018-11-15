# `doi2bib`: obtain BibTeX database entries given DOIs

## Usage

`doi2bib doi1 [doi2...]`

## Details

The DOIs can optionally be prefixed by `https://doi.org/` to allow for easy copy-and-paste
from websites. DOIs may need to be quoted at the command line if they contain certain 
characters.

The script makes use of the [Crossref API](http://api.crossref.org) to retrieve the 
bibliography entries. Minor post-processing is performed: the underscore in between the 
author and the year is removed from the cite-key, and the braces around the month field 
are removed for better compatibility with [BibLaTeX](https://ctan.org/pkg/biblatex).

To directly place the resulting database entry in the Mac OS X clipboard, you can use:

`copydoi doi1 [doi2...]`

This script can trivially be altered to work on Linux.