# Tutorial: Maximum Likelihood phylogeny inference
Mozes Blom, for questions [contact](mailto:mozes.blom@gmail.com)
___
## Requirements
* [Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/user/interface.html) and/or [Google Colab](https://colab.google/)
* Python 3+
    * [biopython](https://biopython.org/)
* [condacolab](https://github.com/conda-incubator/condacolab)
* [iqtree3](https://iqtree.github.io/) (installed using conda and the [bioconda repository](https://anaconda.org/bioconda/iqtree))
___
## Introduction
The overarching aim of this practical is to demonstrate how we can infer a phylogeny using Maximum-Likelihood and how we can use IQtree3 to achieve this objective. This tutorial can be done on its own but has been developed as a computer practical which demonstrates topics discussed in a lecture on Maximum-Likelihood inference, presented during the MSc course Phylogenetics in Ecology & Evolution at Potsdam University.

This computer practical is styled in a Jupyter Notebook (NB) format (see Github [README](https://github.com/MozesBlom/tutorials/tree/main) for more details). In short, Jupyter NBs contain either text cells (such as the current cell) in Markdown format or code cells (frequently) in Python3 format. The aim of this practical is not to provide an exhaustive introduction into Python/Markdown/Jupyter, but to provide an introduction into phylogenomic inference using Maximum Likelihood. Therefore, all code to run this practical is already in place. In addition, there are several questions to be answered and you can double-click on the corresponding cells to enter your answer. Alternatively, you can just write them down for yourself.

This tutorial is loosely based on a workshop organised by the developers of IQ-Tree (Minh Bui et al.) and includes a subset of data from [Chiara et al. (2012)](https://bmcbiol.biomedcentral.com/articles/10.1186/1741-7007-10-65). It contains all the commands to infer a ML phylogeny for this dataset but I would strongly encourage to explore the rich functionality of the programme and the fantastic [documentation](https://iqtree.github.io/doc/) with examples, explanations and walk-throughs.