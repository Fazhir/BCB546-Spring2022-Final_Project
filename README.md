# BCB546-Spring2022-Final_Project
Final Group Project

This repository has files and codes that were used to reproduce some figures in the [paper](https://doi.org/10.1371/journal.pone.0200081) entitled ***"Gene expression analysis of porcine whole blood cells infected with foot-and-mouth disease virus using high-throughput sequencing technology"*** by Ding et al., 2018. 

We shared roles and responsibilities amongst ourselves and each member reproduced a particular figure in the paper
- Fig.1 was to be reproduced by `Ann Murithi`; but since we did not have data for gene expression of all the genes, it was non-reproducible. She used the available data to look at the ***Distribution of gene length*** and also looking at how it varried between the two major groups (The infected and Non-Infected)
- Fig.2 was reproduced by `Stephen Gray` but since we did not have sufficient data that was used, the available data could only reproduce and annotate a few genes to the pathways on the Gene Ontology figure. He used Entrez to retrieve the provided GeneIDs.
- Fig.3 was reproduced by `Ceren Ordas` about ***KEGG annotation of differentially expressed genes*** but the paper did not mention the software they used for this. She thus used `pathfindR` package in ShinyGO 0.76 web application and made the chart using RStudio
- Fig.4 was reproduced by `Fazhir Kayondo` (Me) about ***Relative expression levels of 10 randomly selected DEGs***
- Fig.5 was not reproduced due to lack of data regarding the IgG titers, but the available data was utilized by `Mercy Fakude` to produce new figures for ***Quality scores across all bases*** and another one for ***Total GC content quality***

Downloading, inspection and description of the data used in this study
  The links to the data used were available in the `supplementary information` section of the paper
  Data relating to the particular segment of the paper to be reproduced was downloaded by each corresponding member on to their PC for further operations.
  I, personally utilized [Excel dataset](https://journals.plos.org/plosone/article/file?type=supplementary&id=10.1371/journal.pone.0200081.s004) that had the expression levels of the differentially expressed genes.
  My intention was to reproduce Figure 4; which was produced during the validation of 10 randomly selected genes that had been observed to be upregulated
  
 ***Rerunning analysis***
 
 -- All codes used are in the [Github repository](https://github.com/Fazhir/BCB546-Spring2022-Final_Project)
 
 -- Uniprot Gene names retrieved using the provided ENSMBL gene IDs are in the Excel file named `ID_identify_uniprot.xlsx`
 
 -- The repository also has the .ppt presentation of the work done by the group; named `Final Group Project Presentation.ppt`
  
- ***Rerun by Ann Murithi:***

The code used is named `End of semester project.ipynb`. She intended to look at the distribution of the gene length amongst the DEGs. She also went further to look at this distribution across the two groups (NI and I) in order to see if a particular size of the gene is observed more in a specific group of infection status.
    
- ***Rerun by Mercy Fakude:***

The code used to produce the different figures for the quality of the trimmed data are available on Github. She intended to examine the Q-score of the bases in the sequence data across the different quality thresholds set by the authors of this paper (Q10, Q20 and Q30). She also looked at the GC content of the RNAseq data trimmed at the three different thresholds.
    
- ***Rerun by Stephen Gray:***

Gray tried to rerun the Gene Ontology functional classification of the DEGs by extracting the corresponding gene names and their functions from the Entrez database using the ENSMBL gene IDs provided. He then characterized the genes by a Functional term within three domains; `Molecular`, `Cellular` or `Biological` function using DAVID. Returned gene clusters are in a text file named `DEGs_clustering.txt` in the Github repository. The code used to recreate these is named `Gene_Ontology_RMarkdown.Rmd`
 
- ***Rerun by Ceren Ordas:***

Ceren was tasked with reproducing the KEGG enrichment analysis performed in the paper intended to identify the different enrinched pathways amongst the DEGs. The challenge was that the paper never mentioned the particular software used to produce their chart. She resorted to using `ShinyGO 0.76 Web application` but this could produce contradicting results corresponding to the gene IDs provided. 
    
- ***Rerun by Fazhir Kayondo (Me):***

I was tasked with recreating the graph for validation of gene expression for 10 randomly selected genes. The code used for reproducing Fig.4 is an RMarkdown file in the Github repository named `Validation of gene expression`. I performed all the tasks of manipulating the data and rerunning the analysis using R version 4.1.3.
The analysis involved; 
  - `Loading the packages`
  - `Importing and manipulating the dataset` into the R environment
  - `Randomly selecting 10 genes` for validation
  - `Assigning corresponding gene names` to the GeneIDs
  - `Visualizing the selected genes` using Plotly package of R 
    
A pdf showing all the figures created during the re-analysis by the group and compairing with the figures present in the paper has been included in the repository named. It has been named `Figures compared`. These were created using different software packages in `RStudio` and `Python`
