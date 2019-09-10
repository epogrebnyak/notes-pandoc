---
author: Evgeny Pogrebnyak
title: Simple text to PDF workflow
date: September 2018
bibliography: bib1.yaml
---


Text-based command-line research workflow 
=========================================

Actors:
-------

- source in markup language
  - markdown  
  - rst
  - bookdown
  
- static site or documentation generator 
   
- creating PDF


Tools:
-----

- [jupyter-book](https://jupyter.org/jupyter-book/intro.html)
- bookdown
- asciidoctor
- static site documentation themes
- sphinx, mcdocs

To PDF
------

- weasyprint
- wkhtml
- athena-pdf
- reportlab

Features
--------

- write text in a lightweight markup language
- produce PDF, HTML and other report
- automate workflow using command line



Takeaways
=========

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
 