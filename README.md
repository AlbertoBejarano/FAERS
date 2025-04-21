These Jupyter notebooks process FDA adverse event data for a set of drugs. It first retrieves data using an API and extracts relevant details about the types of adverse events
for each drug. The data is then aggregated, grouped by drug and event, and pivoted into a table format for further analysis. The notebook applies data scaling and dimensionality
reduction techniques, such as Principal Component Analysis (PCA), to standardize and reduce the dimensionality of the dataset. It uses clustering (Leiden algorithm) to group 
similar data points and explores the relationships between the drugs and their adverse events. Finally, the notebook visualizes the results using UMAP, providing insights into 
the patterns and associations between the drugs and the severity of their associated adverse events.
--          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --          --    
00_openFDA_UMAP_v01  
This script processes FDA adverse event data for a selected set of cancer drugs by retrieving records from the openFDA API. It fetches reports per drug in batches, extracting information
on adverse events and associated seriousness flags (e.g., death, hospitalization). The data is cleaned and standardized by capitalizing drug and event names, and a full list of unique
adverse events is saved to a text file. The script then aggregates and summarizes the data, computing total counts and percentages of each seriousness category per drug-event pair.
This normalized dataset allows for comparison of adverse event profiles across drugs. Finally, the processed data is saved as a CSV file.
