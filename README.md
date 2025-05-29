
  These Jupyter notebooks process FDA adverse event data for a set of drugs. It first retrieves data using an API and extracts relevant details about the types of adverse events
for each drug. The data is then aggregated, grouped by drug and event, and pivoted into a table format for further analysis. The notebook applies data scaling and dimensionality
reduction techniques, such as Principal Component Analysis (PCA), to standardize and reduce the dimensionality of the dataset. It uses clustering (Leiden algorithm) to group 
similar data points and explores the relationships between the drugs and their adverse events. Finally, the notebook visualizes the results using UMAP, providing insights into 
the patterns and associations between the drugs and the severity of their associated adverse events.
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
