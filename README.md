# SPE Datathon 2026 – Oil Presence Prediction using Machine Learning

## Overview

This project was developed for the **SPE Datathon 2026** to predict the presence of oil in unexplored locations using geological and geophysical data. The objective was to provide a non-destructive, data-driven alternative to costly exploratory drilling by leveraging machine learning techniques.

Our solution combined domain knowledge, rigorous data preprocessing, feature engineering, and model optimization to build robust predictive models for both competition tasks.

---

## Project Workflow

### 1. Domain Research
Before modelling, we investigated geological relationships between reservoir properties to validate the dataset and identify inconsistencies. This helped guide feature engineering decisions and prevented unrealistic assumptions from affecting the models. 
Our findings are documented [here](https://docs.google.com/document/d/18KgChC6qzngcY5tHbvzZDImq3opYi2hnKpBRUSOYS7s/edit?usp=sharing).

### 2. Data Cleaning
- Standardized categorical values and column names.
- Removed duplicate and conflicting records.
- Investigated outliers using Isolation Forest and retained valid geological observations.
- Carefully handled missing values using statistically and geologically appropriate strategies.

### 3. Exploratory Data Analysis
EDA was used to understand:
- Class imbalance in oil presence.
- Relationships between seismic attributes and oil occurrence.
- Distribution of reservoir properties.
- Correlations between numerical variables.
- Geological patterns across rock and trap types.

The analysis confirmed seismic score, proximity to known oil fields, porosity, permeability, and geological formations as key predictive variables.

### 4. Feature Engineering
Several domain-informed features were created, including:
- Encoded geological categories.
- Rock-type-specific transformations.
- Adjusted porosity and permeability relationships.
- Scaled interaction features.
- Missing-value prediction pipelines for reservoir properties.

### 5. Model Development
Multiple machine learning models were evaluated, including:
- Logistic Regression
- Random Forest
- LightGBM
- XGBoost

Hyperparameter optimization was performed using:
- **Optuna** (Part 1)
- **Randomized Search CV** (Part 2)

The evaluation primarily focused on **F1 Macro**, **Recall**, and **Precision** due to the imbalanced nature of the dataset.

---

## Results

### Part 1
**Best Model:** LightGBM

- F1 Macro: **0.67**
- Recall: **0.75**
- Accuracy: **79%**

### Part 2
**Best Model:** Random Forest

- F1 Macro: **0.77**
- Precision: **0.80**
- Recall: **0.54**
- Accuracy: **84%**

---

## Key Takeaways

- Domain knowledge significantly improved feature engineering and data validation.
- Careful preprocessing and handling of geological relationships enhanced model performance.
- Optimizing for **F1 Macro** and **Recall** produced models better suited for identifying potential oil-bearing locations than accuracy alone.
- Ensemble tree-based models consistently outperformed linear models for this problem.

---

## Team

**Team Wisdom**

- Chigozie Udoh
- Adejire Adegite
- Kenechukwu Ezeonugo
- Adedamola Adams

---

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- LightGBM
- XGBoost
- Optuna
- Matplotlib
- Seaborn

---

## Repository Structure

```text
├── data/
├── notebooks/
├── models/
├── outputs/
├── presentation/
├── README.md
└── requirements.txt
```

---

## Acknowledgement

This project was developed as part of the **Society of Petroleum Engineers (SPE) Datathon 2026**, demonstrating the application of machine learning and domain knowledge to support data-driven exploration decisions in the energy industry.


## Used during competition
## Notes
This dataset contains outliers, null values, and some technical anomalies. It is expected that participating teams will apply oil and gas domain knowledge

**Part 1** will be data science based perhaps no domain knowledge things, just basic way of data cleaning, no constraints check, an intuitive way of filling missing values, just the basic stuff, maybe outlier removal as well

**Part 2** will be listening to constraints, domain knowledge of generating features, etc. It will include all of part 1 + extra basically. Something to note, there's 3 geological anomalies in 3 features, perhaps some constraints are violated based on provided range in the about the dataset part or something like that.

## Plan
### Phase 1 - 19th June - 20th June
### Phase 1 A
**KC & AJ** - In depth research and understanding of all features and empirical formulas related to this part of geology combined with dataset exploration (EDA) to understand what the organizers mean about "correct geological anomalies or inconsistencies in at least three (3)
dataset features"

### Phase 1 B
**Damola** - Start Basic Data Cleaning check in notebook for train data (this checks will apply to Part 1 and Part 2). You can reference this [notebook](https://github.com/pithun/2024-SPE-DSEATS-Datathon-Open-Solution/blob/master/2nd-Place/Submissions/Chigozie_Udoh_2024_DSEATS_Datathon_5272808.ipynb)

Specifically, do;
1. Column name shortening
2. Data Type check (ensure correct data types are assigned)
3. Consistency check for text columns (ensure trap_type for example has the different trap types with same name. e.g we shouldn't have DOME and dome)
4. Missing Data check (you have to suggest ways to fill missing values)
5. Duplicate check
6. Outlier Detection (Feel free to use a model like Isolation Forest for this later on)
7. Any extra stuff is highly welcomed

### Phase 1 C
**Udoh**  - Slides preparation + Review/Support 1A and Review 1B

### Phase 2 - 21st June
Brainstorm Session to get clarity on what to do with dataset regarding part 2

### Phase 3 - 21st June to 24th June
- **Everyone** - Feature Engineering and Modelling Brainstorming
- **KC** - Review Slides Template
- **Udoh and Damola** - FE and Modelling Execution
- **AJ** - FE and Modelling Support

### Phase 4  - 25th June to 26th June
**Everyone** - Populating Slides based on part you worked on

### Phase 5 - 27th June to 28th June
Individual reviews to confirm that results make sense
