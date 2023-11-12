### RESYS project 2023
DELOUIS Maëlys, REY Soraya
This project was realised in the context of the unit RESYS 
from Biocomputing and Modelisation master 2
Sorbonne Université

## Requirements
Python version 3.10 
> Python librairies:
> pandas, numpy, os

R version 4.3.2
> R libraries:
> Seurat, GENIE3, igraph, ggplot2, stringr, vegan, Rgraphviz, doParallel, doRNG,
> Matrix, qgraph, minet, Biocmanager, dplyr, bnlearn

MIIC.curie (https://miic.curie.fr/)

RStudio

## Launch
To launch project code, change input files path in R files (in file_names)
Executed in RStudio and VsCode.

## Content
The following directories and files are provided:
> Report.pdf: a report of the project with bibliography

> ./data: project datas (the original matrix was too large and can be found here https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE131907)
>> ./Epithelial_cells:  preprocessed csv for each stage as splited data for Normal and Tumoral lung at each stage could not be provided (too large)
>> cell_data_simplified.csv: metadata from original dataset

> ./source_code: code in R and Python
>> cell_type_separator.py, data_process.py: scripts for spliting original matrix with metadatas
>> preprocessing.R: Seurat R pipeline for normalizing datas and creating datasets for each stage from Normal and Tumoral data for network building algorithms 
>> network_building: from preprocessed files, construct GENIE3 and ARACNE networks
>> analysis.R: creates centrality distribution from networks matrix and finds main genes
>> centrality.R: for MIIC matrixes (obtained online) confronts centrality and connection to class vertex to find central genes in network

> ./results: GENIE3, ARACNE and MIIC networks matrixes, ARACNE and GENIE3 networks visualisations at each stage, distributions of centrality
