# Data-Analyst-Nicolas
1. Exploratory Data Analysis (EDA)
Project Title:
"Parking Violations in Vancouver: An Exploratory Data Analysis"

Objective:
The primary goal of this EDA is to analyze the parking ticket violations in Vancouver to understand trends, such as which bylaws are most frequently violated and how these violations are distributed across the city and over time.

Dataset:
The dataset contains parking ticket information from Vancouver, including violation dates, bylaw numbers, and geographic data (street and block details).

Methodology:

Step 1: The parking ticket data was uploaded to AWS S3, where it was organized by year in the "Landing/" folder.
Step 2: Data ingestion was performed using AWS Glue to load the data from S3 for cleaning and transformation.
Step 3: Basic data cleaning was done using AWS Glue DataBrew, including handling missing values and standardizing column formats.
Step 4: Initial exploratory analysis was performed on the cleaned data, focusing on identifying high-frequency violations, the most violated bylaws, and violation trends over time using AWS Athena for queries on the dataset stored in S3.
Step 5: Visualizations were created using Amazon QuickSight to generate heatmaps and bar charts that display the distribution of violations across Vancouver.
Tools and Technologies:

AWS S3: Storage of raw and processed data.
AWS Glue DataBrew: For data cleaning and preprocessing.
AWS Athena: For running SQL queries on the dataset.
Amazon QuickSight: For visualizing data trends.
Deliverables:

Heatmaps displaying geographic patterns of parking violations.
Bar charts showing the frequency of bylaw violations.
Image to Add:
Use the visualization from Step 12: Data Visualization, which was created using Excel but can be replaced with an Amazon QuickSight dashboard showcasing parking ticket trends from 2020-2024.

2. Descriptive Analysis
Project Title:
"Understanding Parking Violation Trends in Vancouver: A Descriptive Analysis"

Objective:
This section focuses on summarizing the data to provide an overview of the most common violations, including the total number of violations per bylaw and year-over-year changes.

Dataset:
Parking ticket data categorized by bylaw and geographic location over several years.

Methodology:

Step 1: Data storage was managed using AWS S3, organized by year in the "Processed/" folder after the data wrangling step.
Step 2: Descriptive statistics, such as the average number of violations per bylaw and total violations per year, were calculated using AWS Athena queries.
Step 3: The analysis results were stored in the Analytics/ folder on S3, allowing for easy access to the computed statistics.
Step 4: Amazon QuickSight was used to generate bar charts that summarized the total number of violations for each bylaw.
Tools and Technologies:

AWS S3: For structured data storage.
AWS Athena: For querying and calculating summary statistics.
Amazon QuickSight: For generating visual reports on the analysis results.
Deliverables:

Summary report on the most violated bylaws.
Bar charts showing total violations per year.
Image to Add:
The image from Step 11: Data Analysis can be used here. It shows the analysis of bylaw violations across years, highlighting significant trends in bylaws 2952 and 2849.

3. Diagnostic Analysis
Project Title:
"Diagnostic Analysis of Parking Violations in Vancouver: Investigating Contributing Factors"

Objective:
To determine the underlying reasons for observed trends in parking violations, such as why certain bylaws are more frequently violated and how changes in enforcement may have influenced these trends.

Dataset:
Historical parking ticket data from 2020-2024, including violation dates, bylaw numbers, and enforcement information.

Methodology:

Step 1: All relevant datasets were stored in AWS S3 under the "Processed/" folder.
Step 2: Data analysis was performed using AWS Glue to handle complex transformations such as aggregating violation counts by year and bylaw.
Step 3: Correlation analysis was carried out using AWS Athena to explore relationships between geographic locations and violation frequency.
Step 4: Amazon QuickSight was used to visualize the correlation between enforcement changes and violation rates, as well as geographic hot spots for violations.
Tools and Technologies:

AWS S3: For storing and organizing processed datasets.
AWS Glue: For performing data transformations.
AWS Athena: For correlation analysis.
Amazon QuickSight: For visualizing diagnostic results.
Deliverables:

Correlation heatmaps showing relationships between bylaw violations and enforcement changes.
Geographic visualizations showing high-violation areas.
Image to Add:
The image from Step 9: Data Structuring showing the process of filtering and grouping the data by bylaw for analysis.

4. Data Wrangling
Project Title:
"Data Wrangling for Parking Violations: Preparing Data for Analysis"

Objective:
To clean and transform the raw parking ticket data, ensuring that it is structured and ready for analysis.

Dataset:
Raw parking ticket data from Vancouver’s Open Data Portal, with key fields such as violation dates, bylaw numbers, and geographic details.

Methodology:

Step 1: The raw data was uploaded to AWS S3 and organized by year in the "Landing/" folder.
Step 2: AWS Glue DataBrew was used to clean the data by removing duplicate records, handling missing values, and standardizing the formats for violation dates and bylaw numbers.
Step 3: The cleaned data was then stored in the "Processed/" folder on S3, ready for analysis.
Step 4: The data was validated using AWS Glue to ensure it met the project’s requirements for accuracy and consistency.
Tools and Technologies:

AWS S3: For storing raw and processed data.
AWS Glue DataBrew: For data cleaning and transformation.
AWS Glue: For further data validation.
Deliverables:

A cleaned dataset, free from missing or duplicate values.
Documentation of the cleaning and transformation steps.
Image to Add:
Include the image from Step 8: Data Cleaning using AWS Glue DataBrew, which shows the data quality checks performed.

5. Data Quality Control
Project Title:
"Ensuring Data Quality for Parking Violations: A Data Quality Control Approach"

Objective:
To ensure that the data is accurate, complete, and consistent by applying quality control measures during the analysis process.

Dataset:
Processed parking ticket data, including bylaw numbers, violation dates, and locations.

Methodology:

Step 1: Data quality was assessed using AWS Glue DataBrew, which checked for missing values, duplicate rows, and invalid bylaw codes.
Step 2: Validation rules were set in AWS Glue to ensure that only valid parking violations were included in the final dataset.
Step 3: AWS CloudWatch was used to monitor the data quality metrics in real-time, such as the completeness and accuracy of the data.
Step 4: An AWS IAM policy was implemented to control access to the data, ensuring that only authorized users could access sensitive information.
Tools and Technologies:

AWS Glue DataBrew: For checking and validating data quality.
AWS CloudWatch: For monitoring real-time data quality metrics.
AWS IAM: For managing access control to ensure data security.
Deliverables:

A final report on data quality, including checks for missing or inaccurate data.
A validated dataset ready for further analysis or reporting.
Image to Add:
Use the image from Step 16: Data Quality Control, showing the rules applied in AWS Glue to ensure the dataset's integrity and quality.

