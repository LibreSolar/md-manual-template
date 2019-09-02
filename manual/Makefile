# Targets not producing a file with their name
.PHONY: all pdf html clean

all:: pdf html

pdf:: metadata.yml *.md
	pandoc \
		metadata.yml *.md \
		--output manual.pdf \
		--template template/eisvogel.tex \
		--from markdown \
		--listings \
		--number-sections \
		--table-of-contents \
		--metadata date="`date -u '+%Y-%m-%d'`"

html:: metadata.yml *.md
	pandoc \
		metadata.yml *.md \
		--output manual.html \
		--template template/mdbook.html \
		--from markdown \
		--listings \
		--number-sections \
		--table-of-contents \
		--toc-depth=2 \
		--katex \
		--metadata date="`date -u '+%Y-%m-%d'`"

clean::
	rm -f manual.pdf
	rm -f manual.html
