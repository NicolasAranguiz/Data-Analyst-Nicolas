# Data-Analyst-Nicolas
# Parking Violations in Vancouver: Data Analysis Project

## 1. Exploratory Data Analysis (EDA)

**Project Title:**  
*Parking Violations in Vancouver: An Exploratory Data Analysis*

**Objective:**  
The primary goal of this EDA is to analyze the parking ticket violations in Vancouver to understand trends, such as which bylaws are most frequently violated and how these violations are distributed across the city and over time.

**Dataset:**  
The dataset contains parking ticket information from Vancouver, including violation dates, bylaw numbers, and geographic data (street and block details).

**Methodology:**
1. **Step 1:** The parking ticket data was uploaded to **AWS S3**, where it was organized by year in the `Landing/` folder.
2. **Step 2:** Data ingestion was performed using **AWS Glue** to load the data from S3 for cleaning and transformation.
3. **Step 3:** Basic data cleaning was done using **AWS Glue DataBrew**, including handling missing values and standardizing column formats.
4. **Step 4:** Initial exploratory analysis was performed on the cleaned data, focusing on identifying high-frequency violations, the most violated bylaws, and violation trends over time using **AWS Athena** for queries on the dataset stored in S3.
5. **Step 5:** Visualizations were created using **Amazon QuickSight** to generate heatmaps and bar charts that display the distribution of violations across Vancouver.

**Tools and Technologies:**  
- **AWS S3**: Storage of raw and processed data.
- **AWS Glue DataBrew**: For data cleaning and preprocessing.
- **AWS Athena**: For running SQL queries on the dataset.
- **Amazon QuickSight**: For visualizing data trends.

**Deliverables:**  
- Heatmaps displaying geographic patterns of parking violations.
- Bar charts showing the frequency of bylaw violations.

---

## 2. Descriptive Analysis

**Project Title:**  
*Understanding Parking Violation Trends in Vancouver: A Descriptive Analysis*

**Objective:**  
This section focuses on summarizing the data to provide an overview of the most common violations, including the total number of violations per bylaw and year-over-year changes.

**Dataset:**  
Parking ticket data categorized by bylaw and geographic location over several years.

**Methodology:**
1. **Step 1:** Data storage was managed using **AWS S3**, organized by year in the `Processed/` folder after the data wrangling step.
2. **Step 2:** Descriptive statistics, such as the average number of violations per bylaw and total violations per year, were calculated using **AWS Athena** queries.
3. **Step 3:** The analysis results were stored in the `Analytics/` folder on S3.
4. **Step 4:** **Amazon QuickSight** was used to generate bar charts that summarized the total number of violations for each bylaw.

**Tools and Technologies:**  
- **AWS S3**: For structured data storage.
- **AWS Athena**: For querying and calculating summary statistics.
- **Amazon QuickSight**: For generating visual reports on the analysis results.

**Deliverables:**  
- Summary report on the most violated bylaws.
- Bar charts showing total violations per year.

---

## 3. Diagnostic Analysis

**Project Title:**  
*Diagnostic Analysis of Parking Violations in Vancouver: Investigating Contributing Factors*

**Objective:**  
To determine the underlying reasons for observed trends in parking violations, such as why certain bylaws are more frequently violated and how changes in enforcement may have influenced these trends.

**Dataset:**  
Historical parking ticket data from 2020-2024, including violation dates, bylaw numbers, and enforcement information.

**Methodology:**
1. **Step 1:** All relevant datasets were stored in **AWS S3** under the `Processed/` folder.
2. **Step 2:** Data analysis was performed using **AWS Glue** for aggregating violation counts by year and bylaw.
3. **Step 3:** Correlation analysis was carried out using **AWS Athena** to explore relationships between geographic locations and violation frequency.
4. **Step 4:** **Amazon QuickSight** was used to visualize the correlation between enforcement changes and violation rates.

**Tools and Technologies:**  
- **AWS S3**: For storing and organizing processed datasets.
- **AWS Glue**: For performing data transformations.
- **AWS Athena**: For correlation analysis.
- **Amazon QuickSight**: For visualizing diagnostic results.

**Deliverables:**  
- Correlation heatmaps showing relationships between bylaw violations and enforcement changes.
- Geographic visualizations showing high-violation areas.

---

## 4. Data Wrangling

**Project Title:**  
*Data Wrangling for Parking Violations: Preparing Data for Analysis*

**Objective:**  
To clean and transform the raw parking ticket data, ensuring that it is structured and ready for analysis.

**Dataset:**  
Raw parking ticket data from Vancouver’s Open Data Portal, with key fields such as violation dates, bylaw numbers, and geographic details.

**Methodology:**
1. **Step 1:** The raw data was uploaded to **AWS S3** and organized by year in the `Landing/` folder.
2. **Step 2:** **AWS Glue DataBrew** was used to clean the data by removing duplicate records, handling missing values, and standardizing formats.
3. **Step 3:** The cleaned data was then stored in the `Processed/` folder on S3.
4. **Step 4:** The data was validated using **AWS Glue** to ensure it met accuracy and consistency requirements.

**Tools and Technologies:**  
- **AWS S3**: For storing raw and processed data.
- **AWS Glue DataBrew**: For data cleaning and transformation.
- **AWS Glue**: For further data validation.

**Deliverables:**  
- A cleaned dataset, free from missing or duplicate values.
- Documentation of the cleaning and transformation steps.

---

## 5. Data Quality Control

**Project Title:**  
*Ensuring Data Quality for Parking Violations: A Data Quality Control Approach*

**Objective:**  
To ensure that the data is accurate, complete, and consistent by applying quality control measures during the analysis process.

**Dataset:**  
Processed parking ticket data, including bylaw numbers, violation dates, and locations.

**Methodology:**
1. **Step 1:** Data quality was assessed using **AWS Glue DataBrew**, which checked for missing values, duplicate rows, and invalid bylaw codes.
2. **Step 2:** Validation rules were set in **AWS Glue** to ensure that only valid parking violations were included.
3. **Step 3:** **AWS CloudWatch** was used to monitor the data quality metrics in real-time.
4. **Step 4:** An **AWS IAM** policy was implemented to control access to sensitive data.

**Tools and Technologies:**  
- **AWS Glue DataBrew**: For checking and validating data quality.
- **AWS CloudWatch**: For monitoring real-time data quality metrics.
- **AWS IAM**: For managing access control.

**Deliverables:**  
- A final report on data quality, including checks for missing or inaccurate data.
- A validated dataset ready for further analysis.
