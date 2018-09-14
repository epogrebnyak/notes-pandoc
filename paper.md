---
author: Evgeny Pogrebnyak
title: Simple text to PDF workflow
date: September 2018
bibliography: bib1.yaml
---

Text-based command-line workflow for printable and publishable research delievery (yes, on Windows).
====================================================================================================

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

- <https://github.com/nteract/nteract>
- <https://joshldavis.com/2014/02/12/doing-your-homework-in-latex/>
- <https://github.com/ihrke/markdown-paper>
- <https://github.com/ihrke/markdown-talk>
- <https://www.crossref.org/labs/citation-formatting-service>
- <https://content.iospress.com/articles/information-services-and-use/isu862>

Formulas:
- Supplement: mathjax, katex and [annotated formulas](https://github.com/distillpub/template/wiki/Annotated-Formulas)


Review and practices:
- <http://facweb.cs.depaul.edu/mobasher/classes/CSC426/>
- <https://www.soas.ac.uk/cedep-demos/000_P506_RM_3736-Demo/unit1/index.htm>

Peer-review bias:
- https://pdfs.semanticscholar.org/62c2/a36763d95fdf38bdc4a5358985f1030e6c21.pdf
- https://www.vox.com/2015/12/7/9865086/peer-review-science-problems
- http://journals.sagepub.com/doi/pdf/10.1177/1367493517727320


Writing:
- http://web.mit.edu/me-ugoffice/communication/technical-writing.pdf
- https://shd101wyy.github.io/markdown-preview-enhanced/#/math

Reproducibility: 

- <https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.2005468>
- <http://blogs.discovermagazine.com/neuroskeptic/2018/01/02/is-reproducibility-central-science>
- <https://www.nature.com/articles/d41586-018-06008-w>
- <https://www.coursera.org/learn/reproducible-research#syllabus>
- <https://www.tse-fr.eu/publications/how-make-pie-reproducible-research-empirical-economics-econometrics>
- <https://academia.stackexchange.com/questions/14010/how-do-you-cite-a-github-repository>

Search based on title:

- http://conference.scipy.org/proceedings/scipy2018/pdfs/proceedings.pdf
- http://www7.inra.fr/mia/T/cros/Interests.html
- http://ropensci.github.io/reproducibility-guide/sections/introduction/
- https://arxiv.org/pdf/1503.02388.pdf


Replication economics NBER:

- http://www.nber.org/papers/w13026
- http://www.nber.org/papers/w15794
- 

Journals
--------

- <https://journals.plos.org/plosone>
- <https://arxiv.org>


Chart
-----
![md-pdf-workflow](https://kieranhealy.org/files/misc/workflow-rmd-md.png)
![md-pdf-workflow-2](https://ljvmiranda921.github.io/assets/png/tuts/workflow.png)
![md-pdf-workflow-2](https://4bds6hergc-flywheel.netdna-ssl.com/wp-content/uploads/2017/09//troff-latex-html-asciidoc-compare-source-code.png)


Takeaways
=========

```

domain,                                research finding             contribution
idea,
problem                                service/product              utility

                                                                    clarity

              theory

              data, evidence

              methods, code

              previous findings


                              images

                              tables

                              text

                                       book

                                       report
                    
                                       research article              readers

                                       commentary

                                       documentation                 users

                                       service, product
```


Choice of reporting format depends on:
  - ratios of code/images to prose
  - layout complexity
  - maths 
  - end user expectations about delievery (time to market, reproducible)

Names:
- learning `markdown` is highly recommended
- `jupiter` notebooks are here to stay (enhance your experience with `nbconvert`)
- learn `pandoc` to see how you can convert between different formats quickly
- invest in `latex`, if you will have to work with them in your domain field

Example
=======

I would like to mention @lc03 in the text.

I would like a short mention of [@Allen2001gtd] in the text.

<!-- pandoc-citeproc will add references to end of file, so header is desirable
QUESTION: how do I control appearance of bibliography, CSL-?
-->
#### References