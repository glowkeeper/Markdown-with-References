If, like me, you find yourself writing large academic papers, then your choice of writing tool and methods of integrating references are of primary importance. For large papers, my tool of choice is [Scrivener](https://www.literatureandlatte.com/scrivener.php); I love the way it seemlessly breaks a document into smaller, more manageable, sections. And for referencing, I use [Zotero](https://www.zotero.org/) and it's fantastic [Firefox](https://www.mozilla.org/en-GB/firefox/new/) plugin. The problem was then how to integrate the two. 

The most well-documented method of integrating Scrivener and Zotero involves using [OpenOffice](https://www.openoffice.org/) or [LibreOffice](https://www.libreoffice.org/) and the scannable cite option from within Zotero - [Here's one such example](http://thedigitalresearcher.com/how-to-use-zotero-with-scrivener/). 

That's a worthy method, but if you're running MAC OS X or Linux (this method probably works on Windows too, but I don't work on such systems, so I cannot verify it) and you're comfortable using a command line, then there is an alternative. 

And the result of that alternative will be a beautiful PDF from what is, essentially, a text file. And because we're working with text files, the documents you produce are amenable to version control. And that makes them amenable to collaboration too.

## Dependencies

1. [pandoc](http://pandoc.org/).
2. A LaTex processor. The [BasicTex](http://www.tug.org/mactex/morepackages.html) package will suffice.
3. Check that the LaTex commands are in your $PATH; e.g export PATH=$PATH:/usr/texbin.

## Optional


