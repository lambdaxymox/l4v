#
# Copyright 2020, Data61, CSIRO (ABN 41 687 119 230)
#
# SPDX-License-Identifier: GPL-2.0-only
#

# This Makefile is not meant to be invoked manually because it relies on
# files generated by a run of `isabelle build`.

LaTeX      = pdflatex -interaction=nonstopmode
BibTeX     = bibtex


all: pdf
pdf: root.pdf

root.pdf: root.tex Makefile
	@echo generating document
	${LaTeX} root; ${BibTeX} root; ${LaTeX} root; ${LaTeX} root; echo ""
	@echo generated/root.pdf

clean:
	rm -f *.aux *.toc *.bbl *.blg *.dvi *.log *.pstex* *.brf \
		*.out .log

realclean: clean
	rm -f root.pdf
