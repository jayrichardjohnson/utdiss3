# Makefile for compiling UT disseration in Latex using pdflatex and biblatex
#   22 Feb 2019 - Jay Johnson

all: diss clean

log: diss neat 

full: diss

reportfile=report

files = ${reportfile}.tex

diss:
		pdflatex ${reportfile}
		biblatex ${reportfile}||true
		pdflatex ${reportfile}
		pdflatex ${reportfile}

.PHONY: clean

clean:
	@rm -f content/*.aux 
	@rm -f $(foreach ext, .ttt .idx .lot .lof .fff .aux .ps .bbl .blg .log .dvi .nav .nlo .out .ind .snm .spl .toc .vrb .ilg -blx.bib .run.xml,$(patsubst     %.tex,%$(ext),$(files)))
	@rm -f *.aux 
	@echo "All clean." 

neat:
	@rm -f $(foreach ext, .ttt .idx .lot .lof .fff .aux .ps .blg .dvi .nav .nlo .out .snm .spl .toc .vrb -blx.bib .run.xml,$(patsubst     %.tex,%$(ext),$(files)))
	@echo "All clean." 
