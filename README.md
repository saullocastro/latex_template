# Latex template for thesis

## Overview 

This repository provides a latex template for creating JB2 (Jupyter Book 2) books using MyST Markdown, specifically configured for bachelor’s and master’s thesis layouts. {todo: these will probably look different, different repos?}

Folders in this repository:

- Template - the template used for the conversion to PDF
- Templates - other templates (will be changed later)
- parts - parts of the thesis (introduction, method, etc)
- notebooks - supporting notebooks for the thesis
- exports - contains pdf version
- project.md - main project file

### Different formats 

JupyterBook supports producing your report in multiple formats, including:
- <b> web-based format: </b> Ideal for online reading, interactive content and sharing with supervisors and collaborators. An example can be seen [here](https://luukfroling.github.io/BEP/)
- <b> PDF format: </b> Suitable for official submission and printing. This repository focuses on providing a template specifically designed for the PDF format. 

## How to use this template

The following instructions will guide you through the process of: 

- Copying this repository into your own GitHub account
- Editing your thesis using VS Code (or another editor)
- Viewing your thesis as a website or as a PDF
- Adjusting the template to your needs

Make sure the following are installed: 

- Visual Studio Code (or any editor with a terminal)
- GitHub Desktop (or Git)
- Python

### Install Jupyter Book

Start by installing Jupyter Book: 
:::{code}
pip install "jupyter-book>=2.0.0a0"
:::

### Create repository

1) Click the green button `use this template` and click `create a new repository`.
2) Choose a proper name of your repository (this will be also part of your URL!) and choose the option public.
3) In your repository, click on settings and in the left menu on Pages and choose Github Actions.

This enables automatic building and publishing of the web-based version of your thesis.

### View web-based book locally

1) Clone the new repository to your device using Github Desktop (or Git). Using the dekstop version, go to clone repository > your repositories > {new repository name}. 
2) Open the project in an editor of choice. 
3) In a terminal, use `jupyter book start` and navigate to http://localhost:3000/ in your browser. 

Changes you make in the editor will automatically refresh in the local web preview.

### View web-based book via GitHub-actions

1) commit and push changes to GiHub
2) After the workflow completes, the web version will be available under GitHub Pages. You can access it via `https://<your-username>.github.io/<your-repository>/`.

### Build PDF version locally

To produce a PDF: 

```{code} 
jupyter book build --pdf
```

You can configure the output name and location in your myst.yml file:

```{code}
:emphasize-lines: 3

exports:
    - format: pdf 
        output: exports/output_file.pdf
        template: custom_theme
        id: output-pdf
```
## Making changes to the template 

## Alternatives / further reading

- typst 

- adding overleaf

- using overleaf tex templates instead