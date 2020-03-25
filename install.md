---
layout: default
title: install (GAAs only)
nav_order: 10
description:
---


# Editing R files via jupyter Notebook

## Windows

1. Install Anaconda

1. Install R

1. Launch Anaconda

1. Create a new conda environment called `reasearch-commons`

1. Press the play button to open the conda terminal

    * Install Jupyter - run `conda install -c anaconda jupyter` in the conda terminal

    * Install R-essentials - run `conda install -c r r-essentials` in the conda terminal

1. Navigate to the directory where you downloaded this repo

    * e.g. `cd /Workspace/intro-r/jupyter`

    * `Ctrl + c` terminates the process

1. Start the jupyter notebook - run `jupyter notebook .`

1. A new window in your browser will open, click on `workshop` and start running the commands in the Jupyter environment

1. Once you finish editing and running all the workshop, click in `file` > `download` > `markdown`


# Adding the changes to the rc-template

## Windows

1. Install Ruby

1. Install Jekyll

1. Open the windows menu and run `Start Command Prompt with Ruby`

1. Navigate to the directory where you downloaded this repo

    * e.g. `cd /Workspace/intro-r`

1. Compile & run Jekyll

    * run `bundle install` in the ruby terminal

    * run `bundle exec jekyll s` in the ruby terminal

    * It will show that jekyll is running at `http://127.0.0.1:4000/intro-r/`

    * `Ctrl + c` terminates the process

1. Copy the contents of the Markdown file exported from Jupyter into the appropriate files:

    * `index.md`

    * `data_manipulation.md`

    * `descriptive_stats.md`

    * `inference_stats.md`

    * `conclusions.md`

1. This part is particularly boring, but you need to go over the `.md` files and edit images and tables

    * the best way to do this is with `edit` > `replace`

        * from `src="figures/` to `src="{{site.baseurl}}/jupyter/figures/`

        * from `<th scope=col>` to `<th scope="col">`

1. Refresh the jekyll url and check changes. 




