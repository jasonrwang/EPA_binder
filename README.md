# EPA_binder

Binder config that can run Jupyter Notebook and R with the packages and tools you'll likely need for EPA1315 and EPA1333.

## How To

1. Fork this repository (repo) – you'll need a GitHub account
2. Upload the notebook files you need to run into your repo (this requires a "commit"). The "master" branch should be fine, though you should learn what this means.
3. Launch your Binder (or Google Colab)
4. Run the notebook or R files you need (or create a new one from the interface); make sure you're on the kernel you want
5. Save and download the saved file to your own computer and then re-upload it to your GitHub repository

Example: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jasonrwang/EPA_binder/master)
Example with RStudio: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jasonrwang/EPA_binder/master?urlpath=rstudio)

### Launching your Binder

You have two options to access Binder:

1. Go to [mybinder.org](https://mybinder.org) and follow the instructions there – use your own repo
2. Use this URL but paste in your own username: https://mybinder.org/v2/gh/jasonrwang/EPA_binder/master

Binder also lets you run RStudio directly instead of launching a Jupyter Notebook. To do this, simply add `?urlpath=rstudio` at the end of the URL (like in #2 above). For example, [https://mybinder.org/v2/gh/jasonrwang/EPA_binder/master?urlpath=rstudio](https://mybinder.org/v2/gh/jasonrwang/EPA_binder/master?urlpath=rstudio)

#### Alternative Option: Google Colab

If you're only using Python, you can also launch this in [Google Colab](https://colab.research.google.com/). It might be more user-friendly to use, but comes with a bunch of Google-specific stuff that might be annoying. You can easily integrate Google Colab with your GitHub account too, or you can keep the files in your Google Drive.

## Other

Comes with packages listed in:

- requirements.yml (Conda for Python)
- runtime.txt (specific version of Microsoft R – note this may differ from Conda's version)
- install.R (for R)

Note that the melt and cast features of `reshape2` can also be done in `tidyr`, which is part of tidyverse! See more [here](http://www.milanor.net/blog/reshape-data-r-tidyr-vs-reshape2/).

### Adding More Packages

Edit one of the above requirements/install files to include the package you want to use for next time you launch Binder. This may require Binder to recompile your working environment, which can take many, many

If you need to do something quickly, make a new cell and:

- With a Python kernel, run `%pip install package_name`
- With an R kernel, run `install.packages("package_name")`
