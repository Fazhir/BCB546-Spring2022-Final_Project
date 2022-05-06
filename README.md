# BCB546-Spring2022-Final_Project
Final Group Project

This repository has files and codes that were used to reproduce the ***Gene expression analysis of porcine whole blood cells infected with foot-and-mouth disease virus using high-throughput sequencing technology*** by Ding et al., 2018. `https://doi.org/10.1371/journal.pone.0200081`

We shared roles and responsibilities amongst ourselves and each member reproduced a particular figure in the paper
- Fig.1 was to be reproduced by `Ann Murithi`; but since we did not have data for gene expression of all the genes, it was non-reproducible. She used the available data to look at the ***Distribution of gene length*** and also looking at how it varried between the two major groups (The infected and Non-Infected)
- Fig.2 was reproduced by `Stephen Gray` but since we did not have sufficient data for that was used, the available data could only reproduce and annotate a few genes to her pathways on the Gene Ontology figure. He used Entrez to retrieve the pprovided GeneIDs.
- Fig.3 was reproduced by `Ceren Ordas` about ***KEGG annotation of differentially expressed genes*** but the paper did not mention theh software they used for this. She thus used pathfindR package in ShinyGO 0.76 web application and made the chart using RStudio
- Fig.4 was reproduced by `Fazhir Kayondo` (Me) about ***Relative expression levels of 10 randomly selected DEGs***
- Fig.5 was not reproduced due to lack of data regarding the IgG titers, but the available data was utilized by `Mercy Fakude` to produce a new figure for ***Quality scores across all bases*** and another one for ***Total GC content quality***

Downloading, inspection and description of the data used in this study
  The links to the data used were available in the `supplementary information` section of the paper
  Data relating to the particular segment of the paper to be reproduced was downloaded by each corresponding member on to their PC for further operations.
  I, personally utilized `https://journals.plos.org/plosone/article/file?type=supplementary&id=10.1371/journal.pone.0200081.s004` excel dataset that had the expression levels of the differentially expressed genes.
  My intention was to reproduce Figure 4; which was produced during the validation of 10 randomly selected genes that had been observed to be upregulated
  
 Rerunning analysis
- Figures produced by Ann
    The code used to produced the figures is a vailable in a markdown file on the Github repository [here](https://journals.plos.org/plosone/article/file?type=supplementary&id=10.1371/journal.pone.0200081.s004) for the 
    
  I performed all the tasks of manipulating the data and rerunning the analysis using R version 4.1.3
  The analysis involved; 
  - `Loading the packages`
  - `Importing and manipulating the dataset` into the R environment
  - `Randomly selecting 10 genes` for validation
  - `Assigning corresponding gene names` to the GeneIDs
  - `Visualizing the selected genes` using Plotly package of R 
  The code markdown file used for reproducing Fig.4 is in the repository named "Validation of gene expression"
  
A pdf showing all the figures created during the re-analysis by the group has been included in the repository named `Reproduced_figures`. These were created using different software packages in `RStudio` and `Python`
