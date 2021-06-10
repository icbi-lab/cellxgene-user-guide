# Cell-x-gene user guide

[cell-x-gene](https://chanzuckerberg.github.io/cellxgene/) is a single-cell visualization platform
developed by the [Chan-Zuckerberg initative](https://chanzuckerberg.com/). It allows
to explore single-cell RNA-seq (scRNA-seq) datasets in the web browser without any 
computational skills. This guide gives an overview of the most important features. 

## Table of Contents

- [Cell-x-gene user guide](#cell-x-gene-user-guide)
	- [Table of Contents](#table-of-contents)
	- [Portal overview](#portal-overview)
	- [How to color by categorical variables (cell-type, patient, etc.)](#how-to-color-by-categorical-variables-cell-type-patient-etc)
	- [How to color by gene](#how-to-color-by-gene)
	- [How to change the embedding](#how-to-change-the-embedding)
	- [How to analyse a subset of data (e.g. specific cell-type or patient)](#how-to-analyse-a-subset-of-data-eg-specific-cell-type-or-patient)
	- [How to perform differential gene expression analysis](#how-to-perform-differential-gene-expression-analysis)

## Portal overview

![picture 1](images/7d0ab9571c89054e98bf0db12d72330c241314b802c4ea066f7f76405164eb14.png)  

The portal consists of three main panels: 

 * the left sidebar for *categorical annotations*, such as patient, cell-type, ...
 * the main panel, visualizing a *embedding* of the single-cells (usually [UMAP](https://www.nature.com/articles/nbt.4314)). 
 * the right sidebar for *continuous variables*, such as genes. 

Additionally, there are two toolbars: 
 * The "main toolbar" at the right top
 * the "embedding toolbar" at the bottom left.


## How to color by categorical variables (cell-type, patient, etc.)

In the left sidebar, click on the drop next to a variable. 
If you open another category ("patient" in the example), you'll see colorbars
indicating the distribution of the category. 

![picture 11](images/1425c5eb6c357e641b2f5f017d45279ce607a49fef5af185111781519f3535e4.png)  

For some variables (cluster, cell-type) it makes sense to overlay the 
legend on the cell-type plot. To activate this feature, click on the "show labels" 
button in the toolbar: 

![picture 5](images/d83053b207ffd6f1232e53d87f837c73eb36916373811067d8382d82288b5993.png)  


## How to color by gene

In the right sidebar, enter a gene in the "Search" bar. 

![picture 6](images/fa6aff7013f0e10bb10737cc2b0f7fd366f0ddddade89cad1d02e04b60917f7f.png)  

This will add a histogram to the right sidebar. Click on the drop to color the 
single-cell plot by the gene expression: 

![picture 12](images/7ef58795d133f1bce4a24563751706655ee15ebcec142e434a2f7b0050717040.png)  


## How to change the embedding

For some datasets, we provide multiple embeddings (usually, that is a UMAP with and
without batch correction, respectively). You can choose the embedding from the
"embedding toolbar" at the bottom left: 

![picture 8](images/860c4e70c7fc1d6964c9c233189195d3eb25122d2563daf81b0dd36869a1d0bb.png)  


## How to analyse a subset of data (e.g. specific cell-type or patient)

There are different ways to select cells in cell-x-gene:

1. By selecting categories in the left sidebar
2. Using drag & drop on the plot
3. By selecting a range in the right sidebar (drag & drop on a histogram)


Once you selected cells, you remove all other cells from the plot by clicking on the 
"Subset" button in the toolbar: 

![picture 9](images/8ce702773a18ed5facc53a38175fd5a27946d18d206fd96f94987f8f1c722f49.png)  

Once you subset the dataset, all cell-counts, colorbars and histograms adapt to 
reflect the reduced dataset. 

To reset the view to include all cells, use the "Undo subset" button. You can also 
undo a single step by using the "undo" button: 

![picture 10](images/04566a9824c467df83c89cea7904b3de5266e0466e9ed3035826c664c6faa874.png)  



## How to perform differential gene expression analysis

With cell-x-gene it is possible to perform a very simple differential gene expression 
(DE)-analysis. It does not correct for any biases and only shows the top 10 most 
differentially expressed genes. This is great for a first glance at the data - if you 
need a more in-depth analysis, contact your Bioinformaticians. 

Once you [selected a group of cells](#how-to-analyse-a-subset-of-data-eg-specific-cell-type-or-patient), 
you can assign these cells to either *group 1* or *group 2* by clicking the buttons
in the toolbar: 

![picture 15](images/cdfcca79e4eb82a0d1e989dac0573dea135147ff7732635cd30f551c93a35ff7.png)  

Once you have both groups filled with cells, you can perform the DE-analysis by clicking
on the "Differential expression" button: 

![picture 16](images/438967e5495cc13d24c6ee6e177be55a71db05b19ffa08016812fbeaa43cc161.png)  

The 10 top DE genes will now appear in the right sidebar. 