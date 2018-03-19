AsciiDoc dblatex README
=======================

Customization
-------------
The `./dblatex` directory contains:

`./dblatex/asciidoc-dblatex.xsl`:: Optional dblatex XSL parameter
customization.

`./dblatex/asciidoc-dblatex.sty`:: Optional customized LaTeX styles.

Use these files with dblatex(1) `-p` and `-s` options, for example:

  dblatex -p ../dblatex/asciidoc-dblatex.xsl \
          -s ../dblatex/asciidoc-dblatex.sty article.xml


Limitations
-----------
Observed in dblatex 0.2.8.

- Callouts do not work inside DocBook 'literallayout' elements which
  means callouts are not displayed inside AsciiDoc literal blocks.  A
  workaround is to change the AsciiDoc literal block to a listing
  block.
