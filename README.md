# SpaceX Falcon 9 Landing Prediction Capstone

## Overview

This repository contains the complete analysis for the **IBM Data Science Capstone Project** focused on SpaceX Falcon 9 launches and first-stage landing outcomes.

The project combines data collection, web scraping, data wrangling, exploratory data analysis, SQL, interactive visualization, and machine learning to investigate factors associated with successful Falcon 9 landings.

The main objective is to analyze historical launch characteristics and build classification models that predict whether the Falcon 9 first stage will land successfully.

---

## Project Objectives

The project addresses the following questions:

- How does landing success vary across launch sites?
- How are payload mass and orbit type related to landing outcomes?
- Has landing success improved with flight experience and over time?
- What geographic characteristics surround major Falcon 9 launch sites?
- Can machine-learning models predict first-stage landing success?
- Which classification model provides the strongest predictive performance?

---

## Methodology

The project was completed through the following workflow:

1. **Data Collection with the SpaceX REST API**
2. **Web Scraping of Falcon 9 Launch Records**
3. **Data Wrangling and Target Variable Preparation**
4. **Exploratory Data Analysis with Python**
5. **Exploratory Data Analysis with SQL**
6. **Machine Learning Classification**
7. **Interactive Geographic Analysis with Folium**
8. **Interactive Dashboard Development with Plotly Dash**

---

## Project Notebooks

| No. | Notebook | Description |
|---|---|---|
| 01 | [SpaceX Data Collection – API](01_SpaceX_Data_Collection_API_completed.ipynb) | Collects Falcon 9 launch data using the SpaceX REST API and prepares the initial dataset. |
| 02 | [SpaceX Web Scraping](02_SpaceX_Web_Scraping_completed.ipynb) | Extracts historical Falcon 9 launch records through web scraping. |
| 03 | [SpaceX Data Wrangling](03_SpaceX_Data_Wrangling_completed.ipynb) | Cleans and transforms the dataset and creates the binary landing-success target variable. |
| 04 | [SpaceX EDA – Data Visualization](04_SpaceX_EDA_Data_Visualization_completed.ipynb) | Explores launch-site, payload, orbit, flight-number, and yearly landing-success patterns. |
| 05 | [SpaceX EDA – SQL](05_SpaceX_EDA_SQL_completed.ipynb) | Performs SQL queries to investigate launch sites, payloads, mission outcomes, landing outcomes, and booster versions. |
| 06 | [SpaceX Machine Learning](06_SpaceX_Machine_Learning_completed.ipynb) | Builds, tunes, evaluates, and compares classification models for landing prediction. |
| 07 | [SpaceX Interactive Map – Folium](07_SpaceX_Interactive_Map_Folium.ipynb) | Maps launch sites, landing outcomes, and proximity to geographic and transportation features. |
| 08 | [SpaceX Interactive Dashboard – Plotly Dash](08_SpaceX_Interactive_Dashboard_Plotly_Dash.ipynb) | Creates an interactive dashboard with launch-site filtering, payload filtering, pie charts, and scatter plots. |

---

## Exploratory Analysis Highlights

The exploratory analysis showed several important patterns:

- Landing success generally increased with **flight experience and over time**.
- Landing performance differed across **launch sites**.
- **Payload mass** and **orbit type** showed meaningful relationships with landing outcomes.
- Interactive geographic analysis highlighted the locations of launch facilities and their proximity to coastlines and transportation infrastructure.
- The Plotly Dash dashboard enabled interactive comparison of landing outcomes by launch site and payload range.

---

## Interactive Analytics

### Folium

The Folium analysis includes:

- Falcon 9 launch-site locations
- Successful and unsuccessful landing markers
- Marker clustering
- Interactive coordinate inspection
- Geographic proximity analysis
- Distance measurements to nearby coastline, railway, highway, and city features

### Plotly Dash

The interactive dashboard includes:

- Launch-site dropdown selection
- Payload-mass range filtering
- Landing-outcome pie chart
- Payload vs. landing-outcome scatter plot
- Booster-version color grouping
- Interactive Dash callbacks

---

## Machine Learning

Four classification algorithms were evaluated:

- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree
- K-Nearest Neighbors (KNN)

Hyperparameters were tuned using **GridSearchCV with 10-fold cross-validation**.

### Model Performance

| Model | Cross-Validation Accuracy | Test Accuracy |
|---|---:|---:|
| Logistic Regression | 82.14% | 83.33% |
| Support Vector Machine | **84.82%** | **83.33%** |
| Decision Tree | 86.07% | 72.22% |
| K-Nearest Neighbors | 83.39% | **83.33%** |

Logistic Regression, SVM, and KNN tied for the highest test accuracy at **83.33%**.

Among the tied test-set leaders, **SVM achieved the highest cross-validation accuracy of 84.82%** and was therefore selected for final reporting.

### Selected Model Confusion Matrix

For the selected SVM classifier:

- True Positives: **12**
- True Negatives: **3**
- False Positives: **3**
- False Negatives: **0**
- Test Accuracy: **83.33%**

The principal classification error was false positives, while all successful landings in the test set were correctly identified.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SQLite / SQL
- BeautifulSoup
- Requests
- Folium
- Plotly
- Dash
- Jupyter Notebook

---

## Repository Structure

```text
SpaceX-Falcon9-Capstone/
│
├── README.md
├── 01_SpaceX_Data_Collection_API_completed.ipynb
├── 02_SpaceX_Web_Scraping_completed.ipynb
├── 03_SpaceX_Data_Wrangling_completed.ipynb
├── 04_SpaceX_EDA_Data_Visualization_completed.ipynb
├── 05_SpaceX_EDA_SQL_completed.ipynb
├── 06_SpaceX_Machine_Learning_completed.ipynb
├── 07_SpaceX_Interactive_Map_Folium.ipynb
└── 08_SpaceX_Interactive_Dashboard_Plotly_Dash.ipynb
