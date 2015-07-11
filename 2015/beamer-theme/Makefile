NULL =

SRC = guadec-example.tex

OUT = $(SRC:%.tex=%.pdf)

BYPRODUCTS = \
	$(SRC:%.tex=%.aux) \
	$(SRC:%.tex=%.log) \
	$(SRC:%.tex=%.nav) \
	$(SRC:%.tex=%.out) \
	$(SRC:%.tex=%.snm) \
	$(SRC:%.tex=%.toc) \
	$(NULL)

all: $(OUT)

%.pdf: %.tex
	pdflatex $<

clean:
	rm -Rf $(OUT) $(BYPRODUCTS)

.PHONY: all clean

