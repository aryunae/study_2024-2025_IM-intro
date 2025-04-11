FILES = $(patsubst %.md, %.docx, $(wildcard *.md))
FILES += $(patsubst %.md, %.pdf, $(wildcard *.md))

FILTERS = --filter pandoc-crossref
OPTIONS = --number-sections
PDF_ENGINE = --pdf-engine=xelatex
PDF_OPTIONS = --pdf-engine-opt=--shell-escape

%.docx: %.md
	-pandoc "$<" $(FILTERS) $(OPTIONS) -o "$@"

%.pdf: %.md
	-pandoc "$<" $(FILTERS) $(PDF_ENGINE) $(PDF_OPTIONS) $(OPTIONS) -o "$@"

all: $(FILES)

clean:
	-rm $(FILES) *~

cleanall: clean

