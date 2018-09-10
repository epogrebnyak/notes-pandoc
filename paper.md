---
author: Evgeny Pogrebnyak
title: Simple text to PDF workflow
date: September 2018
bibliography: bib1.yaml
---

Text-based command-line workflow for printable and publishable media (on Windows).
==================================================================================

Objectives
----------

- [ ] write text in a lightweight markup language
- [ ] produce PDF, html and other formats
- [ ] automate workflow using command line
- [ ] run on Windows
- [ ] cannot use online web-based services

Some examples of workflow
-------------------------

- <https://gist.github.com/maxogden/97190db73ac19fc6c1d9beee1a6e4fc8>
- <https://github.com/mschroen/Science.md>
- charts section below


Software
--------

#### Latex

Latex:

- describes content and layout for PDF files
- long-standing standard for scientific publishing
- aims to separate content from presentation
- can handle complex formulas and layouts
- gives stable output on different platforms
- has a process to include bibliograpy
- often a preferred format for journal submissions

Drawbacks:

- the price you pay is overhead: large installation pakages and document manipulations requires skill
- not too readable without prior knowledge, very hard to write from scratch  
- easier when working on an existing project or working in a template

Cutting edge:

- [online editors](https://blog.typeset.io/the-only-latex-editor-guide-youll-need-in-2018-e63868fae027)
  cut down installation burden and provide visual functionality
- ... yet you loose some of control over files
- alternative is git-based workflow to handle

Stories:

- [1](https://3d.bk.tudelft.nl/ken/en/2016/04/02/my-latex-thesis-workflow.html)
- [2](http://pierog.it/en/2018/03/markdown-workflow/)

#### pandoc and pandoc-citeproc

Render this paper to latex (prints to screen):

    pandoc --filter pandoc-citeproc -s paper.md -t latex


More at [this example](http://pandoc.org/demo/example19/Extension-citations.html)

#### Citation managers

**GUI**:

- JabRef
- Zotero (public funding), Mendeley (Elsevier), Paper (for Mac), EndNote (private, $249.95)
- Docear (Windows)

Functionality:

- GUI for citation database
- conversion of formats
- MS Word and browser integration

**Command line**:

- <https://github.com/papis/papis>
- <https://github.com/pubs/pubs>
- [bibtools](https://github.com/search?utf8=%E2%9C%93&q=bibtool) (little documentation) 

May have useful features, but...

- running a bit rough, little documentation
- failing on Windows
- hard to compete with big names

Common functions:

- init a local database
- add bibliographic entry
- list database
- export it to `.bib`

Important add-ons:

- query by doi
- use other online resources

Similar CLI work process for microlearning:

- <https://github.com/dnote/cli>

#### Gost citations

- <https://github.com/AndreyAkinshin/Russian-Phd-LaTeX-Dissertation-Template/blob/master/Readme/Bibliography.md>


#### CSL

- [CSL input schema](https://github.com/citation-style-language/schema/blob/master/csl-data.json)
- <http://editor.citationstyles.org/searchByName/>

Other links
---------

- <https://github.com/ihrke/markdown-paper>
- <https://github.com/ihrke/markdown-talk>
- <https://www.crossref.org/labs/citation-formatting-service>

Journals
--------

- <https://journals.plos.org/plosone>
- <https://arxiv.org>


Chart
-----
![md-pdf-workflow](https://kieranhealy.org/files/misc/workflow-rmd-md.png)
![md-pdf-workflow-2](https://ljvmiranda921.github.io/assets/png/tuts/workflow.png)


Example
=======

I would like to mention @lc03 in the text.

I would like a short mention of [@Allen2001gtd] in the text.

<!-- pandoc-citeproc will add references to end of file, so header is desirable
QUESTION: how do I control appearance of bibliography, CSL-?
-->
#### References