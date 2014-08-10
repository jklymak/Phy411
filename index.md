---
layout: default
title: Home
---

# Uvic Ocean Physics software page

This is a list of useful software we may need.

## [brew](http://brew.sh)

If `brew` is not already on your computer, see Install Homebrew at [http://brew.sh]() and follow the prompts.  Brew is the *nix package manager for OS X, and it largely has what we want.

## [git](github.com)

git is the version control system we use.  Some of our stuff is kept on [github](github.com), which is a public repository of our code.  See [http://jklymak.github.com]().

    brew install git

You probably want to set up a github account.

## [jekyll](http://jekyllrb.com)

    sudo gem install jekyll

jekyll is the site generator for these webpages, and how we will serve the documentation for each project.  Github runs it automatically if you follow the directions at [http://jklymak.github.io/projtemplate]().  However, if you want to preview the webpage locally before committing and pushing it, then you can run 

    jekyll serve --baseurl ''

and you will be able to see it at [http://localhost:4000/]().  

## Editors and Document Preparation:

For general editing, I use [Sublime Text](http://www.sublimetext.com) or Emacs.  

For formal document preparation, I keep a Latex files.  For OS X use [MacTeX](https://tug.org/mactex/) and it will install TexShop and BibDesk

For [LaTeX](http://www.latex-project.org) I use [TexShop](http://pages.uoregon.edu/koch/texshop/), or [TexPad](https://www.texpadapp.com).  

For my bibliographies, I use [bibtex](http://www.bibtex.org) and [Bibdesk](http://bibdesk.sourceforge.net).  

## Data Analysis

For data analysis I almost exclusive use python now.  All the libraries I use can be installed from [Anaconda](https://store.continuum.io/cshop/anaconda/).  

### Python libraries

Most libraries not included with [Anaconda](https://store.continuum.io/cshop/anaconda/) can be included by running

    conda update
    conda install newlib

You may have to append `sudo`.

My libraries are at [https://github.com/jklymak/pythonlib](https://github.com/jklymak/pythonlib), and I'll try to keep them up to date.  The way to clone these using git is to go to the directory above where you want to install the library and:

    cd ~/python
    git clone git://github.com/jklymak/pythonlib.git

This will install a directory `~/python/pythonlib`

To make sure python sees this, modify the `PYTHONPATH` by adding the following two lines to `~/.profile`:

    PYTHONPATH="/Users/yourlogin/python/pythonlib/:${PYTHONPATH}"
    export PYTHONPATH

### [ipython notebook](http://ipython.org/notebook.html)

I run [ipython notebook](http://ipython.org/notebook.html) for most of my analysis.  To get this running I  type:

    % ipython notebook --profile=nbserver &

I think ipython sets this up automatically.  If they don't lets update this documentation.  

Then, you need to open [Firefox](www.mozilla.org/en-US/firefox/new/), to [http://localhost:9999/](http://localhost:9999/) and your notebook will appear.  You can start entering python code and running it.  The result will be saved in `Notebookname.ipynb` in the directory you are working in (where you choose the `Notebookname`).  












