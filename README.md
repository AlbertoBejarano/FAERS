
  These Jupyter notebooks process FDA adverse event data for a set of drugs. It first retrieves data using an API and extracts relevant details about the types of adverse events
for each drug. The data is then aggregated, grouped by drug and event, and pivoted into a table format for further analysis. The notebook applies data scaling and dimensionality
reduction techniques, such as Principal Component Analysis (PCA), to standardize and reduce the dimensionality of the dataset. It uses clustering (Leiden algorithm) to group 
similar data points and explores the relationships between the drugs and their adverse events. Finally, the notebook visualizes the results using UMAP, providing insights into 
the patterns and associations between the drugs and the severity of their associated adverse events.
--          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --    
  **00_openFDA_UMAP_v01**  
This script processes FDA adverse event data for a selected set of cancer drugs by retrieving records from the openFDA API. It fetches reports per drug in batches, extracting information
on adverse events and associated seriousness flags (e.g., death, hospitalization). The data is cleaned and standardized by capitalizing drug and event names, and a full list of unique
adverse events is saved to a text file. The script then aggregates and summarizes the data, computing total counts and percentages of each seriousness category per drug-event pair.
This normalized dataset allows for comparison of adverse event profiles across drugs. Finally, the processed data is saved as a CSV file.
--          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --    
  **01_openFDA_UMAP_v01**  
This notebook processes FDA adverse event data by merging standard-of-care and drug-specific reports, focusing on serious outcomes like LifeThreatening events.
It transforms the data into a drug-by-event matrix and applies PCA for dimensionality reduction, followed by Leiden clustering to identify groups of drugs with similar adverse event profiles. 
UMAP is then computed across a grid of `min_dist` and `spread` values to visualize the structure of the data, and drug labels are overlaid on the final UMAP for interpretation.
The visualization highlights distinct AE patterns across drugs, providing insights into safety-related clustering.
--          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          -- 
  **02_openFDA_UMAP_v01**  
This notebook analyzes FDA adverse event (AE) data for both standard-of-care (SoC) and investigational drugs, with a focus on serious events such as LifeThreatening cases. 
It retrieves, merges, and reshapes the data into a structured drug-by-event matrix, scales the values, and reduces dimensionality using PCA. 
The Leiden algorithm is applied across multiple resolutions to detect clusters of drugs with similar AE profiles. UMAP is then computed using different `min_dist` and `spread` 
values to visualize these clusters in 2D space. The results help identify AE-driven groupings of drugs and visualize how their safety profiles relate to each other.
--          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          -- 
  **03_openFDA_UMAP_v01**  
This JupyterLab cell processes and visualizes FDA adverse event data for drugs by applying dimensionality reduction and clustering techniques. It first merges two datasets—one for
standard-of-care drugs and one for experimental drugs—then pivots the data to create a matrix of adverse event severities. Using Scanpy, the data is standardized and reduced via PCA,
followed by Leiden clustering to group drugs with similar adverse event profiles. UMAP is used to generate a 2D embedding of the data, exploring multiple combinations of `min_dist`
and `spread` parameters to visualize cluster separation. The final plots show UMAP projections colored by drug name, data source, and Leiden cluster, helping identify drug-specific
and cluster-level patterns in adverse event profiles.
--          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          -- 
  **03_openFDA_UMAP_v02**
This JupyterLab cell processes and visualizes FDA adverse event data for drugs by applying dimensionality reduction and clustering techniques. It first merges two datasets—one for
standard-of-care drugs and one for experimental drugs—then pivots the data to create a matrix of adverse event severities. Using Scanpy, the data is standardized and reduced via PCA,
followed by Leiden clustering to group drugs with similar adverse event profiles.  Data is transformed into a numerical matrix and processed using PCA and Leiden clustering.
UMAP is applied for dimensionality reduction and visualization. Multiple UMAP parameter combinations are explored, and final plots are generated, coloring points by drug name, 
data source, and cluster assignment to uncover patterns and relationships among drug safety profiles.

--          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          -- 

  
Standard of Care Drugs for the 10 Most Common Cancers
------------------------------------------------------

1. Breast Cancer
   - Hormonal: Tamoxifen, Letrozole, Anastrozole, Exemestane
   - CDK4/6 Inhibitors: Palbociclib, Ribociclib, Abemaciclib
   - HER2+: Trastuzumab, Pertuzumab, T-DM1, T-DXd (Enhertu)
   - Chemotherapy: Paclitaxel, Carboplatin
   - Immunotherapy (TNBC): Pembrolizumab, Atezolizumab

2. Lung Cancer (NSCLC & SCLC)
   - Targeted: Osimertinib (EGFR), Alectinib, Lorlatinib (ALK)
   - Chemotherapy: Carboplatin, Cisplatin, Pemetrexed, Paclitaxel, Etoposide
   - Immunotherapy: Pembrolizumab, Atezolizumab, Durvalumab

3. Colorectal Cancer
   - Chemotherapy: 5-FU, Leucovorin, Oxaliplatin, Irinotecan
   - Targeted: Cetuximab, Panitumumab (RAS wild-type), Bevacizumab

4. Prostate Cancer
   - Hormonal: Leuprolide, Goserelin, Abiraterone, Enzalutamide, Apalutamide
   - Chemotherapy (CRPC): Docetaxel, Cabazitaxel

5. Stomach (Gastric) Cancer
   - Chemotherapy: 5-FU, Cisplatin, Oxaliplatin, Capecitabine
   - HER2+: Trastuzumab
   - Immunotherapy (PD-L1+): Nivolumab

6. Liver Cancer (Hepatocellular Carcinoma)
   - Immunotherapy + Anti-VEGF: Atezolizumab + Bevacizumab
   - Other Targeted: Sorafenib, Lenvatinib, Regorafenib, Cabozantinib

7. Cervical Cancer
   - Chemotherapy: Cisplatin, Paclitaxel
   - Targeted: Bevacizumab
   - Immunotherapy (PD-L1+): Pembrolizumab

8. Esophageal Cancer
   - Chemotherapy: 5-FU, Cisplatin, Paclitaxel, Carboplatin
   - Immunotherapy (PD-L1+ or adjuvant): Nivolumab

9. Thyroid Cancer
   - RAI-sensitive: Radioactive iodine, Levothyroxine
   - RAI-refractory: Lenvatinib, Sorafenib
   - Medullary: Vandetanib, Cabozantinib
   - Anaplastic (BRAF+): Dabrafenib + Trametinib

10. Bladder Cancer
    - Chemotherapy: Cisplatin + Gemcitabine
    - Immunotherapy (advanced): Atezolizumab, Nivolumab
    - ADC: Enfortumab Vedotin
