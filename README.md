# Overview

Nodular lymphocyte-predominant Hodgkin lymphoma (NLPHL) is a rare disease with few comprehensive studies investigating its microenvironment. We performed the largest study to date analyzing tissue samples from 171 patients. 
We utilized the machine learning framework EcoTyper to identify 34 distinct cell states across 14 cell types. We found evidence of CD8 T-cell exhaustion, M2 polarized macrophages, immune checkpoint genes expressed by follicular T-cells, and three distinct LP cell states. These distinct cell states co-occur in 3 lymphocyte-predominant EcoTypes (LPEs) with LPE3 portending worse freedom from progression in the training (n=109) and validation cohorts (n=62) after multivariable adjustment for the lymphocyte-predominant-international prognostic score. Using spatial transcriptomics, we validate the co-occurrence and co-localization of these cell states. 

# Setup

First start by cloining the latest version of EcoTyper source code from either the EcoTyper Github Repository or the EcoTyper website:
```
git clone https://github.com/digitalcytometry/ecotyper
cd ecotyper
```
or:
```
wget https://github.com/digitalcytometry/ecotyper/archive/refs/heads/master.zip
unzip master.zip
cd ecotyper-master
```

From within the "EcoTyper" folder that has been created, you can add the "LPEcoTyper" github from this repository by following these commands:
```
cd EcoTyper
git init
git remote add -f origin https://github.com/msbinkley/LPEcoTyper
git config core.sparseCheckout true
echo 'NLPHL' >> .git/info/sparse-checkout
git pull origin master
cd ..
```

To run recovery of cell states and ecotypes in user-provided data (bulk RNA sequencing, single cell RNA sequencing, or spatial transcriptomics), refer to the instructions provided on the EcoTyper GitHub repository
