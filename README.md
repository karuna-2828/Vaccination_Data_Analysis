# 🦠 VaccinationData Analysis & Visualization (Mini Project -2)

## Overview
This project performs Exploratory Data Analysis (EDA) and visualizations to uncover insights from global vaccination datasets, including coverage, disease incidence trends, vaccine schedules, and introduction timelines. The goal is to identify regional disparities, assess vaccination impact on disease reduction, and support public health decision-making.

## 📁 Datasets Used

| Dataset Name                     | Description                                                                     |
| -------------------------------- | ------------------------------------------------------------------------------- |
| `coverage-data.xlsx`             | Vaccination coverage percentages by region, year, antigen, and population group |
| `incidence-rate-data.xlsx`       | Disease incidence rates by country, disease, and year                           |
| `reported-cases-data.xlsx`       | Number of reported cases for various diseases                                   |
| `vaccine-introduction-data.xlsx` | Year-wise vaccine introduction status by region                                 |
| `vaccine-schedule-data.xlsx`     | Vaccine scheduling data including year, vaccine code, target population         |

## ⚙️ Features & Functionalities
### Missing Value Handling
  * Imputation using median, mode, and logic-based estimation (e.g., COVERAGE = (DOSES / TARGET_NUMBER) * 100)

### Normalization & Consistency Checks
  * Data types normalized (e.g., dates), units standardized (percentages, counts), and format consistency maintained

### Univariate Analysis
  * Histograms, bar plots, and count plots for individual columns (numerical and categorical)

### Bivariate Analysis
  * Correlation analysis between variables like DOSES vs TARGET_NUMBER, COVERAGE vs REGION, etc.

### Multivariate Analysis
  * Heatmaps, grouped bar plots, and trend lines to analyze patterns across 3 or more variables (e.g., TARGETPOP vs YEAR vs VACCINE CODE)

### Visualization Tools

  * Seaborn for statistical graphics

  * Matplotlib for base visualizations

  * Pandas for analysis and pivoting


## 🗄️ MySQL Integration
After the data cleaning phase, integrating the datasets into a MySQL database provides a robust foundation for structured querying, analysis, and reporting. 
### Database Design:
* Individual tables are created for each cleaned dataset (e.g., coverage, incidence rates, reported cases, vaccine introduction, and vaccine schedule), with appropriate schema definitions.

### Connection Setup:
* A secure connection to the MySQL server is established using a connector (like mysql-connector or SQLAlchemy in Python).

### Data Import:
* Cleaned DataFrames are loaded into MySQL tables using automated scripts, ensuring that data types align with the table schema.

### Indexing and Keys:
* Primary keys and indexes are defined for efficient querying. Foreign keys may be used to establish relationships between datasets where applicable (e.g., linking vaccine codes across tables).

### Validation:
* Post-import checks are performed to validate row counts, column types, and null values to ensure data integrity.

### Querying and Analysis:
* Once integrated, the datasets can be queried using SQL for descriptive and exploratory analysis. This also enables integration with BI tools like Power BI or Tableau via SQL connectors.

### Scalability and Maintenance:
* The MySQL database allows for easy updates, scalability with large datasets, and centralized access for analytics and reporting teams.

## 📊 Power BI Integration

After integrating datasets into a MySQL database, Power BI can be used to visualize and analyze the data interactively.

### MySQL Connector Setup:
* Ensure that the MySQL ODBC or MySQL Connector for Windows is installed. This allows Power BI to communicate with the MySQL server.

### Establishing the Connection:
* In Power BI Desktop, the “Get Data” option is used to select MySQL database. The host (server), database name, and credentials are entered to establish a secure connection.

### Data Import or Direct Query:
Users can choose between:

*  Import Mode: Data is loaded into Power BI's in-memory model for fast performance.

*  Direct Query: Data remains in MySQL and is queried live when visuals are interacted with.

### Table Selection and Relationships:
* After connecting, the relevant tables (e.g., coverage_data, incidence_rate, etc.) are selected. Relationships between tables can be defined in Power BI's Model View for integrated analysis.

### Data Transformation:
* Power BI’s Power Query Editor allows further cleaning, filtering, and shaping of data before analysis, directly from the MySQL source.

### Visualization and Dashboards:
* Users can build interactive dashboards to visualize:

* Trends in vaccination coverage

* Regional disparities

* Correlations between disease incidence and vaccine introduction

### Scheduled Refresh:
* Power BI Service (cloud version) allows scheduled refreshes by configuring a gateway to keep dashboards up-to-date with changes in the MySQL database.

### Security and Access Control:
* Role-based access can be configured to restrict data visibility, ensuring only authorized users can view or edit reports.

## 📊 Key Insights
* Identified regions with consistently low vaccination coverage

* Observed strong inverse correlation between vaccine coverage and disease incidence

* Highlighted disparities in vaccine introduction across WHO regions

* Visualized vaccination scheduling trends over years by vaccine


<img width="484" alt="image" src="https://github.com/user-attachments/assets/9ffd076a-21f7-40bd-a8b3-0715cb8a7dae" />

<img width="485" alt="image" src="https://github.com/user-attachments/assets/b20e3165-ac30-4076-9319-f150fb53a8f7" />

<img width="485" alt="image" src="https://github.com/user-attachments/assets/f1988c38-fa12-4fc1-b956-d8b3141fc79a" />

<img width="486" alt="image" src="https://github.com/user-attachments/assets/c65e6199-2847-46f5-a7c2-ceef4b302d1d" />



## 🧠 Possible Enhancements
* Build an interactive dashboard using Streamlit or Dash

* Incorporate predictive modeling for future coverage or disease trends

* Merge with geospatial data for map visualizations

## ✅ Conclusion
This project successfully demonstrates how integrated data from multiple sources—such as vaccine coverage, disease incidence, reported cases, vaccine introduction, and scheduling—can be cleaned, structured, and analyzed to derive meaningful insights. Through comprehensive Exploratory Data Analysis (EDA), we identified vaccination trends, low-coverage regions, and correlations with disease reduction.

The integration of these datasets into a MySQL database allowed for efficient querying, structured storage, and scalability. Visualization tools like Power BI enabled the creation of dynamic dashboards, enhancing our ability to monitor public health metrics and support data-driven decision-making.

By combining statistical techniques, database management, and visualization, this project highlights the value of end-to-end data pipelines in public health analytics.
