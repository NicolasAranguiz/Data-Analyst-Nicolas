# Data-Driven Analytical Portfolio: Trends and Insights

# Parking Violations in Vancouver: Data Analysis Project

## 1. Exploratory Data Analysis (EDA)

**Project Title:**  
*Parking Violations in Vancouver: An Exploratory Data Analysis*

**Objective:**  
The primary goal of this project is to analyze the parking violations data from Vancouver, identifying which bylaws are most frequently violated and how these violations have changed year-over-year.

**Dataset:**  
The parking ticket dataset includes the following fields:
- **Block**: The block number where the violation occurred.
- **Street**: The name of the street where the parking violation took place.
- **EntryDate**: The date when the violation was recorded.
- **Bylaw**: The bylaw number corresponding to the violation.
- **Section**: The section of the bylaw that was violated.

**Methodology:**
1. **Data Collection and Preparation**:
   - The parking ticket data was stored in **AWS S3**, organized by year under the `Landing/` folder.
   - The data was cleaned using **AWS Glue DataBrew**, including handling missing values and correcting formats in columns such as "EntryDate" and "Bylaw."

2. **Descriptive Statistics**:
   - Using **AWS Athena**, SQL queries were executed to calculate summary statistics (e.g., the number of violations per bylaw, average violations per year).
   - Frequency distributions for each bylaw were computed, helping identify the most violated bylaws.

3. **Data Visualization**:
   - A PDF was generated from **Excel** to visually represent the trends of parking violations between 2020 and 2024.
   - The visualization highlights the number of parking tickets issued under different bylaws, revealing patterns over time.

4. **Insights and Findings**:
   - The analysis showed that **Bylaw 2952** (parking meters) consistently had the highest number of violations.
   - Violations were concentrated in downtown areas, with peak violation periods during weekdays.

**Tools and Technologies:**
- **AWS S3**: For data storage and organization.
- **AWS Glue DataBrew**: For cleaning and preparing the dataset.
- **AWS Athena**: For querying the dataset and generating descriptive statistics.
- **Excel**: For generating visualizations.

**Deliverables:**
- A cleaned dataset stored in **AWS S3**.
- A detailed analysis report with descriptive statistics and insights.
- A PDF report with visualizations of the parking violation trends by bylaw.

---

## 2. Descriptive Analysis

**Project Title:**  
*Descriptive Analysis of Parking Violations in Vancouver*

**Objective:**  
The purpose of this analysis is to summarize the parking ticket data in Vancouver and identify trends over the past five years, focusing on which bylaws were most frequently violated.

**Dataset:**  
The dataset includes parking ticket records from multiple years, detailing fields such as violation date, bylaw, and location.

**Methodology:**
1. **Data Storage and Preparation**:
   - The dataset was stored in **AWS S3**, organized under the `Processed/` folder for easy access.
   - The data was cleaned and standardized using **AWS Glue**, ensuring the consistency of important columns like "Bylaw" and "EntryDate."

2. **Statistical Summarization**:
   - **AWS Athena** was used to perform SQL queries that calculated statistics such as total violations per bylaw and the average number of tickets issued per year.
   - These statistics helped pinpoint the bylaws with the highest number of violations.

3. **Insights and Findings**:
   - The descriptive analysis revealed that **Bylaw 2952** accounted for the majority of parking violations, with downtown areas experiencing the highest violation rates.

**Tools and Technologies:**  
- **AWS S3**: For structured data storage.
- **AWS Glue**: For cleaning and preprocessing the dataset.
- **AWS Athena**: For querying the dataset and generating descriptive statistics.

**Deliverables:**
- A detailed report summarizing the number of parking violations by bylaw.
- Visualizations generated using **Excel** for better understanding of the trends.

---

## 3. Diagnostic Analysis

**Project Title:**  
*Diagnostic Analysis of Parking Violations in Vancouver: Identifying Causes of Violations*

**Objective:**  
To determine the factors driving parking violations in Vancouver, this analysis focuses on understanding the root causes behind the trends in the most violated bylaws and their geographic distribution.

**Dataset:**  
Parking ticket data categorized by bylaw, location, and year.

**Methodology:**
1. **Data Collection and Filtering**:
   - The dataset was uploaded to **AWS S3** and prepared for analysis using **AWS Glue**.
   - A filtering process was implemented to retain only valid violations (those marked as "Issued" in the status column).

2. **Correlation Analysis**:
   - **AWS Athena** was used to perform correlation analysis between bylaw violations and geographic factors (e.g., the number of violations per block).
   - The data was segmented by location to assess which regions had the highest concentration of violations.

3. **Insights and Findings**:
   - The analysis revealed that violations were primarily concentrated in commercial districts with high traffic, particularly during weekdays.
   - Changes in parking regulations, such as increased enforcement, had a measurable effect on reducing violations in some areas.

**Tools and Technologies:**  
- **AWS S3**: For data storage.
- **AWS Glue**: For data filtering and transformation.
- **AWS Athena**: For conducting correlation analysis.

**Deliverables:**
- A report detailing the root causes of parking violations.
- Visualizations showing correlations between geographic factors and violation trends.

---

## 4. Data Wrangling

**Project Title:**  
*Data Wrangling for Parking Violations in Vancouver*

**Objective:**  
To clean and prepare the parking violation data for further analysis by handling missing values, duplicates, and standardizing data formats.

**Dataset:**  
The raw dataset was sourced from the Vancouver Open Data Portal and included fields such as violation date, bylaw number, and block.

**Methodology:**
1. **Data Cleaning**:
   - The raw data was uploaded to **AWS S3**.
   - **AWS Glue DataBrew** was used to handle missing values, remove duplicate records, and standardize formats for key fields such as "EntryDate" and "Bylaw."

2. **Data Transformation**:
   - The cleaned dataset was transformed in **AWS Glue** to include additional features, such as aggregating the number of violations per block.
   - The processed data was stored in the `Processed/` folder in **AWS S3**.

3. **Validation**:
   - The cleaned dataset was validated to ensure no missing values or inconsistencies, making it ready for subsequent analysis.

**Tools and Technologies:**  
- **AWS S3**: For storing raw and processed datasets.
- **AWS Glue DataBrew**: For cleaning and handling missing values.
- **AWS Glue**: For transforming the dataset.

**Deliverables:**
- A cleaned dataset stored in **AWS S3**.
- Documentation of the data wrangling process.

---

## 5. Data Quality Control

**Project Title:**  
*Ensuring Data Quality in Parking Violations Analysis*

**Objective:**  
To ensure that the parking violation dataset is complete, accurate, and reliable, by applying data validation and quality control measures.

**Dataset:**  
The cleaned parking ticket dataset, categorized by bylaw and violation date.

**Methodology:**
1. **Data Profiling**:
   - **AWS Glue DataBrew** was used to profile the dataset and assess the quality of key fields (e.g., completeness and accuracy of "Bylaw" and "EntryDate" columns).

2. **Data Validation**:
   - Custom validation rules were created in **AWS Glue** to check for missing or duplicate data entries, ensuring the dataset was complete and error-free.

3. **Data Monitoring**:
   - **AWS CloudWatch** was used to monitor the data ingestion and processing steps, tracking the number of violations processed and the consistency of data updates.

**Tools and Technologies:**  
- **AWS Glue DataBrew**: For data profiling and validation.
- **AWS CloudWatch**: For monitoring data quality.

**Deliverables:**
- A data quality report outlining the validation steps and ensuring that the dataset meets quality standards.
- A clean, validated dataset ready for further analysis.
