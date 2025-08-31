# Tutorial: Exploring coalescent variation across the genome
Mozes Blom, for questions [contact](mailto:mozes.blom@gmail.com)
___
## Requirements
* [Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/user/interface.html) and/or [Google Colab](https://colab.google/)
* Python 3+
    * [msprime](https://msprime.readthedocs.io/en/stable/)

___
## Introduction

The overarching aim of this practical is to visualise how genealogical history can vary across the genome and use computer simulations to explore how the rate of deep coalescence scales with past population dynamics. This tutorial can be done on its own but has been developed as a computer practical which demonstrates topics discussed in the lecture: **Reconciling gene tree - species tree discordance**, presented during the MSc course Phylogenetics in Ecology & Evolution at Potsdam University. This practical includes code snippets and examples from [Georgia Tsambos](https://github.com/gtsambos/2022-ts-workshops) and [Simon Martin](https://github.com/simonhmartin/tutorials/blob/master/topology_weighting/).

This computer practical is styled in a Jupyter Notebook (NB) format (see Github [README](https://github.com/MozesBlom/tutorials/tree/main) for more details). In short, Jupyter NBs contain either text cells (such as the current cell) in Markdown format or code cells (frequently) in Python3 format. The aim of this practical is not to provide an exhaustive introduction into Python/Markdown/Jupyter, but to provide an introduction into phylogenomic inference, how to account for genome wide variation in inheritance histories (coalescent variation) and what may cause such variation. Therefore, all code to run this practical is already in place and we will only make minor changes to the code itself to demonstrate the phylogenetic consequences of changing specific model parameters. In addition, there are several questions to be answered and you can double-click on the corresponding cells to enter your answer. Alternatively, you can just write them down for yourself.