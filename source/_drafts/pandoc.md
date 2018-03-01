categories: markdown
tags: pandoc
title: pandoc
date: 2017/02/13 20:46:25
---

a universal document converter

## About pandoc

Pandoc is free software, released under the GPL. © 2006-2016 John MacFarlane.

<!--more-->

If you need to convert files from one markup format into another, pandoc is your swiss-army knife. Pandoc can convert documents in markdown, reStructuredText, textile, HTML, DocBook, LaTeX, MediaWiki markup, TWiki markup, OPML, Emacs Org-Mode, Txt2Tags, Microsoft Word docx, LibreOffice ODT, EPUB, or Haddock markup to

- HTML formats: XHTML, HTML5, and HTML slide shows using Slidy, reveal.js, Slideous, S5, or DZSlides.
- Word processor formats: Microsoft Word docx, OpenOffice/LibreOffice ODT, OpenDocument XML
- Ebooks: EPUB version 2 or 3, FictionBook2
- Documentation formats: DocBook, TEI Simple, GNU TexInfo, Groff man pages, Haddock markup
- Page layout formats: InDesign ICML
- Outline formats: OPML
- TeX formats: LaTeX, ConTeXt, LaTeX Beamer slides
- PDF via LaTeX
- Lightweight markup formats: Markdown (including CommonMark), reStructuredText, AsciiDoc, MediaWiki markup, DokuWiki markup, Emacs Org-Mode, Textile
- Custom formats: custom writers can be written in lua.

! [](https://pandoc.org/diagram.jpg)

## Installing pandoc

### Windows
- There is a package installer at pandoc’s [download page](https://github.com/jgm/pandoc/releases/tag/1.19.1).

## Demos

### Try pandoc online
- You can try pandoc online [here](http://pandoc.org/try/).


### Examples

- HTML fragment:

> pandoc MANUAL.txt -o example1.html

- Standalone HTML file:

> pandoc -s MANUAL.txt -o example2.html

- HTML with smart quotes, table of contents, CSS, and custom footer:

> pandoc -s -S --toc -c pandoc.css -A footer.html MANUAL.txt -o example3.html

- LaTeX:

> pandoc -s MANUAL.txt -o example4.tex

- From LaTeX to markdown:

> pandoc -s example4.tex -o example5.text

- reStructuredText:

> pandoc -s -t rst --toc MANUAL.txt -o example6.text

- Rich text format (RTF):

> pandoc -s MANUAL.txt -o example7.rtf

- Beamer slide show:

> pandoc -t beamer SLIDES -o example8.pdf

- DocBook XML:

> pandoc -s -S -t docbook MANUAL.txt -o example9.db

- Man page:

> pandoc -s -t man pandoc.1.md -o example10.1

- ConTeXt:

> pandoc -s -t context MANUAL.txt -o example11.tex

- Converting a web page to markdown:

> pandoc -s -r html http://www.gnu.org/software/make/ -o example12.text

- From markdown to PDF:

> pandoc MANUAL.txt --latex-engine=xelatex -o example13.pdf

- PDF with numbered sections and a custom LaTeX header:

> pandoc -N --template=mytemplate.tex --variable mainfont="Palatino" --variable sansfont="Helvetica" --variable monofont="Menlo" --variable fontsize=12pt --variable version=1.17.2 MANUAL.txt --latex-engine=xelatex --toc -o example14.pdf

- A wiki program using Happstack and pandoc: gitit

- HTML slide shows:

> pandoc -s --mathml -i -t dzslides SLIDES -o example16a.html

> pandoc -s --webtex -i -t slidy SLIDES -o example16b.html

> pandoc -s --mathjax -i -t revealjs SLIDES -o example16d.html

- TeX math in HTML:

> pandoc math.text -s -o mathDefault.html

> pandoc math.text -s --mathml -o mathMathML.html

> pandoc math.text -s --webtex -o mathWebTeX.html

> pandoc math.text -s --mathjax -o mathMathJax.html

> pandoc math.text -s --latexmathml -o mathLaTeXMathML.html

- Syntax highlighting of delimited code blocks:

> pandoc code.text -s --highlight-style pygments -o example18a.html

> pandoc code.text -s --highlight-style kate -o example18b.html

> pandoc code.text -s --highlight-style monochrome -o example18c.html

> pandoc code.text -s --highlight-style espresso -o example18d.html

> pandoc code.text -s --highlight-style haddock -o example18e.html

> pandoc code.text -s --highlight-style tango -o example18f.html

> pandoc code.text -s --highlight-style zenburn -o example18g.html

- GNU Texinfo, converted to info, HTML, and PDF formats:

> pandoc MANUAL.txt -s -o example19.texi

> makeinfo --no-validate --force example19.texi -o example19.info

> makeinfo --no-validate --force example19.texi --html -o example19

> texi2pdf example19.texi  # produces example19.pdf

- OpenDocument XML:

> pandoc MANUAL.txt -s -t opendocument -o example20.xml

- ODT (OpenDocument Text, readable by OpenOffice):

> pandoc MANUAL.txt -o example21.odt

- MediaWiki markup:

> pandoc -s -S -t mediawiki --toc MANUAL.txt -o example22.wiki

- EPUB ebook:

> pandoc -S MANUAL.txt -o MANUAL.epub

- Markdown citations:

> pandoc -s -S --bibliography biblio.bib --filter pandoc-citeproc CITATIONS -o example24a.html

> pandoc -s -S --bibliography biblio.json --filter pandoc-citeproc --csl chicago-fullnote-bibliography.csl CITATIONS -o example24b.html

> pandoc -s -S --bibliography biblio.yaml --filter pandoc-citeproc --csl ieee.csl CITATIONS -t man -o example24c.1

- Textile writer:

> pandoc -s -S MANUAL.txt -t textile -o example25.textile

- Textile reader:

> pandoc -s -S example25.textile -f textile -t html -o example26.html

- Org-mode:

> pandoc -s -S MANUAL.txt -o example27.org

- AsciiDoc:

> pandoc -s -S MANUAL.txt -t asciidoc -o example28.txt

- Word docx:

> pandoc -s -S MANUAL.txt -o example29.docx

- LaTeX math to docx:

> pandoc -s math.tex -o example30.docx

- DocBook to markdown:

> pandoc -f docbook -t markdown -s howto.xml -o example31.text

- MediaWiki to html5:

> pandoc -f mediawiki -t html5 -s haskell.wiki -o example32.html

- Custom writer:

> pandoc -t sample.lua example33.text -o example33.html

- Docx with a reference docx:

> pandoc -S --reference-docx twocolumns.docx -o UsersGuide.docx MANUAL.txt

- Docx to markdown, including math:

> pandoc -s example30.docx -t markdown -o example35.md

- EPUB to plain text:

> pandoc MANUAL.epub -t plain -o example36.text

