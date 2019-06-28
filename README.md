# Markdown Manual

This is a template that uses [Pandoc](https://pandoc.org/) to auto-generate PDF and HTML manuals based on markdown content.

It can be easily integrated into existing repositories and deployed via gh-pages.

## PDF generation

PDF files are generated using LaTeX, so a working LaTeX engine needs to be installed on your system already (e.g. texlive). The manual uses the [Eisvogel](https://github.com/Wandmalfarbe/pandoc-latex-template) template.

```
cd manual
make pdf
```

## HTML generation

The HTML template is based on the great [mdBook](https://github.com/rust-lang-nursery/mdBook) theme, which was simplified and adjusted a bit to suit the needs of a manual.

```
cd manual
make html
```
