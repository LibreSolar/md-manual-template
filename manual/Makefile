# Targets not producing a file with their name
.PHONY: all pdf html clean

all:: pdf html

pdf:: metadata.yml *.md
	pandoc metadata.yml *.md -o manual.pdf --template template/eisvogel.tex --from markdown --listings --number-sections --toc

html:: metadata.yml *.md
	pandoc metadata.yml *.md -o manual.html --template template/mdbook.html --from markdown --listings --number-sections --toc --toc-depth=2 --katex

clean::
	rm -f manual.pdf
	rm -f manual.html
