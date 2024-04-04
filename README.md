# INTER-NOISE 2024 Template for Quarto

## Creating a New Article

You can use this as a template to create an article for the INTER-NOISE Conference. To do this, use the following command:

```bash
quarto use template MitchellAcoustics/quarto-internoise
```

This will install the extension and create an example qmd file and bibiography that you can use as a starting place for your article.

## Installation For Existing Document

You may also use this format with an existing Quarto project or document. From the quarto project or document directory, run the following command to install this format:

```bash
quarto add MitchellAcoustics/quarto-internoise
```

## Usage

To use the format, you can use the format names internoise-pdf and internoise-typst. For example:

```bash
quarto render article.qmd --to internoise-pdf
```

or in your document yaml

```yaml
format:
  internoise-typst: default
```

## Typst and LaTeX

(Typst)[https://typst.app/home] is a new markup-based typesetting system for the sciences. It is designed to be an alternative both to advanced tools like LaTeX and simpler tools like Word and Google Docs. While it is still new and perhaps not as mature at LaTeX, it is *much faster* to render (nearly instant). 

The Typst template has been designed to be nearly identical to the original INTER-NOISE template. When using the Typst template, you should use the `bib-typst: sample.bib` field in the yaml header, rather than `bibliography: `. This passes the raw citation commands to Typst (which uses the same basic `@citekey` syntax as Quarto) to let it handle creating the Bibliography better.

The most noticable difference for these Quarto templates compared to the original INTER-NOISE template is the use of [1], [2], [3] rather than 1., 2., 3. in the bibliography. This is because the original LaTeX template uses the unsrt with bibtex; Quarto uses biblatex rather than bibtex, so unsrt is not available. In its place, we've used a modified version of the IEEE reference format which renders consecutive references in text as [1-4] rather than [1][2][3][4].

You can view a preview of the rendered template [here](template_typst.pdf).
