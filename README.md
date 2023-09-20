# [Bibtex to Markdown Converter](https://github.com/awesomedev08/bibtex-to-markdown-next)

[![Download from PyPI](https://img.shields.io/pypi/v/academic.svg?style=for-the-badge)](https://pypi.python.org/pypi/academic)
[![Discord](https://img.shields.io/discord/722225264733716590?style=for-the-badge)](https://discord.com/channels/722225264733716590/742892432458252370/742895548159492138)
[![GitHub Sponsors](https://img.shields.io/github/sponsors/gcushen?label=%E2%9D%A4%EF%B8%8F%20sponsor&style=for-the-badge)](https://github.com/sponsors/gcushen)
[![Twitter Follow](https://img.shields.io/twitter/follow/georgecushen?label=Follow%20on%20Twitter&style=for-the-badge)](https://twitter.com/GeorgeCushen)
[![GitHub followers](https://img.shields.io/github/followers/gcushen?label=Follow%20on%20GH&style=for-the-badge)](https://github.com/gcushen)  


### 📚 Easily import publications from your reference manager to your Markdown-formatted website or book

**Features**

* Import Bibtex publications (such as **books, conference proceedings and journals**) from your reference manager to your Markdown-formatted website or book
  * Simply export a BibTeX file from your reference manager, such as [Zotero](https://www.zotero.org), and provide this as the input to the converter tool
* Compatible with all static website generators such as Next, Astro, Gatsby, Hugo, etc.


**❤️ Support this open-source software**

To help us develop this converter tool and the associated Wowchemy software sustainably under the MIT license, we ask all individuals and businesses that use it to help support its ongoing maintenance and development via sponsorship and contributing.

Support development of the Academic CLI:

  - ❤️ [Become a **GitHub Sponsor** and **unlock perks**](https://github.com/sponsors/gcushen)
  - ☕️ [**Donate a coffee**](https://github.com/sponsors/gcushen)
  - 👩‍💻 [**Contribute**](#contribute)

## Prerequisites

1. Install [Python 3.11+](https://realpython.com/installing-python/) if it’s not already installed

## Installation

Open your Terminal or Command Prompt app and install the Academic CLI tool:

    pip3 install -U academic
    
Or, help test the latest development version:

    pip3 install -U git+https://github.com/wowchemy/hugo-academic-cli.git

## Usage

Download references from your reference manager, such as Zotero, in the Bibtex format.

Use the `cd` command to navigate to the folder containing your Bibtex file:

    cd <MY_BIBTEX_FOLDER>

**Import publications:**

Say we downloaded our publications from our reference manager, such as Zotero, to a file named `my_publications.bib` within the website folder. We can import them into the default `content/publication/` folder with:

    academic import --bibtex my_publications.bib

**Import publications to a specific folder (e.g. `content/zh/publication`):**

Say our site has multiple languages, we may want to output the publications to a specific folder with:

    academic import --bibtex my_publications.bib --publication-dir content/zh/publication/

Optional arguments:

* `--publication-dir PUBLICATION_DIR` Folder to import publications to (defaults to `content/publication`)
* `--overwrite` Overwrite any existing publications in the output folder
* `--normalize` Normalize tags by converting them to lowercase and capitalizing the first letter (e.g. "sciEnCE" -> "Science")
* `--featured` Flag these publications as *featured* (to appear in *Featured Publications* widget)
* `--verbose` or `-v` Show verbose messages
* `--help` Help


## Contribute

Interested in contributing to **open source** and **open science**?

Learn [how to contribute code on Github](https://codeburst.io/a-step-by-step-guide-to-making-your-first-github-contribution-5302260a2940).

For local development, clone this repository and use Poetry to install and run the converter using the following commands:

    git clone https://github.com/wowchemy/bibtex-to-markdown.git
    cd bibtex-to-markdown
    poetry install
    poetry run academic import --bibtex=tests/data/article.bib --publication-dir=debug --overwrite

Preparing a contribution:

- Lint: `make lint`
- Format: `make format`
- Test: `make test`

