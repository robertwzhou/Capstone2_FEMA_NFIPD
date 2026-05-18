# FEMA NFIP Data Analysis Capstone Project

## Table of Contents
1. [Introduction](#introduction)
2. [Data Wrangling](#data-wrangling)
3. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
4. [Preprocessing](#preprocessing)
5. [Modeling](#modeling)
6. [Results & Findings](#results--findings)
7. [Conclusion](#conclusion)
8. [Future Steps](#future-steps)
9. [Project Structure](#project-structure)
10. [Getting Started](#getting-started)

---

## Introduction

### Project Overview
This capstone project analyzes data from the National Flood Insurance Program (NFIP), administered by the Federal Emergency Management Agency (FEMA). The project aims to [**insert your specific research question/objective here**].

### Data Source
The dataset originates from the [FEMA OpenFEM platform](https://www.fema.gov/openfem), containing comprehensive NFIP policy information. The original dataset comprises 70+ million rows, making this a large-scale data analysis challenge.

### Objectives
- **Primary Goal**: [Define your main analytical or predictive objective]
- **Secondary Goals**: [List any supporting objectives]
- **Key Stakeholders**: Insurance professionals, FEMA analysts, risk assessment teams

### Dataset Overview
- **Total Records in Full Dataset**: 70+ million rows
- **Sampled Training Data**: [Specify number of rows]
- **Sampled Test Data**: [Specify number of rows]
- **Key Features**: [Brief description of important variables]

---

## Data Wrangling

### Overview
Data wrangling prepares the raw NFIP data for analysis by addressing inconsistencies, handling missing values, and organizing information into a usable format.

### Process Workflow
**File**: `sample.ipynb`

1. **Data Extraction**: Downloaded and accessed the `FimaNfipPoliciesV2.parquet` file from FEMA's OpenFEM platform
2. **Sampling Strategy**: 
   - Sampled representative subsets from the 70+ million row dataset
   - [Specify sampling methodology, e.g., stratified sampling, random sampling, time-based sampling]
   - Created balanced train/test splits for modeling

**File**: `datawrangling.ipynb`

3. **Data Cleaning**:
   - Identified and handled missing values
   - Removed duplicate records
   - [List any specific data quality issues addressed]

4. **Data Type Conversions**:
   - Standardized date formats
   - Converted categorical variables
   - Ensured numeric precision where needed

5. **Feature Engineering**:
   - [Describe any new features created during wrangling]
   - [Explain domain-specific transformations]

6. **Data Validation**:
   - Verified data integrity across sampled train and test sets
   - Checked for data leakage
   - Validated statistical properties

### Key Challenges & Solutions
| Challenge | Solution |
|-----------|----------|
| [Issue 1] | [Resolution] |
| [Issue 2] | [Resolution] |
| [Issue 3] | [Resolution] |

### Output
- Cleaned training dataset: `[output_filename]`
- Cleaned test dataset: `[output_filename]`

---

## Exploratory Data Analysis (EDA)

### Overview
EDA investigates the structure, distribution, and relationships within the NFIP data to uncover patterns and insights.

**File**: `eda.ipynb`

### Key Analyses Performed

#### 1. **Univariate Analysis**
- Distribution of individual features (histograms, box plots, density plots)
- [Specific insights about key variables]

#### 2. **Bivariate & Multivariate Analysis**
- Correlations between key variables
- Relationships among [specific feature groups]
- [Notable patterns discovered]

#### 3. **Categorical Variable Analysis**
- Frequency distributions of policy types, coverage levels, states
- [Key categorical insights]

#### 4. **Geographic Analysis**
- Regional patterns in policy distribution
- Risk concentration by state/district
- [Geographic findings]

#### 5. **Temporal Trends** (if applicable)
- Historical policy trends
- Seasonal patterns
- [Temporal insights]

### Key Findings
- **Finding 1**: [Description and impact]
- **Finding 2**: [Description and impact]
- **Finding 3**: [Description and impact]

### Visualizations
Key visualizations created include:
- Distribution plots of major features
- Correlation heatmaps
- Geographic risk maps
- Trend analysis charts

### Missing Data Analysis
- Percentage of missing values by column
- Patterns in missingness
- Imputation strategy decisions

---

## Preprocessing

### Overview
Preprocessing transforms the analyzed data into machine-learning-ready features while preserving data integrity and preventing information leakage.

**File**: `preprocessing.ipynb`

### Steps Performed

#### 1. **Feature Selection**
- Applied domain knowledge to select relevant features
- Removed highly correlated features (correlation threshold: [value])
- [Any feature importance analysis results]

#### 2. **Scaling & Normalization**
- Applied [StandardScaler/MinMaxScaler/other] to numeric features
- Rationale: [Explain why this scaling was chosen]

#### 3. **Encoding Categorical Variables**
- [One-hot encoding/Label encoding/Target encoding] for categorical features
- Handling of [specific categorical challenges]

#### 4. **Missing Value Imputation**
- Strategy: [Describe imputation method: mean, median, KNN, etc.]
- Reasoning: [Why this strategy was selected]
- Features affected: [List key features]

#### 5. **Outlier Handling**
- Detection method: [IQR method/Z-score/other]
- Treatment approach: [Removal/capping/transformation]
- [Impact on data distribution]

#### 6. **Train-Test Split Verification**
- Ensured no data leakage between train and test sets
- Verified stratification (if applicable)
- Checked feature distributions across splits

### Data Quality Metrics
| Metric | Train Set | Test Set |
|--------|-----------|----------|
| Record Count | [N] | [N] |
| Missing Values (%) | [%] | [%] |
| Feature Dimensions | [N] | [N] |

### Output
- Preprocessed training features: `[filename]`
- Preprocessed test features: `[filename]`
- Preprocessing pipeline/scaler objects: `[filename]`

---

## Modeling

### Overview
Multiple machine learning models were developed to [**insert your predictive/analytical objective**]. This ensemble approach allows for robust performance evaluation and comparison.

**File**: `modeling.ipynb`

### Models Developed

#### 1. **[Model Name 1]** (e.g., Logistic Regression)
- **Type**: [Classification/Regression]
- **Purpose**: [Why this model was chosen]
- **Hyperparameters**: [Key parameters used]
- **Rationale**: [Domain-specific considerations]

#### 2. **[Model Name 2]** (e.g., Random Forest)
- **Type**: [Classification/Regression]
- **Purpose**: [Why this model was chosen]
- **Hyperparameters**: [Key parameters used]
- **Rationale**: [Domain-specific considerations]

#### 3. **[Model Name 3]** (e.g., Gradient Boosting)
- **Type**: [Classification/Regression]
- **Purpose**: [Why this model was chosen]
- **Hyperparameters**: [Key parameters used]
- **Rationale**: [Domain-specific considerations]

#### 4. **[Model Name 4]**
- **Type**: [Classification/Regression]
- **Purpose**: [Why this model was chosen]
- **Hyperparameters**: [Key parameters used]

#### 5. **[Model Name 5]**
- **Type**: [Classification/Regression]
- **Purpose**: [Why this model was chosen]
- **Hyperparameters**: [Key parameters used]

#### 6. **[Model Name 6]**
- **Type**: [Classification/Regression]
- **Purpose**: [Why this model was chosen]
- **Hyperparameters**: [Key parameters used]

### Model Training Strategy
- **Cross-Validation**: [e.g., 5-fold cross-validation]
- **Hyperparameter Tuning**: [Grid search/Random search/Bayesian optimization]
- **Class Imbalance Handling** (if applicable): [SMOTE/class weights/other]

### Model Evaluation
- **Train/Validation/Test Split**: [Specify proportions]
- **Evaluation Metrics**: [e.g., Accuracy, Precision, Recall, F1, AUC, RMSE, MAE]
- **Cross-validation Results**: [Summary of fold performance]

---

## Results & Findings

### Model Performance Comparison

| Model | Metric 1 | Metric 2 | Metric 3 | Rank |
|-------|----------|----------|----------|------|
| [Model 1] | [Score] | [Score] | [Score] | [1-6] |
| [Model 2] | [Score] | [Score] | [Score] | [1-6] |
| [Model 3] | [Score] | [Score] | [Score] | [1-6] |
| [Model 4] | [Score] | [Score] | [Score] | [1-6] |
| [Model 5] | [Score] | [Score] | [Score] | [1-6] |
| [Model 6] | [Score] | [Score] | [Score] | [1-6] |

### Best Performing Model
- **Model**: [Name]
- **Key Metrics**: 
  - [Metric 1]: [Value]
  - [Metric 2]: [Value]
  - [Metric 3]: [Value]
- **Why It Performs Best**: [Explanation of success factors]

### Feature Importance Analysis
**Top 10 Most Influential Features** (for tree-based models):
1. [Feature] - [Importance %]
2. [Feature] - [Importance %]
3. [Feature] - [Importance %]
4. [Feature] - [Importance %]
5. [Feature] - [Importance %]
6. [Feature] - [Importance %]
7. [Feature] - [Importance %]
8. [Feature] - [Importance %]
9. [Feature] - [Importance %]
10. [Feature] - [Importance %]

### Model Insights
- **Key Insight 1**: [Interpretation of model behavior and business implications]
- **Key Insight 2**: [Interpretation of model behavior and business implications]
- **Key Insight 3**: [Interpretation of model behavior and business implications]

### Performance Metrics File
Detailed metrics are available in: `model_metrics.txt`

---

## Conclusion

### Summary of Findings
This project successfully analyzed [number] records from the FEMA NFIP dataset to [state your objective]. Through systematic data exploration, preprocessing, and modeling, we developed six distinct machine learning models to [describe what the models do].

### Key Achievements
1. **Data Processing**: Successfully sampled and cleaned [number] records from a 70+ million row dataset
2. **Analysis**: Identified [X] key patterns and relationships in NFIP policy data
3. **Modeling**: Developed 6 models with [best metric value] achieved on [metric name]
4. **Insights**: Generated [number] actionable insights for [stakeholders/use cases]

### Business Impact
- **Operational**: [How these findings improve operations]
- **Strategic**: [Strategic implications]
- **Risk Management**: [Risk insights or improvements]

### Limitations
- [Limitation 1 and mitigation]
- [Limitation 2 and mitigation]
- [Limitation 3 and mitigation]

### Model Reliability & Considerations
- Best performing model shows [metric] performance on test data
- Model is suitable for [specific use cases]
- Consider [specific caveats] when deploying this model
- Regular retraining recommended [frequency] due to [reasons]

---

## Future Steps

### Short-term Improvements (Next 1-3 months)
1. **Model Enhancement**
   - Implement ensemble techniques (stacking, voting) to improve performance
   - Conduct more extensive hyperparameter tuning
   - Explore deep learning approaches

2. **Feature Engineering**
   - Create additional domain-specific features based on stakeholder feedback
   - Investigate non-linear feature transformations
   - Develop interaction terms for key variable combinations

3. **Data Expansion**
   - Incorporate additional external data sources (weather, demographic data)
   - Extend temporal analysis with historical trend data
   - Increase sample size for improved generalization

### Medium-term Initiatives (3-12 months)
1. **Productionization**
   - Develop API endpoints for model inference
   - Create monitoring and alert systems for model performance degradation
   - Implement automated retraining pipeline

2. **Advanced Analytics**
   - Conduct causal inference analysis
   - Perform clustering analysis for policy segmentation
   - Develop scenario planning models

3. **Stakeholder Integration**
   - Deploy interactive dashboards for business users
   - Establish feedback loops with FEMA analysts
   - Create documentation for non-technical stakeholders

### Long-term Vision (12+ months)
1. **Real-time System**
   - Build real-time prediction system for incoming policies
   - Integrate with existing FEMA systems
   - Develop mobile-friendly interfaces

2. **Advanced Techniques**
   - Incorporate reinforcement learning for dynamic policy optimization
   - Explore graph neural networks for relational data
   - Develop explainable AI (XAI) frameworks

3. **Research Opportunities**
   - Publish findings in peer-reviewed journals
   - Collaborate with academic institutions
   - Contribute findings to FEMA policy discussions

### Technical Debt & Maintenance
- [ ] Code refactoring and modularity improvements
- [ ] Comprehensive test suite development
- [ ] Documentation updates
- [ ] Pipeline optimization for scalability

---

## Project Structure

```
Capstone2_FEMA_NFIPD/
├── README.md                          # This file
├── sample.ipynb                        # Data sampling from 70M+ row dataset
├── datawrangling.ipynb                 # Data cleaning and preparation
├── eda.ipynb                           # Exploratory data analysis
├── preprocessing.ipynb                 # Feature engineering & preprocessing
├── modeling.ipynb                      # Model development & evaluation
├── model_metrics.txt                   # Detailed model performance metrics
├── data/
│   ├── FimaNfipPoliciesV2.parquet     # Original dataset (sampled)
│   ├── train_data_clean.parquet       # Cleaned training data
│   ├── test_data_clean.parquet        # Cleaned test data
│   ├── train_data_processed.parquet   # Preprocessed training data
│   └── test_data_processed.parquet    # Preprocessed test data
├── models/
│   ├── model1.pkl                     # Serialized model 1
│   ├── model2.pkl                     # Serialized model 2
│   ├── model3.pkl                     # Serialized model 3
│   ├── model4.pkl                     # Serialized model 4
│   ├── model5.pkl                     # Serialized model 5
│   └── model6.pkl                     # Serialized model 6
├── output/
│   ├── eda_visualizations/            # EDA charts and plots
│   └── model_comparison.csv           # Model performance comparison
└── requirements.txt                    # Python dependencies
```

---

## Getting Started

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Required libraries: see `requirements.txt`

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/robertwzhou/Capstone2_FEMA_NFIPD.git
   cd Capstone2_FEMA_NFIPD
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

### Running the Analysis

1. **Start Jupyter**
   ```bash
   jupyter notebook
   ```

2. **Execute notebooks in order**
   - `sample.ipynb` - Data sampling
   - `datawrangling.ipynb` - Data preparation
   - `eda.ipynb` - Exploratory analysis
   - `preprocessing.ipynb` - Feature engineering
   - `modeling.ipynb` - Model development

### Key Files
- **Model Metrics**: View detailed performance in `model_metrics.txt`
- **Visualizations**: Check `output/eda_visualizations/` for charts and plots
- **Data**: Raw and processed datasets in `data/` directory

---

## Contact & Support

**Project Owner**: Robert W. Zhou  
**GitHub**: [@robertwzhou](https://github.com/robertwzhou)  
**Repository**: [Capstone2_FEMA_NFIPD](https://github.com/robertwzhou/Capstone2_FEMA_NFIPD)

### Questions or Feedback?
- Open an issue on GitHub
- Check existing documentation in this README
- Review individual notebook comments for detailed methodology

---

## License
[Specify your license - MIT, Apache 2.0, etc., or note if using public FEMA data]

## Acknowledgments
- Data source: [FEMA OpenFEM Platform](https://www.fema.gov/openfem)
- [Any collaborators or institutions]
- [Any references or papers used]

---

**Last Updated**: May 18, 2026  
**Project Status**: [In Progress / Completed / Archived]
