# Population Analysis Capstone Project

Welcome to the Population Analysis Capstone Project, a collaborative effort aimed at understanding global population trends and their relationship with various human development indicators.

## 📊 Project Objective

This project seeks to analyze the global population and its growth using data analysis techniques in Python (Pandas) and SQL. The goal is to evaluate whether social, economic, and health-related factors significantly impact population trends.


## 🧱 Repository Structure
```
population_analysis/
├── data_cleaning/ # Jupyter notebooks for cleaning datasets
│   ├── data_clean/ # Individual scripts for each dataset
│   │   ├── cleaning_education.ipynb
│   │   ├── cleaning_fertility.ipynb
│   │   ├── cleaning_gdp_person.ipynb
│   │   ├── cleaning_mortality.ipynb
│   │   └── cleaning_population.ipynb
│   └── .DS_Store
│
├── data_raw/ # Original raw data (CSV files)
│   ├── Top_and_Bottom_5_Countries_by_*.csv # Summary data for selected countries
│   ├── child_mortality.csv
│   ├── education.csv
│   ├── fertility_rate.csv
│   ├── gdp_person.csv
│   └── population.csv
│
├── data_wrangling/ # Processed and reshaped datasets
│   ├── HDI_selected_data/ # Data for 60 selected countries
│   │   ├── child_mortality_HDI.csv
│   │   ├── education_HDI.csv
│   │   ├── fertility_HDI.csv
│   │   ├── gdp_HDI.csv
│   │   └── population_HDI.csv
│   └── datasets_from_1985_total/ # Data for 60 selected countries starting from 1985
│       ├── 1985_child_mortality_selected.csv
│       ├── 1985_education_rate_selected.csv
│       ├── 1985_fertility_rate_selected.csv
│       ├── 1985_gdp_selected.csv
│       └── 1985_population_selected.csv
│
├── hypothesis_test/ # Statistical hypothesis testing
│   └── hyp_testing.ipynb
│
├── melted_tables_to_sql/ # Reshaped data ready for SQL import for easier visualization in Tableau
│   ├── additional_tables_melt/
│   │   ├── melted_1985_fertility.csv
│   │   ├── melted_1985_population.csv
│   │   └── population_fertility_melting.ipynb
│   └── to_sql.ipynb # Script to load data into SQL
│
├── sql_HDI_selected_data/ SQL script for querying data only for 60 selected countries
│   └── sql_population_analysis.sql
│
├── from_sql_HDI_1985.ipynb # Notebook for querying modified data from SQL
├── to_sql_final.ipynb # Final SQL load notebook
├── .gitignore
└── README.md
```


Each directory represents a stage in the data analytics process.

## 📂 Data Sources

The primary datasets used in this project include:

- Fertility rate, total (births per woman): 
  - Columns: Years 1960-2022, Country Name, Country Code,  266 Rows
  - https://data.worldbank.org/indicator/SP.DYN.TFRT.IN
- Population, total:
  - Columns: Years 1960-2022, Country Name, Country Code,  266 Rows
  - https://data.worldbank.org/indicator/SP.POP.TOTL
- Mortality Rate, under-5 (per 1,000 live births)
  - Columns: Years 1960-2022, Country Name, Country Code,  266 Rows
  - https://data.worldbank.org/indicator/SH.DYN.MORT
- GDP per Capita (current US$ )
  - Columns: Years 1960-2022, Country Name, Country Code,  266 Rows
  - https://data.worldbank.org/indicator/NY.GDP.PCAP.CD
- Educational attainment, at least completed lower secondary, population 25+, female (%) (cumulative)
  - Columns: Years 1960-2022, Country Name, Country Code, 266 Rows
  - https://data.worldbank.org/indicator/SE.SEC.CUAT.LO.FE.ZS


## 🧹 Data Cleaning

Raw datasets are cleaned to handle:

- Missing values
- Inconsistent formatting
- Unnecessary columns

This step ensures the data is analysis-ready.

## 🔄 Data Wrangling

We use Pandas and SQL techniques to reshape, merge, and filter datasets. Examples include:

- Melting wide tables to long format for further visualization using Tableau.
- Filtering countries
  - We defined 6 regions of the world, such as Africa, the Americas, Asia, Oceania, Europe and the Middle East. From each region, 10 countries were selected as a sample of the region, consisting of 5 most developed and 5 least developed countries. This was defined using the UN Human Development Index (HDI). 
- Filtering years of interest
  - The original datasets covered the period from 1960 to 2022. However, due to a high volume of missing values prior to 1985, we excluded those years and focused our analysis on the more complete timeframe from 1985 to 2022.

## 🔬 Hypothesis Testing

Statistical methods were used to test following hypotheses:

- Null Hypothesis (H₀): There is no significant difference in population growth trends across regions.
- Null Hypothesis (H₀): There is no linear relationship between fertility rate and population growth rate.
- Null hypothesis (H₀): Child mortality rate has no effect on population growth.
- Null hypothesis (H₀): Female education rate has no effect on population growth.
- Null hypothesis (H₀): GDP per capita has no effect on population growth.
- Null hypothesis (H₀): Child mortality rate has no effect on fertility rate.
- Null hypothesis (H₀): Female education rate has no effect on fertility rate.
- Null hypothesis (H₀): GDP per capita has no effect on fertility rate.

## 🗃️ SQL Integration

Cleaned and reshaped datasets are loaded into a SQL database to:

- Support reproducible analysis workflows
- Querying necessary data for the analysis

## 📈 Visualizations

Most visualizations were created using Tableau, with a few generated using Matplotlib. We presented the following insights to stakeholders:
- Trends over time
- Correlations between social, economic, and health-related factors and population patterns
- Regional comparisons to highlight differences across countries and continents
  
## 🤝 Contributors

- [Kseniia Vasylieva](https://github.com/kseniiavasylieva1)
- [GitRdone25](https://github.com/GitRdone25)

---

