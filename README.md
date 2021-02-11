Game Manual 0
=============
![Docs Badge](https://readthedocs.org/projects/game-manual-zero/badge/) ![CI Badge](https://github.com/Coppersource/gm0/workflows/CI/badge.svg) ![Link Check](https://github.com/Coppersource/gm0/workflows/Link%20Check/badge.svg) [![Gitpod Ready-to-Code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/Coppersource/gm0)

Welcome to Game Manual 0 (gm0)!
This repository contains the source of Game Manual 0.

Building Game Manual 0
======================
Game Manual 0 employs the 
[Sphinx documentation generator](https://www.sphinx-doc.org/en/master/), 
and the articles themselves are written in 
[reStructuredText](http://docutils.sourceforge.net/rst.html).  

Requirements
------------
* Python 3
* TexLive
* dvipng
* graphviz
* make

Ensure the Python requirements are installed via running 
`python3 -m pip install -r source/requirements.txt`.

Building
--------

How to check if the documentation is valid:
* `make lint`
* `make linkcheck`

How to build the different versions of the documentation:
* `make html`
* `make latexpdf`

How to see the options for building:
* `make help`

How to develop the website:
* Run `make autobuild`
* This will set up a file watcher and build on file changes. A development server is served at `http://127.0.0.1:8000` by default. Go to your preferred browser and open that URL to view your local development version of gm0.