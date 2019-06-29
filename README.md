# Markdown Manual

This is a template that uses [Pandoc](https://pandoc.org/) to auto-generate PDF and HTML manuals based on markdown content.

It can be easily integrated into existing repositories and deployed via gh-pages.

Please install the most recent Pandoc package to get best results.

## PDF generation

PDF files are generated using LaTeX, so a working LaTeX engine needs to be installed on your system already (e.g. texlive incl. extra fonts). The manual uses the [Eisvogel](https://github.com/Wandmalfarbe/pandoc-latex-template) template.

```
cd manual
make pdf
```

Example:
- [Raw PDF file](https://github.com/LibreSolar/md-manual-template/blob/gh-pages/manual.pdf) as deployed to gh-pages branch
- [PDF file download](https://libre.solar/md-manual-template/manual.pdf)

## HTML generation

The HTML template is based on the great [mdBook](https://github.com/rust-lang-nursery/mdBook) theme, which was simplified and adjusted a bit to suit the needs of a manual.

```
cd manual
make html
```

Example:
- [Raw HTML file](https://github.com/LibreSolar/md-manual-template/blob/gh-pages/index.html) as deployed to gh-pages branch
- [Hosted website](https://libre.solar/md-manual-template/)

## Automatic deployment with Travis CI

Using the configuration in `.travis.yml`, the manual is rebuilt after each commit and automatically published using GitHub pages.

In a new repository you have to prepare the `gh-pages` branch in advance:

```
git checkout --orphan gh-pages
git rm -rf .
echo "My GitHub Page" > index.html
git add index.html
git commit -m "First pages commit"
git push origin gh-pages
```

You can find the atomatically deployed example manual of this repository here: [https://libre.solar/md-manual-template/](https://libre.solar/md-manual-template/).
