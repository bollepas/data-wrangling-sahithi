# Data Wrangling for Enhanced Analytics

## Project Description
Data Wrangling for the City of Vancouver's Capital Project Budget Data

## Project Title
Enhanced Data Wrangling for Comprehensive Analysis

## Objective
The primary goal of this project is to perform comprehensive data wrangling to prepare a robust dataset for analysis and reporting. By cleaning, transforming, and consolidating data from various sources, the project ensures accuracy and usability for further analytical processes.

## Dataset
The data includes:
- Budget requests for multi-year capital projects
- Historical expenditure data
- Service categories like "Public Safety," "Parks and Public Open Spaces," and "One Water"
- Additional metadata from the City of Vancouver’s open data portal

## Methodology
### 1. Data Ingestion
- Raw data was ingested into Amazon S3 buckets (`ceb-raw-sah`) for centralized storage.
- Data security measures, such as AWS Key Management Service (KMS) encryption, were implemented to protect sensitive information.

### 2. Data Profiling and Cleaning
- AWS Glue DataBrew was used for data profiling, identifying missing values, outliers, and inconsistent formats.
- Key cleaning steps included:
  - Handling missing values through imputation or exclusion
  - Addressing outliers to prevent skewed analysis
  - Standardizing formats (e.g., dates as YYYY-MM-DD)
  - Removing duplicates to eliminate redundancy
- A DataBrew recipe documented and automated the cleaning process for future use.

### 3. Data Transformation
- AWS Glue ETL jobs were employed to automate transformations, including:
  - Dropping irrelevant columns to simplify the dataset
  - Aggregating data by service categories for key metrics (e.g., total budget requests and expenditures)
  - Standardizing schemas to ensure compatibility with downstream tools

### 4. Data Consolidation
- Transformed data was stored in structured formats (e.g., JSON, Parquet) in S3 buckets (`ceb-trf-sah`) for optimized storage and querying.
- Separate folders for user and system outputs ensured efficient access for various stakeholders.

### 5. Data Validation and Quality Control
- Data quality metrics were established, ensuring completeness (>95%) and uniqueness (>99%).
- Passed and failed datasets were categorized for auditing and reprocessing as needed.

  ![image](https://github.com/user-attachments/assets/11f44a7b-2613-46ae-a76a-e1a97ded3df9)


## Tools and Technologies
- **AWS Services:** S3, Glue DataBrew, Glue ETL, DynamoDB, and Athena
- **Data Profiling and Cleaning:** AWS Glue DataBrew
- **Data Storage:** S3 with KMS encryption for secure data handling
- **Querying and Analysis:** Amazon Athena

## Deliverables
- A cleaned and structured dataset stored in AWS S3.
- Documentation of the data wrangling process, including methods and tools used.
- Structured and queryable data outputs ready for analysis and visualization.

## Conclusion
This data wrangling project established a robust framework for managing and preparing the City of Vancouver’s capital project data. By leveraging AWS services, the process ensured data accuracy, security, and usability. The structured dataset serves as a foundation for advanced analytics, aiding stakeholders in making data-driven decisions with confidence. The automation and scalability of the wrangling process further enhance its applicability for future projects.
