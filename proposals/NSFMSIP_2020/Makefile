# LatexPDF make file
#
# Define the file name
name = main

all: full

# Add -shell-escape if plot directory is not a subdirectory of tex file location
full: $(name).tex
	pdflatex -shell-escape $(name).tex
	bibtex $(name)
	pdflatex -shell-escape $(name).tex
	pdflatex -shell-escape $(name).tex


.phony: clean

clean:
	rm -f *.aux *.log *.out *.toc $(name).pdf $(name).dvi
