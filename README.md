# 🚦 Urban Mobility and Economic Performance Analysis

Exploratory Data Analysis using TomTom Traffic Index and OECD economic indicators to investigate the relationship between traffic congestion and city-level economic performance.

![Project Preview](IMAGES/traffic_vs_gdp_dual_axis.png)

---

## Project Overview

This project analyzes the relationship between urban mobility and economic performance across Latin American cities using traffic congestion data from the TomTom Traffic Index and economic indicators from the OECD.

The objective is to identify patterns that may support decision-making related to transportation planning and urban development through data cleaning, integration, visualization, and exploratory analysis.

---

## Table of Contents

- [Business Question](#business-question)
- [Business Answer](#business-answer)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Project Visualizations](#project-visualizations)
- [Project Limitations](#project-limitations)
- [Skills Demonstrated](#skills-demonstrated)
- [Repository Structure](#repository-structure)
- [How to Run the Project](#how-to-run-the-project)
- [Future Improvements](#future-improvements)
- [Acknowledgements](#acknowledgements)
- [Author](#author)

---

## Business Question

**Which city—Bogotá, Lima, Buenos Aires, or another major city—shows the strongest combination of high traffic congestion and relatively low economic productivity, suggesting it should be prioritized for transportation infrastructure investment?**

---

## Business Problem

Urban transportation authorities face difficult decisions when prioritizing infrastructure investments across cities with different levels of traffic congestion and economic development.

High traffic congestion can affect travel efficiency and urban mobility, but congestion levels alone do not provide sufficient evidence to determine which cities should receive investment priority.

This project explores how traffic congestion and GDP per capita vary across selected Latin American cities using 2024 data from the TomTom Traffic Index and OECD Metropolitan Database.

The analysis addresses three main questions:

- Which cities experience relatively high traffic delays?
- How does GDP per capita vary across the cities included in the analysis?
- Is there a measurable relationship between traffic congestion and GDP per capita?

The objective is to identify patterns that could inform further transportation planning research, rather than make definitive infrastructure investment decisions.

By integrating mobility and economic indicators, the project demonstrates how exploratory data analysis can help frame evidence-based questions for urban development.


## Business Answer

Based on the exploratory analysis, **Bogotá** emerged as the strongest candidate among the analyzed cities. It combines relatively high traffic congestion with lower GDP per capita compared with Lima and Buenos Aires.

Although the Pearson correlation coefficient (**0.283**) indicates only a weak positive linear relationship between congestion and GDP per capita, Bogotá represents a relevant case for future transportation investment studies. Additional variables such as public transportation quality, urban expansion, and population growth should be incorporated before making policy decisions.

---

## Technologies Used

| Category | Tools |
|---|---|
| Programming | Python |
| Data Analysis | Pandas, NumPy |
| Data Visualization | Matplotlib, Seaborn |
| Development Environment | JupyterLab, Visual Studio Code |

---


## Dataset Description & Data Preparation

### Data Sources

The project combines two publicly available data sources:

| Source | Information Used |
|---|---|
| TomTom Traffic Index | Traffic congestion, travel delays, and urban mobility indicators |
| OECD Metropolitan Database | GDP per capita and other economic and demographic indicators |

The analysis focused on selected Latin American cities using data corresponding to 2024.

### Data Preparation

Python and Pandas were used to prepare the datasets for integration and analysis.

The main preparation steps included:

1. **Data inspection:** Reviewed dataset structure, column names, data types, and available observations.
2. **Data cleaning:** Standardized relevant fields and checked for missing or inconsistent values.
3. **Date processing:** Prepared date information to identify observations corresponding to 2024.
4. **Data aggregation:** Organized mobility and economic information at the city-year level.
5. **Dataset integration:** Combined the prepared datasets using an INNER JOIN.
6. **Final validation:** Reviewed the resulting dataset before performing exploratory analysis.

### Analytical Dataset

The integrated dataset was designed to compare traffic congestion and economic performance across cities using a consistent city-year structure.

The final prepared data supported:

- Comparisons of traffic delay across cities.
- Comparisons of GDP per capita.
- Visual exploration of mobility and economic indicators.
- Pearson correlation analysis.

### Data Preparation Considerations

An INNER JOIN retains only observations with matching keys in both datasets. Therefore, cities without corresponding records in both sources may be excluded from the integrated dataset.

The analysis should be interpreted as an exploratory comparison of the matched observations, rather than a complete assessment of all Latin American cities.


---

## Project Workflow

The analysis followed a structured data analytics workflow:

1. Data loading from TomTom Traffic Index and OECD datasets.
2. Data cleaning and standardization of column names, dates, and numeric variables.
3. Data aggregation by city and year.
4. Integration of traffic and economic datasets using an INNER JOIN.
5. Exploratory data analysis through summary statistics and visualizations.
6. Correlation analysis between traffic congestion and GDP per capita.
7. Business interpretation and recommendations based on the findings.

---

## Methodology

The project followed a standard Exploratory Data Analysis (EDA) process:

- Data acquisition from public sources.
- Data quality assessment.
- Data cleaning and preprocessing.
- Feature selection.
- Dataset integration.
- Exploratory visualization.
- Statistical analysis using Pearson correlation.
- Business interpretation of the results.

---


## Key Findings & Business Insights

### 1. Data Processing and Integration

The initial traffic dataset contained 1,004,464 observations, while the economic dataset contained 30 records covering different cities and years.

Python and Pandas were used to standardize column names, convert dates and numeric fields, filter observations for 2024, and aggregate traffic metrics at the city-year level.

An INNER JOIN combined the mobility and economic datasets using city and year as matching keys.

**Analytical Value:**

The project demonstrates how large-scale traffic observations can be transformed into comparable city-level indicators and integrated with economic information.

### 2. Mexico City: Highest Traffic Congestion in the Aggregated Traffic Dataset

Mexico City recorded the highest average `jams_delay` value in the 2024 traffic aggregation:

- Mexico City: 2,833.06
- Tokyo: 2,152.57
- New York: 2,133.40

These figures represent the TomTom traffic delay metric, aggregated by city, rather than individual commuter travel times.

**Business Insight:**

Mexico City's elevated congestion indicator suggests that it warrants further investigation into mobility conditions, transportation capacity, and urban infrastructure.

### 3. Bogotá: High Congestion and Relatively Lower GDP per Capita

The integrated dataset reported the following results:

| City | Average Jams Delay | GDP per Capita |
|---|---:|---:|
| Bogotá | 1,141.55 | $11,442 |
| Buenos Aires | 571.09 | $18,117 |

Bogotá showed approximately twice the average traffic delay metric of Buenos Aires, alongside a lower GDP per capita.

**Business Insight:**

Bogotá represents a relevant candidate for further transportation planning research because its congestion levels are elevated relative to its economic indicators.

However, this comparison does not establish infrastructure investment priority on its own.

### 4. Weak Relationship Between Congestion and GDP per Capita

The Pearson correlation coefficient between GDP per capita and average traffic delay was:

**r = 0.283**

This indicates a weak positive linear relationship in the integrated dataset.

**Business Insight:**

GDP per capita alone does not adequately explain differences in congestion across the analyzed cities.

Other factors, such as population density, transportation networks, urban development, and vehicle ownership, should be considered before drawing policy conclusions.

### 5. Data Integration and Analysis Limitations

The analysis was limited to observations corresponding to 2024.

The INNER JOIN retained only matching city-year records from both datasets, so the final results should not be generalized to every city in the original traffic dataset.

The exploratory findings identify associations and differences between cities, but they do not demonstrate causation or quantify the benefits of infrastructure investments.

## Overall Business Interpretation

The results illustrate how mobility and economic indicators can be combined to identify cities that merit closer investigation.

Mexico City stood out in the broader traffic dataset, while Bogotá presented a notable combination of high congestion and comparatively lower GDP per capita in the integrated analysis.

These findings support further research and investment feasibility assessments rather than immediate policy decisions.


## Business Recommendations

The following recommendations are based on the exploratory analysis of 2024 traffic congestion and economic indicators.

### 1. Prioritize Further Mobility Research in Bogotá

**Finding:** Bogotá recorded an average traffic delay indicator of 1,141.55 and GDP per capita of $11,442, compared with 571.09 and $18,117, respectively, for Buenos Aires.

**Recommendation:** Conduct a detailed mobility needs assessment in Bogotá, including public transportation capacity, congestion hotspots, travel demand, and infrastructure conditions.

**Expected Value:** Identify the most relevant transportation challenges before determining whether new infrastructure or operational improvements are justified.

### 2. Investigate Congestion Conditions in Mexico City

**Finding:** Mexico City recorded the highest average traffic delay indicator (2,833.06) in the broader 2024 traffic aggregation.

**Recommendation:** Complement the city-level analysis with traffic data by road segment, time of day, and transportation mode.

**Expected Value:** Identify specific congestion patterns that could support more targeted mobility planning.

### 3. Expand the Analysis Beyond GDP per Capita

**Finding:** The Pearson correlation between traffic delay and GDP per capita was weak and positive (r = 0.283).

**Recommendation:** Include additional explanatory variables, such as population density, public transportation coverage, vehicle ownership, urban expansion, and employment concentration.

**Expected Value:** Improve the understanding of factors associated with congestion and reduce reliance on a single economic indicator.

### 4. Strengthen Data Coverage and Comparability

**Finding:** The analysis integrated TomTom and OECD datasets using an INNER JOIN, retaining only matching city-year observations.

**Recommendation:** Review unmatched cities, standardize geographical identifiers, and evaluate data availability across multiple years.

**Expected Value:** Improve the representativeness and comparability of future mobility and economic analyses.

### 5. Establish a Mobility Monitoring Framework

**Finding:** The project demonstrated that traffic and economic indicators can be standardized and compared at the city-year level.

**Recommendation:** Develop periodic monitoring of congestion indicators alongside economic and demographic variables, using a reproducible data preparation process and visual dashboard.

**Expected Value:** Support the identification of emerging mobility trends and provide a stronger evidence base for future transportation planning studies.

---

**Implementation Note:** These recommendations are exploratory proposals. The project did not assess infrastructure costs, forecast investment returns, establish causal relationships, or measure the impact of transportation interventions.

---

## Project Visualizations

### Traffic Delay Distribution

![Traffic Delay Distribution](IMAGES/traffic_delay_distribution.png)

---

### GDP per Capita Distribution

![GDP per Capita Distribution](IMAGES/gdp_distribution_histogram.png)

---

### Traffic Delay vs GDP per Capita

![Traffic Delay vs GDP per Capita](IMAGES/traffic_vs_gdp_dual_axis.png)

---

### Correlation Analysis

![Correlation Analysis](IMAGES/gdp_vs_traffic_scatter.png)

---

## Project Limitations

This analysis has several limitations:

- Only 2024 data were analyzed.
- The study focuses on correlation rather than causation.
- Additional socioeconomic variables could improve the analysis.
- Traffic conditions may be influenced by factors not included in the datasets.

---

## Skills Demonstrated

Throughout this project, the following data analytics skills were applied:

- Data cleaning and preprocessing
- Data aggregation
- Data integration using INNER JOIN
- Exploratory Data Analysis (EDA)
- Data visualization
- Correlation analysis
- Business storytelling
- Insight generation

---

## Repository Structure

```text
mobility-economic-analysis/
│
├── DATA/
├── IMAGES/
├── NOTEBOOKS/
├── ORIGINAL/
├── RESULTS/
├── WORKING/
└── README.md
```

---

## How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries.
3. Open the final notebook located in the `NOTEBOOKS` folder.
4. Run all notebook cells sequentially.

Required libraries:

- pandas
- numpy
- matplotlib
- seaborn

---

## Future Improvements

- Include additional socioeconomic variables.
- Apply multivariate regression models.
- Develop predictive models for traffic congestion.
- Build an interactive dashboard using Power BI or Tableau.

---

## Acknowledgements

This project uses publicly available datasets from:

- TomTom Traffic Index
- OECD Metropolitan Database

These datasets were used exclusively for educational and portfolio purposes.

---

## Author

**Roberto Blanco Lugo**

Data Analyst | Learning & Development | Business Analytics

- LinkedIn: *linkedin.com/in/roberto-blanco-lugo-/*
- GitHub: *github.com/robertwhitelugo*

