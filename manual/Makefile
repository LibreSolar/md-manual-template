# Targets not producing a file with their name
.PHONY: all pdf html clean

all:: pdf html

pdf:: metadata.txt *.md
	pandoc metadata.txt *.md -o manual.pdf --template template/eisvogel.tex --from markdown --listings --number-sections --toc

html:: metadata.txt *.md
	pandoc metadata.txt *.md -o manual.html --template template/mdbook.html --from markdown --listings --number-sections --toc --toc-depth=2 --katex

clean::
	rm manual.pdf
	rm manual.html
