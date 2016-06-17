# Academic Papers with Referencing

If, like me, you find yourself writing lots of academic papers, then your choice of writing and referencing tools are of primary importance. Below is a description of the tools and techniques that I use.

## Markdown with References

The method I am going to outline uses [Markdown](https://daringfireball.net/projects/markdown/), together with [BibTeX](http://www.bibtex.org/) formatted references, to produce beautiful LaTex inspired PDFs.

## Integrating Scrivener and Zotero

The most well-documented method of integrating Scrivener and Zotero uses [OpenOffice](https://www.openoffice.org/) or [LibreOffice](https://www.libreoffice.org/) and the _scannable cite_ option within Zotero - [here's one such example of doing it that way](http://thedigitalresearcher.com/how-to-use-zotero-with-scrivener/). 

## My Method

But my method does not depend on I use. If you're running on a Mac or Linux and you're comfortable using a command line, then you can try my method too. by the way, it probably works on Windows as well, but I don't work on such systems, so I cannot vouch for it. 

Furthermore, the result of my method is  And because our source documents are Markdown, the files I work with are basically text files, which makes them amenable to version control. And that makes them amenable to collaboration too.

For large papers, my writing tool of choice is [Scrivener](https://www.literatureandlatte.com/scrivener.php). I love the way it seemlessly breaks a document into smaller, more manageable, sections. I format my Scrivener documents as [Markdown](https://daringfireball.net/projects/markdown/). Markdown's minimalist style allows me to concentrate on content without worying too much about presentation - such separation of content from presentation is a fundamental principle of computing that Word Processing tools break. And for referencing, I use [Zotero](https://www.zotero.org/), [Firefox](https://www.mozilla.org/en-GB/firefox/new/) for searching for stuff, and its  


### Dependencies

Below is a list of dependencies:

1. A Markdown Editor. For large papers or novels (such as [My Abi](https://glowkeeper.gitbooks.io/my-abi/content/), I use [Scrivener](https://www.literatureandlatte.com/scrivener.php) because I love the way it allows me to break a document into smaller, more manageable, sections. However, to get Scrivener to output Markdown, you also need to install MultiMarkdown - [here are instructions for doing that](http://thaddeushunt.com/tips-setting-up-scrivener-to-compile-multimarkdown/). For shorter works, I use the fuss free [Sublime Text](https://www.sublimetext.com/) editor together with the [Markdown Editing](https://github.com/SublimeText-Markdown/MarkdownEditing) package. 
2. Install the swiss army knife of text formatting tools - [pandoc](http://pandoc.org/). Pandoc is a fabulous, if somewhat complex, tool. You can get it to produce just about anything - PDFs, Word documents, and it can even turn Markdown into beautiful [reveal.js](https://github.com/hakimel/reveal.js/) inspired presentations. I won't document such uses here, but you should be aware that Pandoc can do such things.
3. A LaTex processor. The [BasicTex](http://www.tug.org/mactex/morepackages.html) package will suffice. 
4. A reference manager that can output [BibTeX](http://www.bibtex.org/). I use [Zotero](https://www.zotero.org/) as my reference manager. It works best with [Firefox](https://www.mozilla.org/en-GB/firefox/new/) and Firefox's [Zotero plugin](https://download.zotero.org/extension/zotero-4.0.29.10.xpi). Additionally, I have installed Zotero's [Better BibText](https://github.com/retorquere/zotero-better-bibtex) plugin, primarily because that helps avoid citation key clashes. 

### Configuration

1. Setup Zotero so that the _Export_ _Default Output Format_ is _Better BibTex Quick Copy_ and make sure that Better BibTex's QuickCopy format is _Pandoc_. 
2. Make sure the command _pandoc_ is in your path.
3. Make sure that the LaTex commands are also in your $PATH; e.g. export PATH=$PATH:/usr/texbin.

## Workflow

Let's imagine you have to produce a paper for conference on renewable energy. Your paper is entitled **Only Oil Executives and Their Friends in Government Believe Fracking is a Good Energy Option**.  You want to open with great impact, and you find an article by [Bill McKibben](http://www.billmckibben.com/) in the [Rolling Stone](http://www.rollingstone.com/), which outlines the mathematical case for keeping fossil fuels in the ground. That's just the impact you were looking for, so you save that article to Zotero, and then open your paper with the following statement:

_Here's the terryfying truth: there are already enough known fossil fuel reserves to fry planet earth five times over._

Bang! Of course, you still need to include that Bill McKibben reference, so you head on over to Zotero, highlight the Rolling Stone article, hit cmd+shift+c (on a Mac) and then past that reference into your Markdown:

_Here's the terryfying truth: there are already enough known fossil fuel reserves to fry planet earth five times over @Bill_mckibben_2012._



    

