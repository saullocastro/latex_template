# Jupyter Book Latex template for Buckling Handbook

This repository provides a LaTeX template for creating JB2 (Jupyter Book 2) books using MyST Markdown, specifically configured for the Buckling Handbook.

## Using the template

Add the following code to the `myst.yml` file: 

```{code} yml

downloads:
    - id: output-pdf

exports:
    - format: pdf 
        output: exports/output_file.pdf
        template: { - TODO: replace with published link - }
        id: output-pdf
```

This will automatically apply the template when running `jupyter book build --pdf` in the command line. 
