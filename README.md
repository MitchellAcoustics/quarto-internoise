# INTER-NOISE 2024 Template for Quarto

## Creating a New Article

You can use this as a template to create an article for an AFT journal. To do this, use the following command:

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

You can view a preview of the rendered template at https://quarto-journals.github.io/article-format-template/.
