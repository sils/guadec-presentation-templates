NULL =

SRC = guadec-example.tex
PANDOC_SRC = presentation.md

OUT = $(SRC:%.tex=%.pdf)
PANDOC_OUT = $(PANDOC_SRC:%.md=%.pdf)

BYPRODUCTS = \
	$(SRC:%.tex=%.aux) \
	$(SRC:%.tex=%.log) \
	$(SRC:%.tex=%.nav) \
	$(SRC:%.tex=%.out) \
	$(SRC:%.tex=%.snm) \
	$(SRC:%.tex=%.toc) \
	$(NULL)

default: pandoc

ctex: tex clean
tex: $(OUT)

pandoc:
	pandoc $(PANDOC_SRC) -t beamer -s -o $(PANDOC_OUT) --smart \
	-V theme:guadec --slide-level 2

%.pdf: %.tex
	pdflatex $<

clean:
	rm -Rf $(OUT) $(BYPRODUCTS)

.PHONY: all clean

