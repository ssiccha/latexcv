# Settings
TARGET=main
OUTNAME=Siccha-Sergio-CV
PDFLATEX=latexmk --pdf -file-line-error -halt-on-error

EXTRA_DEPS :=
TEXOPTS := --synctex=1 -shell-escape --file-line-error --halt-on-error

# Rules
all : $(OUTNAME).pdf

$(OUTNAME).pdf : $(TARGET).tex *.tex $(EXTRA_DEPS)
	$(PDFLATEX) $(TEXOPTS) $<

clean :
	rm -f *.aux *.bbl *.bcf *.blg *.fdb_latexmk *.fls *.log *.out *.run.xml *.synctex.gz *'.synctex.gz(busy)' *.toc *.xyc


dist-clean : clean
	rm -f $(TARGET).pdf $(OUTNAME).pdf

.PHONY: all clean dist-clean
