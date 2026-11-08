## IBM Data Science Capstone SpaceX Project


**SpaceX Falcon 9 First Stage Landing Prediction**

End-to-End Data Science | Exploratory Data Analysis | Machine Learning | Interactive Visualization

<p align="center">
  <img src="https://img.shields.io/badge/Python-Data%20Science-blue?logo=python" />
  <img src="https://img.shields.io/badge/Machine%20Learning-Classification-orange" />
  <img src="https://img.shields.io/badge/Visualization-Plotly%20%7C%20Folium-green" />
  <img src="https://img.shields.io/badge/SQL-IBM%20DB2-blue" />
  <img src="https://img.shields.io/badge/Project-IBM%20Capstone-052FAD" />
  <img src="https://img.shields.io/badge/License-MIT-brightgreen" />
</p>

# Executive Summary

Can we predict whether a SpaceX Falcon 9 first-stage booster will land successfully using historical launch data?

This project explores that question through an end-to-end data science workflow involving data collection, data wrangling, exploratory data analysis, geospatial visualization, interactive dashboards, and machine learning.

The primary objective is to identify patterns in historical Falcon 9 launches and develop classification models capable of predicting first-stage landing outcomes.

Using data collected from the SpaceX API and web scraping, I investigated the relationships between launch characteristics, including payload mass, orbit type, launch site, and mission outcomes.

**Four machine learning algorithms were developed and evaluated:**

- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree
- K-Nearest Neighbors (KNN)

The **Decision Tree** achieved the highest GridSearchCV score of **88.93%** among the evaluated models.

Beyond predictive modeling, this project demonstrates practical experience in data acquisition, SQL querying, statistical exploration, geographical analysis, and interactive data storytelling.

---

# Business Problem

SpaceX's Falcon 9 is designed with a reusable first stage, allowing the company to recover and reuse significant portions of its launch vehicle.

Booster recovery is an important contributor to SpaceX's launch economics. Understanding the factors associated with successful first-stage landings can provide useful information for launch planning and commercial launch analysis.

For companies evaluating commercial launch opportunities, estimating the likelihood of booster recovery can help inform launch-cost assumptions and competitive assessments.

**The central business question:**

- Given the characteristics of a Falcon 9 launch, can we predict whether its first-stage booster will land successfully?

This project investigates the question using historical launch data and supervised machine learning.

# **Project Objectives**

1. Collect historical Falcon 9 launch data using the SpaceX REST API.
2. Extract supplementary launch information through web scraping.
3. Clean, transform, and prepare data for analysis.
4. Investigate launch patterns using Python, Pandas, NumPy, and SQL.
5. Identify relationships between launch characteristics and landing outcomes.
6. Explore launch-site geography using interactive maps.
7. Build an interactive dashboard for launch data exploration.
8. Train, optimize, and evaluate multiple classification algorithms.
9. Identify the most promising predictive model based on evaluation results.

---

# Technology Stack


|Category| Tools and Technologies
|Programming| Python
|Data Collection| REST API, Requests, BeautifulSoup
|Data Processing| Pandas, NumPy
|Database| IBM DB2, SQL
|Data Visualization| Matplotlib, Seaborn
|Interactive Maps| Folium
|Interactive Dashboard| Plotly, Dash
|Machine Learning| Scikit-learn
|Model Optimization| GridSearchCV
|Development Environment| Jupyter Notebook


# End-to-End Project Workflow

The project follows seven major stages of the data science lifecycle.

<ins>**1. Data Collection Using SpaceX API**</ins>

Notebook: "1.jupyter_labs_spacex_data_collection_api.ipynb"

Collected historical launch information through the SpaceX REST API.

**Key activities:**

- Accessed SpaceX launch data using HTTP requests.
- Retrieved JSON responses from the API.
- Used Pandas "json_normalize()" to structure nested JSON data.
- Filtered the records to include Falcon 9 launches.
- Examined missing values and prepared the dataset for further analysis.

Dataset obtained: 90 records and 17 features.

**2. Web Scraping**

Notebook: "2.jupyter-labs-webscraping.ipynb"

Collected supplementary launch information through web scraping.

Key activities:

- Retrieved the Falcon 9 launch history webpage.
- Parsed HTML content using BeautifulSoup.
- Extracted table headers and launch records.
- Transformed the extracted information into a structured Pandas DataFrame.

Dataset obtained: 121 records and 11 features.

**3. Data Wrangling and Preparation**

Notebook: "3.labs-jupyter-spacex-Data wrangling-v2.ipynb"

Prepared the collected data for meaningful analysis and predictive modeling.

Key activities:

- Identified and handled missing values.
- Cleaned and transformed relevant variables.
- Prepared categorical and numerical features.
- Created the target variable representing landing success.
- Structured the analytical dataset for subsequent exploration.

**4. Exploratory Data Analysis Using SQL**

Notebook: "4.jupyter-labs-eda-sql-coursera_sqllite.ipynb"

Used SQL to investigate launch records and identify important patterns.

The analysis included:

- Identifying unique SpaceX launch sites.
- Investigating payload mass across missions.
- Calculating average payload mass for specific booster versions.
- Examining launch frequencies and mission characteristics.
- Analyzing records using aggregation and filtering.

SQL concepts used included:

"SELECT", "DISTINCT", "WHERE", "GROUP BY", "ORDER BY", "COUNT()", "SUM()", "AVG()", "MIN()", and "MAX()".

**5. Exploratory Data Analysis and Visualization**

Notebook: "5.jupyter-labs-eda-dataviz-v2.ipynb"

Performed exploratory analysis to understand the relationships between launch characteristics and landing outcomes.

Areas investigated:

- Launch success patterns across flight numbers.
- Relationships between payload mass and launch sites.
- Landing success rates across different orbit types.
- Distribution of mission outcomes.
- Relationships between launch characteristics and landing performance.

Visualization techniques included:

- Scatter plots
- Bar charts
- Line charts
- Categorical plots

Libraries: Matplotlib, Seaborn, Pandas, and NumPy.

**6. Geospatial Analysis Using Folium**

Notebook: "6.lab-jupyter-launch-site-location-v2.ipynb"

Explored the geographical characteristics of SpaceX launch facilities.

Key activities:

- Mapped SpaceX launch sites.
- Visualized successful and unsuccessful launch outcomes.
- Used marker clustering to explore launch distributions.
- Investigated distances between launch facilities and nearby geographical features, including cities, railways, and highways.

This analysis provides a geographical perspective on launch operations and recovery-related patterns.

**7. Interactive Dashboard Using Plotly and Dash**

Application: "7. IBM_SpaceX_Dash_App.py"

Developed an interactive dashboard to make launch data exploration more accessible.

Dashboard functionality includes:

- Selecting launch sites through an interactive dropdown.
- Filtering payload mass using a range slider.
- Comparing successful and unsuccessful launch outcomes.
- Exploring launch-site success distributions through pie charts.
- Investigating payload mass against mission outcomes using scatter plots.

The dashboard provides an interactive way to explore the dataset without manually executing individual analysis queries.

**8. Machine Learning: Predicting Landing Outcomes**

Notebook: "8.SpaceX_Machine_Learning_Prediction_Part_5_v1.ipynb"

Developed supervised classification models to predict Falcon 9 first-stage landing outcomes.

Model development workflow:

1. Prepared the features and target variable.
2. Standardized numerical features using "StandardScaler".
3. Split the dataset into training and testing sets.
4. Trained four classification algorithms.
5. Applied "GridSearchCV" for hyperparameter optimization.
6. Evaluated model performance using accuracy scores and confusion matrices.
7. Compared the optimized models.

Algorithms implemented:

Algorithm| Scikit-learn Implementation
Logistic Regression| "LogisticRegression"
Support Vector Machine| "SVC"
Decision Tree| "DecisionTreeClassifier"
K-Nearest Neighbors| "KNeighborsClassifier"

---

# Machine Learning Results

**Model Comparison**

The following table presents the best cross-validation scores obtained through GridSearchCV.

Model| Best GridSearchCV Score
Decision Tree| 88.93%
K-Nearest Neighbors| 84.82%
Support Vector Machine| 84.82%
Logistic Regression| 84.64%

<details>
<summary><strong>Click to see the detailed model scores</strong></summary>- Decision Tree: 0.8892857142857142
- K-Nearest Neighbors: 0.8482142857142858
- Support Vector Machine: 0.8482142857142856
- Logistic Regression: 0.8464285714285713

</details>Best Performing Model

Decision Tree Classifier

The Decision Tree achieved the highest GridSearchCV score of approximately 88.93%, making it the strongest candidate among the four evaluated algorithms based on the reported cross-validation results.

An important observation from the evaluation was that all four models produced the same accuracy score and confusion matrix on the test dataset. Consequently, the best cross-validation scores were used to distinguish their performance.

Interpretation: The Decision Tree demonstrated the strongest cross-validation performance on this dataset. However, its generalization performance should be validated with additional data and robust evaluation before using it in a real-world launch-planning environment.

---

# Key Analytical Insights

The exploratory analysis highlighted several relationships worth investigating:

**1. Launch-site characteristics**

Launch outcomes can be explored across different launch facilities to understand how historical landing performance varies by location.

**2. Payload mass**

Payload mass is an important launch characteristic. Its relationship with landing outcomes can vary across mission configurations and orbit types.

**3. Orbit type**

Different orbit categories exhibit different historical landing patterns. The relationship between payload mass and landing outcome is not necessarily consistent across all orbit types.

**4. Flight history**

Analyzing flight number against landing outcomes provides a way to investigate patterns associated with booster launch history.

**5. Geographical characteristics**

Interactive geographical analysis helps explore the spatial distribution of launch sites and their surrounding infrastructure.

These observations are exploratory associations, not proof of causation.

---

# Repository Structure

IBM-Data-Science-Capstone-SpaceX-Project/
│
├── 1.jupyter_labs_spacex_data_collection_api.ipynb
│
├── 2.jupyter-labs-webscraping.ipynb
│
├── 3.labs-jupyter-spacex-Data wrangling-v2.ipynb
│
├── 4.jupyter-labs-eda-sql-coursera_sqllite.ipynb
│
├── 5.jupyter-labs-eda-dataviz-v2.ipynb
│
├── 6.lab-jupyter-launch-site-location-v2.ipynb
│
├── 7. IBM_SpaceX_Dash_App.py
│
├── 8.SpaceX_Machine_Learning_Prediction_Part_5_v1.ipynb
│
├── Data Science Capstone Project Report.pdf
│
├── SpaceX_Falcon9_Data_Science_Presentation.pptx
│
├── LICENSE
│
└── README.md

₹ Project Deliverables

The repository includes the complete analytical workflow and supporting project materials.

Deliverable| Description
Jupyter Notebooks| Data collection, wrangling, EDA, mapping, and machine learning
Python Dashboard| Interactive SpaceX launch analysis
PDF Report| Consolidated project documentation
PowerPoint Presentation| Project presentation and findings

Additional resources:

- "Project Report (PDF)" (Data%20Science%20Capstone%20Project%20Report.pdf)
- "Project Presentation (PowerPoint)" (SpaceX_Falcon9_Data_Science_Presentation.pptx)

---

# How to Run the Project

Prerequisites

- Python 3.x
- Jupyter Notebook or JupyterLab
- Git
- Internet connection for external data collection

**1. Clone the repository**

git clone https://github.com/rudrascience/IBM-Data-Science-Capstone-SpaceX-Project.git

**2. Navigate to the project directory**

cd IBM-Data-Science-Capstone-SpaceX-Project

**3. Install the Python dependencies**

pip install pandas numpy requests beautifulsoup4
pip install matplotlib seaborn scikit-learn
pip install folium plotly dash
pip install jupyter ipython-sql sqlalchemy

Some SQL notebook operations were originally developed using IBM DB2 and its associated Python connector. Running those sections may require an appropriately configured DB2 environment and additional dependencies.

**4. Launch Jupyter Notebook**

jupyter notebook

**5. Explore the notebooks**

Open the notebooks in numerical order to follow the complete data science workflow.

For the interactive dashboard, use:

python "7. IBM_SpaceX_Dash_App.py"

The dashboard may require additional environment configuration and compatible Dash dependencies.

---

# Limitations and Future Enhancements

While this project demonstrates a complete data science workflow, there are opportunities to improve its analytical depth and production readiness.

**Potential enhancements include:**

**Data and feature engineering**

- Expand the dataset with additional historical launch records.
- Investigate additional booster and mission characteristics.
- Improve handling of missing and inconsistent observations.
- Establish a consistent data extraction and preprocessing pipeline.

**Machine learning**

- Evaluate models using stratified cross-validation.
- Investigate class imbalance.
- Compare precision, recall, F1-score, and ROC-AUC.
- Perform more extensive hyperparameter optimization.
- Explore ensemble methods such as Random Forest and Gradient Boosting.
- Apply model interpretability techniques such as feature importance and SHAP.

**Deployment and engineering**

- Develop a reusable prediction pipeline.
- Build a deployment-ready application.
- Add automated testing and dependency management.
- Improve reproducibility through a documented environment configuration.
- Add automated data updates and model monitoring.

These improvements would help evolve the project from an analytical capstone into a more production-oriented machine learning application.

---

# Skills Demonstrated

This project demonstrates practical application of the following data science competencies:

Skill| Practical Application
Python Programming| Data extraction, transformation, and analysis
API Integration| Collecting structured SpaceX launch data
Web Scraping| Extracting historical launch records
Data Wrangling| Cleaning and preparing analytical datasets
SQL| Querying and investigating launch records
Exploratory Data Analysis| Identifying patterns and relationships
Data Visualization| Communicating insights through charts
Geospatial Analytics| Mapping launch sites and outcomes
Dashboard Development| Building interactive data applications
Machine Learning| Developing classification models
Hyperparameter Optimization| Applying GridSearchCV
Model Evaluation| Comparing classification performance

# References and Acknowledgements

- "SpaceX API" (https://github.com/r-spacex/SpaceX-API)
- "IBM Data Science Professional Certificate" (https://www.coursera.org/professional-certificates/ibm-data-science)
- "Scikit-learn Documentation" (https://scikit-learn.org/stable/)
- "Pandas Documentation" (https://pandas.pydata.org/docs/)
- "Matplotlib Documentation" (https://matplotlib.org/)
- "Seaborn Documentation" (https://seaborn.pydata.org/)
- "Folium Documentation" (https://python-visualization.github.io/folium/)
- "Plotly Dash Documentation" (https://dash.plotly.com/)

This project was completed as part of the IBM Data Science Professional Certificate capstone experience.

# Author

Rudrajit Das

Data Science | Data Analytics | Python | SQL | Machine Learning

**GitHub: "@rudrascience" (https://github.com/rudrascience)**

**Project Repository:** "IBM Data Science Capstone – SpaceX Project" (https://github.com/rudrascience/IBM-Data-Science-Capstone-SpaceX-Project)

---

Thank you for exploring this project. Feedback, suggestions, and constructive discussions are always welcome.
