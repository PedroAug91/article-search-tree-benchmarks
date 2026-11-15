MAIN := main
PDF := $(MAIN).pdf
LATEXMK := latexmk

.PHONY: all build watch clean distclean view

all: build

build:
	$(LATEXMK) -pdf -interaction=nonstopmode -halt-on-error $(MAIN).tex

watch:
	$(LATEXMK) -pdf -pvc -interaction=nonstopmode $(MAIN).tex

clean:
	$(LATEXMK) -c $(MAIN).tex

distclean:
	$(LATEXMK) -C $(MAIN).tex

view: build
	xdg-open $(PDF)
