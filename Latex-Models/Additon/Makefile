# LaTeX notes, compiled with XeLaTeX (needed for Chinese via xeCJK).

# Use the first .tex file found in this directory, or override with
# `make SRC=myfile.tex`.
SRC      ?= $(firstword $(wildcard *.tex))
PDF      := $(SRC:.tex=.pdf)
XELATEX  := xelatex
XELATEXFLAGS := -interaction=nonstopmode -halt-on-error -synctex=1

ifeq ($(SRC),)
$(error No .tex source found. Place a .tex file here or run `make SRC=file.tex`)
endif

.PHONY: all clean cleanall

all: $(PDF)

$(PDF): $(SRC)
	$(XELATEX) $(XELATEXFLAGS) $(SRC)
	$(XELATEX) $(XELATEXFLAGS) $(SRC)

clean:
	rm -f *.aux *.log *.out *.toc *.synctex.gz

cleanall:
	rm -f *.aux *.log *.out *.toc *.synctex.gz $(PDF)
