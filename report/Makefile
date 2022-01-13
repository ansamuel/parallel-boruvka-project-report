all: $(patsubst %.tex, %.pdf, $(wildcard *.tex))

%: %.pdf
	@echo -n ""

%.pdf: %.tex
	latexmk -pdf -pdflatex="pdflatex -interaction=nonstopmode" -use-make $<

clean:
	latexmk -CA
	rm *.bbl *-eps-converted-to.pdf

spell:
	ispell -f ispell.words -t *.tex
