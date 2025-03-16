# R-template
Template for a data analysis project in R 

# Quick guide
This repo contains a template for a data analysis project in R.
The objective is to make it easy for any R users to set up a data analysis project.
To use the template click the green "Code" button at the top to clone the repo, or [download](https://github.com/sashahafner/R-template/archive/refs/heads/main.zip) a ZIP archive.
Extract the files, move to a suitable directory, navigate to `scripts/main.R`, and start editing the scripts to fit your project.
Or, starting from GitHub, click the green "Use this template" button.

# Some more details
R scripts are in the `scripts` subdirectory.
This template is set up so all the R code can be run by running `main.R`, e.g., in an R console:
```
> source('main.R')
```
Of course, the working directory must be set to `scripts`.
(This is the default behavior when a script is opened for some development environments, but not all.)

All the code in the scripts is simply for demonstration, but in several cases it could be useful to keep it.
Lines in the scripts that start with `# RAD:` are meant to be read and then deleted.

Input data goes in the `data` subdirectory.
Notes can go in `data/README.md` and original data in `data/original`.

The `logs` subdirectory is used for a text file log of R and package versions (created by `scripts/packages.R` and a pdf record of the analysis (see `scripts/analayis.Rmd`).

Output can be found in `output`, and plots in `plots`.

Lastly, a README.md file should be included for any other notes for collaborators and future users (including yourself).
The file you are reading can be used as a template.

Note that all file paths are relative, so this repo is completely portable. 
We recommend sticking with this approach, and further, not setting a working directory by R code.

This template is not linked to any particular operating system, script editor, or development environment.
Most of us use RStudio, some use Subline Text, and at least one [Neovim](https://neovim.io/) with the [Nvim-R](https://github.com/jalvesaq/Nvim-R) plugin.
But any text editor could be used to write R code, and it is possible to use R without installing any separate integrated development environment (IDE).

# Justification
What we have presented here is just one alternative for organizing data analysis projects.
It is a structure that we have converged on over several years of projects. 
Some original inspiration came from [this Stackoverflow post](https://stackoverflow.com/questions/1429907/workflow-for-statistical-analysis-and-report-writing) and [this blog entry](https://robjhyndman.com/hyndsight/workflow-in-r/).
Some users may find the use of so many separate scripts confusing and unnecessary.
Why not use one big script, or even a single RMarkdown file?
We find the more modular approach used in this repo better for the following:

* Getting a workflow overview: just check `main.R`
* Isolating code problems: it is easy to find scripts by name and see which ones throw errors
* Editing/writing/testing code: work in a single script, run the whole thing to test it (no need to navigate to a particular line of code in a larger file)
* And also perhaps re-using code: easy to copy individual scripts

The modular approach given here is faster than a single large (or several) RMarkdown file(s) (although we have included one for a record of data analysis output). 
Lastly,this approach is not dependent on RStudio or any other particular software (unlike [R Notebooks](https://www.rstudio.com/blog/r-notebooks/)).

# Related work
There are other repos on GitHub with a similar objective.
* <https://github.com/cboettig/template>
* <https://github.com/Pakillo/template>
* <https://github.com/bdcaf/cookiecutter-r-data-analysis>
* <https://github.com/klmr/example-r-analysis>
