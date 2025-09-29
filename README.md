# Genetic Variation and Geographic Correlation in European Populations

## Overview
This project was carried out as the final project in the *Mathematical Methods in Data Science and Signal Processing* course (M.Sc. program, Tel Aviv University).  

The objective was to replicate the algorithm from the paper *"Genes Mirror Geography within Europe"* (Novembre et al.) and apply it to a different dataset — the **1000 Genomes Project**.  
We focused on European populations and evaluated whether similar geographic-genetic patterns could be observed.

---

## Data
- Dataset: 1000 Genomes Project, chromosomes 22 and 1.  
- Selected populations: GBR (British), FIN (Finnish), IBS (Iberian in Spain), CEU (Utah residents of European ancestry), and TSI (Tuscans from Italy).  
- After filtering: 503 individuals.  
- Preprocessing: SNP pruning with **PLINK**, reducing chromosome 22 from 69,945 SNPs to 26,739 variants.  

---

## Methods
1. **Principal Component Analysis (PCA)** to identify main axes of genetic variation.  
2. **Axis rotation** to align PCs with latitude and longitude (optimal angle: 153.03° for chromosome 22).  
3. **Geographic prediction** using:  
   - Multiple linear regression from rotated PCs to latitude/longitude.  
   - Discrete assignment to the nearest country center.  
4. Comparison of results between chromosomes 22 and 1.  

---

## Results
- Unlike the original study, clear clustering by geography was not fully observed.  
- Finnish individuals appeared as the most distinct group, reflecting Finland’s geographic and genetic isolation.  
- Results on chromosome 1 confirmed the same trend observed on chromosome 22.  
- Main limitation: the 1000 Genomes dataset does not include information about participants’ grandparents’ origins, which reduced geographic accuracy.  

---

## Improvements and Future Work
- Use larger and more detailed datasets, including ancestry of grandparents.  
- Apply non-linear dimensionality reduction techniques (e.g., **t-SNE, UMAP**).  
- Incorporate clustering algorithms (e.g., **ADMIXTURE, GMM**) to capture finer structures.  
- Explore deep learning models for large-scale genomic inference.  

---

## Repository Structure
