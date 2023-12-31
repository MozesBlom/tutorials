# Tutorial: Exploring coalescent variation across the genome
Mozes Blom, for questions [contact](mailto:mozes.blom@gmail.com)
___
## Requirements
* [Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/user/interface.html) and/or [Google Colab](https://colab.google/)
* Python 3+
    * [msprime](https://msprime.readthedocs.io/en/stable/)

___
## Introduction

The overarching aim of this practical is to visualise how genealogical history can vary across the genome and use computer simulations to explore how the rate of deep coalescence scales with past population dynamics. This tutorial can be done on its own but has been developed as a computer practical which demonstrates topics discussed in two introductory lectures: i. **Phylogenetics in the Genomic Era** and ii. **Reconciling gene tree - species tree discordance**.

For this computer practical, we will use Python modules but a minimal understanding of Python code itself will be needed as all necessary code is written out in a Jupyter Notebook. However, for those unfamiliar with Jupyter Notebooks, you can find a short introduction below to get you started.

#### Introduction to Jupyter Notebooks.
[Jupyter Notebooks](https://jupyter-notebook.readthedocs.io/en/latest/) are notebooks for computational projects, which can include snippets of code, annotation/comments and the output of code. It is an excellent way to keep track of the code that you built, the rationale behind it and is an excellent format to share code/ideas with colleagues (or your future self!).

A Jupyter notebook can contain several different sections.

<img src="img/notebook.png">

**Section 1** is regular text in Markdown format. Markdown is a simple to use formatting language that automatically takes care of the formatting of plain text in documents. It's basically a code version of similar actions that you do in Microsoft Word using point and click. Here are a few [examples](https://www.markdownguide.org/cheat-sheet/). If you don't use any of the markdown formatting, text filled out in Jupyter notebook cells will simply appear as regular text in standard font. However, by using the markdown formatting you can create rich annotations that include links, images, etc. The present README document that you are reading is for example completely written in Markdown!

**Section 2** of the notebook are code cells. These cells/blocks generally include Python (hence the 'Py' in 'juPYter') code and can be used for computational purposes. The major benefit of Jupyter notebooks is that not only the result, but the code itself can be shared as well. In combination with the code annotation, it enables us to share our work and keep track of what/why we created a certain block of code.

**Section 3** of the notebook is the output of the code above (if output is to be expected from the code above). To make things a bit confusing: When we refer to a Jupyter notebook, we can either refer to an actual notebook created in accordance with the Jupyter notebook format (as outlined above) or the notebook application developed under the [Project Jupyter](https://jupyter-notebook.readthedocs.io/en/latest/) umbrella. By opening a notebook and going through the notebook in the editor, we can actually run the Python code in the cell blocks and evaluate the output (as done here in Section 3).

Jupyter Notebook is the lightweight application to run notebooks, but it requires a bit of background understanding to run this from commandline. Moreover it now has been generally superseded by [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/) for which there is also a Desktop application: [JupyterLab Desktop](https://github.com/jupyterlab/jupyterlab-desktop)

**SUMMARY**: Computational notebooks in Jupyter format ('Jupyter notebooks') are a great way to share code and explore datasets. They are widely used in data science and are increasingly used for computational biology as well. To open and run a Jupyter notebook, we can use applications such as JupyterLab or the desktop version Jupyterlab Desktop. The Jupyter notebook called 'XXX' will be used for the present tutorial.

#### Jupyterlab vs. Google Colab

Understanding the Notebook format itself, we now focus on the application that we will use during this practical to go through the already prepared notebook. [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/) or [JupyterLab Desktop](https://github.com/jupyterlab/jupyterlab-desktop) are both excellent choices to run on your own laptop. However, for the sake of the present practical, they are not optimal due to the background knowledge required to handle with dependencies. Dependencies are modules (software packages effectively) that can be required for a specific activity. For example, in this computer practical we want to do coalescent simulations and we therefore require a python package, [msprime](https://msprime.readthedocs.io/en/stable/), that is not standard packed with every Python installation. Handling python dependencies and modules is relatively straightforward using a package manager such as [(mini)conda](https://docs.conda.io/en/latest/miniconda.html), but it does require some command line knowhow. To avoid this, we will first try to use [Google Colab](https://colab.google/), **HOWEVER I would strongly suggest to also install [JupyterLab Desktop](https://github.com/jupyterlab/jupyterlab-desktop) on your personal machine before the computer practical!** In case the internet connection is spotty OR there are not sufficient Colab instances available, we will switch to Jupyterlab Desktop during the computer practical.

**[Google Colab](https://colab.google/)**

The major benefit of Google Colab is that nothing needs to be installed on your personal machine, everything is executed on a Google computing instance. Here is a [link](https://www.youtube.com/watch?v=inN8seMm7UI) to a short introduction video and [overview](https://colab.research.google.com/?utm_source=scs-index#scrollTo=5fCEDCU_qrC0). The only thing what you need to do is to sign up for a [Google Account](https://www.google.com/account/about/) and login. Then navigate to the **[Google Colab](https://colab.google/)** webpage and click on `Open Colab`. If you are signed in with your Google Account, this should look like:

<img src="img/colab_landing_page.png">

Here you can create a new notebook, continue a previous notebook which you stored locally or on Google Drive, etc. Here we benefit from the Github integration and directly point Colab to the present Github page with the tutorial:

<img src="img/colab_landing_page.png">

Copy paste the link of the present github webpage, select the only notebook present (**2023_coalescent_variation.ipynb**) and it should automatically kickstart the tutorial notebook!

