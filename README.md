# Fast non-linear gravity inversion in spherical coordinates

[Leonardo Uieda](http://www.leouieda.com)
and
[Valéria C. F. Barbosa](http://lattes.cnpq.br/0391036221142471)

**Submitted for publication in the Geophysical Journal International**.

This repository contains Python source code that implements the Moho inversion
method proposed in the paper.  Also included are all data and code required to
produce the results and figures presented in the paper.  The source code for
the Moho inversion method is in the file `code/mohoinv.py`.  The file
`code/datasets.py`  contains utility functions and classes to handle the
datasets and the CRUST1.0 model used in the paper.  The inversions and figure
generation are performed in [Jupyter notebooks](http://jupyter.org/), the
`.ipynb` files in `code`.  You can view static (non-executable) versions of
these files in [the nbviewer webservice](http://nbviewer.jupyter.org/github/pinga-lab/paper-moho-inversion-tesseroids/tree/master/code/).
PDF versions of the notebooks are also available in the `code` folder.

The method was used to estimate the Moho depth of South America.  The final
estimated Moho model for South America is available the file
`model/south-american-moho.txt` in ASCII xyz format.
`model/south-american-moho.jpg` is a preview of what the model looks like
(figure `manscript/figures/south-america-moho.eps` from the paper):

![Preview of the estimated Moho depth for South America](https://raw.githubusercontent.com/pinga-lab/paper-moho-inversion-tesseroids/master/model/south-american-moho.jpg?token=AARtIt4v4DyB2aGd81JkbfVlM7sbFqq5ks5W_ClzwA%3D%3D)


## Reproducing the results

You can download a copy of all the files in this repository by cloning the
[git](https://git-scm.com/) repository:

    git clone https://github.com/pinga-lab/paper-moho-inversion-tesseroids.git

or [click here to download a zip archive](https://github.com/pinga-lab/paper-moho-inversion-tesseroids/archive/master.zip).

### Setting up your environment

You'll need a working Python **2.7** environment with all the standard
scientific packages installed (numpy, scipy, matplotlib, etc).  The easiest
(and recommended) way to get this is to download and install the
[Anaconda Python distribution](http://continuum.io/downloads#all).
Make sure you get the **Python 2.7** version.  All the packages that you'll
need are specified in the `environmet.yml` file.  You'll also need to install
the latest development version of the
[Fatiando a Terra](http://www.fatiando.org/) library.

Unzip the contents of this repository (if you've downloaded the zip file) and
`cd` into the root of the repository.  You can use `conda` package manager
(included in Anaconda) to create a virtual environment with all the required
packages installed (including Fatiando). Run the following command in the
repository folder (where `environment.yml` is located):

    conda env create

To activate the conda environment, run

    source activate moho

or, if you're on Windows,

    activate moho

This will enable the environment for your current terminal session.

### Running the inversions and generating figures

The inversion and figure generation are all run inside Jupyter notebooks.  To
execute them, you must first start the notebook server by going into the
repository folder and running (make sure you have the `conda` environment
enabled first):

    jupyter notebook

This will start the server and open your default web browser to the Jupyter
console interface.  In the page, go into the `code` folder and select the
notebook that you wish to view/run.

Here what a notebook looks like running in Firefox:

![Screenshot of the Jupter notebook](https://raw.githubusercontent.com/pinga-lab/paper-moho-inversion-tesseroids/master/screenshot-jupyter-notebook.png?token=AARtIq6LujCeiRLJLIjqQyqAGnV3KS0aks5W_CY1wA%3D%3D)

The notebook is divided cells (some have text while other have code).  Each can
be executed using `Shift + Enter`. Executing text cells does nothing and
executing code cells runs the code and produces it's output.  To execute the
whole notebook, run all cells in order.

All results figures in the paper are generated by the
`code/paper-figures.ipynb` notebook.

## License

All source code is made available under a BSD 3-clause license.  You can freely
use and modify the code, without warranty, so long as you provide attribution
to the authors.  See `LICENSE.md` for the full license text.

The manuscript text is not open source. The authors reserve the rights to the
article content, which is currently submitted for publication in the
Geophysical Journal International.
