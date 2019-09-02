OUT_DIR = build
RESOURCES = template images
MKDIR_P = mkdir -p

# Targets not producing a file with their name
.PHONY: all pdf html dist clean

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

dist:: all
	${MKDIR_P} ${OUT_DIR}
	cp -r ${RESOURCES} ${OUT_DIR}/
	mv manual.pdf ${OUT_DIR}/
	mv manual.html ${OUT_DIR}/index.html

clean::
	rm -f manual.pdf
	rm -f manual.html
	rm -rf ${OUT_DIR}
