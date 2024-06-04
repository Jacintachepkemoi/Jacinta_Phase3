# Jacinta_Phase3

Data Preparation
To address the issue of missing data in the H1N1 Flu Vaccines dataset, I developed a Python class called DataChecker that systematically handles various data preprocessing tasks. The initial steps involved loading the dataset and identifying missing values and duplicate rows. To clean the dataset, I implemented a method to drop specific columns that had a high percentage of missing values, as these columns (namely health_insurance, employment_industry, and employment_occupation) were not deemed essential for analysis.

For the remaining missing data, I took a two-pronged approach. First, I targeted the numeric columns by calculating the mean of each column and replacing the missing values with these means. This approach ensures that the numeric integrity of the data is maintained without introducing biases. For non-numeric columns, I replaced the missing values with the mode, which is the most frequently occurring value in each column. This method preserves the categorical nature of these columns and maintains the consistency of the data.

The DataChecker class included methods for these tasks, ensuring a modular and reusable code structure. After processing, I verified that the dataset had no remaining missing values, achieving a complete and clean dataset ready for further analysis. This comprehensive approach allowed for efficient data preprocessing, handling both numeric and categorical missing values appropriately, thus ensuring the integrity and usability of the dataset for subsequent analyses.
Data Analsis
