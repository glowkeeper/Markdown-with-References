# Scrivener (Markdown) and References

If you're like me, then you find yourself writing lots of academic papers. That means that it's important you use the most productive writing and referencing tools which work 

## A Brief Aside - Integrating Scrivener and Zotero

For large papers or novels (such as [My Abi](https://glowkeeper.gitbooks.io/my-abi/content/)), I use [Scrivener](https://www.literatureandlatte.com/scrivener.php) as my word processor together with [Zotero](https://www.zotero.org/) as my reference manager. The most well-documented method of integrating Scrivener and Zotero uses [OpenOffice](https://www.openoffice.org/) or [LibreOffice](https://www.libreoffice.org/) and the _scannable cite_ option within Zotero - [here's one such example of doing it that way](http://thedigitalresearcher.com/how-to-use-zotero-with-scrivener/). 

However, I prefer to avoid having to open an addional Word Processor package, so I use another method for integrating Scrivener and Zotero, which I outline below.

## My Method

My method does, however, have other dependencies, aside from a Word Processor package. Not least of which is being comfortable using a command line. Additionally, I have only used this method on a Mac. It will certainly work on Linux, and it probably works on Windows too, but I don't work on such systems, so I cannot vouch for them. 

### Method Overview

The method I am going to outline uses [Markdown](https://daringfireball.net/projects/markdown/), together with [BibTeX](http://www.bibtex.org/) formatted references, to produce beautiful LaTex inspired PDFs. I like Markdown's minimalist style because it allows me to concentrate on content without worying too much about presentation, at least while I'm busy writing.

Furthermore, because the source documents I create are text files, they are perfect for version control on [GitHub](https://github.com/). That also means they are amenable to collaboration through branching, diff'ing and merging.


### Dependencies

Below is a list of tools you'll need:

1. A Markdown Editor. [Scrivener](https://www.literatureandlatte.com/scrivener.php) is great for breaking big documents into smaller, more manageable, sections. I format my Scrivener documents as Markdown using the [MultiMarkdown](http://fletcherpenney.net/multimarkdown/) package - here are [instructions for setting that up](http://thaddeushunt.com/tips-setting-up-scrivener-to-compile-multimarkdown/). For shorter works, I use the fuss free [Sublime Text](https://www.sublimetext.com/) editor together with the [Markdown Editing](https://github.com/SublimeText-Markdown/MarkdownEditing) package. 
2. A reference manager that can output [BibTeX](http://www.bibtex.org/). I use [Zotero](https://www.zotero.org/). It works best with [Firefox](https://www.mozilla.org/en-GB/firefox/new/) and [Firefox's Zotero plugin](https://download.zotero.org/extension/zotero-4.0.29.10.xpi). Additionally, I use Zotero's [Better BibText](https://github.com/retorquere/zotero-better-bibtex) plugin, primarily because that helps avoid citation key clashes. 
3. Install the swiss army knife of text formatting tools - [Pandoc](http://pandoc.org/). Pandoc is a fabulous, if somewhat complex, tool. You can get it to produce just about anything - PDFs, Word documents, and it can even turn Markdown into beautiful [reveal.js](https://github.com/hakimel/reveal.js/) inspired presentations. I won't document such uses here, but if you want to do such things, here's a link to the [documentation](http://pandoc.org/README.html).
4. A [Citation Style Language](http://citationstyles.org/) file that matches the citation style you need. The [Zotero Style Repository](https://www.zotero.org/styles) has many such files. I have to prodce IEEE citations most often, so I use the file [IEEE with URL](https://www.zotero.org/styles/ieee-with-url).
5. A LaTex processor. The [BasicTex](http://www.tug.org/mactex/morepackages.html) package will suffice. 


### Configuration

1. Setup Zotero so that the _Export_ _Default Output Format_ is _Better BibTex Quick Copy_ and make sure that Better BibTex's QuickCopy format is _Pandoc_. 
2. Make sure the command _pandoc_ is in your path.
3. Make sure that the LaTex commands are also in your path; e.g. _export PATH=$PATH:/usr/texbin_.

### Workflow

Let's imagine you have to produce a paper for a conference on renewable energy. Your paper is entitled **Only Oil Executives and Their Friends in Government Believe Fracking is a Good Energy Option**.  You want to open your paper with great impact, and you find an article by [Bill McKibben](http://www.billmckibben.com/) in the [Rolling Stone](http://www.rollingstone.com/), which outlines the mathematical case for keeping fossil fuels in the ground. That's just the impact you were looking for, so you save that article to Zotero, and then open your paper with the following statement:

_Here's the terryfying truth: there are already enough known fossil fuel reserves to fry planet earth five times over._

Bang! Of course, you still need to include that Bill McKibben reference, so you head on over to Zotero, highlight the Rolling Stone article, hit _cmd+shift+c_ (on a Mac) and then past that reference into your Markdown:

_Here's the terryfying truth: there are already enough known fossil fuel reserves to fry planet earth five times over @Bill_mckibben_2012._

    

