# Tutorial: Gene tree - Species tree inference using IQtree3 and ASTRAL
Mozes Blom, for questions [contact](mailto:mozes.blom@gmail.com)
___
## Requirements
* [Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/user/interface.html) and/or [Google Colab](https://colab.google/)
* Python 3+
    * [biopython](https://biopython.org/)
* [condacolab](https://github.com/conda-incubator/condacolab)
* [iqtree3](https://iqtree.github.io/) (installed using conda and the [bioconda repository](https://anaconda.org/bioconda/iqtree))
* [ASTRAL](https://github.com/smirarab/ASTRAL) (installed using conda and the [bioconda repository](https://anaconda.org/bioconda/astral-tree), v5.7.8)
___
## Introduction
The aim of this tutorial is to demonstrate how we can use large-scale datasets to infer phylogenies for genomic windows, sampled from across a chromosome, and how to use the resulting window-trees to infer a Summary-Coalescent species tree using [ASTRAL](https://github.com/smirarab/ASTRAL). Finally, we will use gene-concordance factor to investigate how well specific branches of the species tree are supported across all window trees. Lastly, the tutorial also highlights how you can upload your own data to a Google Colab instance, if you'd like to infer a ML phylogeny or a summary-coalescent species tree for your course project. This tutorial can be done on its own but has been developed as a computer practical which demonstrates topics discussed in a lecture on Gene trees - Species trees, presented during the MSc course Phylogenetics in Ecology & Evolution at Potsdam University.

This computer practical is styled in a Jupyter Notebook (NB) format (see Github [README](https://github.com/MozesBlom/tutorials/tree/main) for more details). In short, Jupyter NBs contain either text cells (such as the current cell) in Markdown format or code cells (frequently) in Python3 format. The aim of this practical is not to provide an exhaustive introduction into Python/Markdown/Jupyter, but to provide an introduction into phylogenomic inference using Maximum Likelihood. Therefore, all code to run this practical is already in place. In addition, there are several questions to be answered and you can double-click on the corresponding cells to enter your answer. Alternatively, you can just write them down for yourself.

The data included in this tutorial is a small subset (50 genomic windows, each 10Kb. in length) taken from a [recent study](https://royalsocietypublishing.org/doi/full/10.1098/rsbl.2024.0611) conducted in our group, focused on unraveling cryptic diversity in New Guinean Jewel babblers.