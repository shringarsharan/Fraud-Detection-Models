## Unsupervised Machine Learning Fraud Model on NY Property Valuation Data using Python – January 2020
#### SUMMARY
• Built a property tax fraud detection model by computing fraud scores for each property in the dataset using two approaches \
• Analyzed >1 million records, 32 fields to build expert variables; PCA reduced dimensionality to 6 PCs, explaining 94% of variance \
• Trained Autoencoder on Z-scored PCA values and used Euclidian distance to rank order each record by two fraud scores 

#### BUSINESS PROBLEM
Property tax evasion and exemption fraud is a problem faced by every government in the world and can have huge implications. Increased instances of property tax fraud cost government agencies millions of dollars in lost revenues and drive taxes higher for communities at-large.

#### OBJECTIVE
The objective of this project is to identify fraudulent or anomalous properties in the New York Property and Valuation dataset, which has around 1 million records and 32 fields for properties spread across the city of New York. This project report elaborates the steps we took to accomplish this task. We built an unsupervised fraud detection model which would score each record in the dataset according to its likelihood of being anomalous. We employed tools such as Python and MS Excel to analyze the data.

#### PROJECT OVERVIEW
The following summarizes the steps entailed to analyze the data and build the fraud detection model:
1. **Data Cleaning**: This involved cleaning the data and imputing those records which have missing values and zero as values.
2. **Building Expert Variables/Feature Engineering**: We built expert variables and standardized the data before inputting them into model.
3. **Dimensionality Reduction**: We employed the Principal Component Analysis (PCA) to reduce the dimensions in the data. At the end of this step, we retained 6 Principal Components which explained around 94% of variance in the data.
4. **Fraud Algorithms and Calculating Fraud Scores**: The two approaches used to compute the individual Fraud Scores are described as follows:\
• Using Heuristic Function to calculate z-score\
• Using Autoencoder to reproduce the data that we input after reducing
dimensionality. The reproduction error is taken as a measure of anomaly. We used
Euclidean distance in this case.
5. **Computing Final Fraud Score**: The scores from the above methods were used
individually to rank order the records in order of their likelihood of being fraudulent or anomalous. The final score was computed by taking the average of the rank orders obtained from the two methods described above.

In conclusion, we identified the top 10 anomalous records in the NY property dataset using the above process of anomaly detection. These records were analyzed in great detail to elicit insightful information regarding the anomalous records and provide recommendations for future work.
