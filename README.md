# AirBnB Data Analysis & Preprocessing Tutorial

[![Codespaces Prebuilds](https://github.com/gperdrizet/gperdrizet-data-preprocessing-project-tutorial/actions/workflows/codespaces/create_codespaces_prebuilds/badge.svg)](https://github.com/gperdrizet/gperdrizet-data-preprocessing-project-tutorial/actions/workflows/codespaces/create_codespaces_prebuilds)

A comprehensive data science project focused on exploratory data analysis (EDA) and data preprocessing using real AirBnB NYC 2019 dataset. This project demonstrates essential data cleaning, exploration, and feature engineering techniques through practical exercises with real-world data.

## Project Overview

This project analyzes **48,895 AirBnB listings** from New York City (2019) and provides hands-on experience with:

- Data loading and exploration
- Statistical analysis and distribution analysis
- Feature relationship investigation using appropriate statistical tests
- Data cleaning and null value handling
- Feature engineering and preprocessing
- Advanced visualization techniques


## Getting Started

### Option 1: GitHub Codespaces (Recommended)

1. **Fork the Repository**
   - Click the "Fork" button on the top right of the GitHub repository page
   - Give the fork a descriptive name including your GitHub username
   - Click "Create fork"
   - Bookmark or save the link to your fork

2. **Create a GitHub Codespace**
   - On your forked repository, click the "Code" button
   - Select "Create codespace on main"
   - Wait for the environment to load (dependencies are pre-installed)

3. **Start Working**
   - Open `notebooks/MVP.ipynb` to begin the assignment
   - Refer to `notebooks/instructions.md` for detailed requirements
   - Check the `full_solution/` folder for complete examples

### Option 2: Local Development

1. **Prerequisites**
   - Git
   - Python >= 3.10

2. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/gperdrizet-data-preprocessing-project-tutorial.git
   cd gperdrizet-data-preprocessing-project-tutorial
   ```

3. **Set Up Environment**
   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

4. **Launch Jupyter & start the notebook**
   ```bash
   jupyter notebook notebooks/MVP.ipynb
   ```

## Project Structure

```
├── .devcontainer/                       # Development container configuration
├── notebooks/                           # Jupyter notebook directory
│   ├── MVP.ipynb                        # Assignment notebook
│   ├── MVP_solution.ipynb               # Solution notebook
│   ├── instructions.md                  # Detailed assignment instructions
│   └── full_solution/                   # Detailed solution notebooks
│       ├── 01_distributions.ipynb
│       ├── 02_correlations.ipynb
│       ├── 03_data_cleaning.ipynb
│       ├── 04_feature_engineering.ipynb
│       └── functions.py
│
├── .gitignore                           # Files/directories not tracked by git
├── requirements.txt                     # Python dependencies
└── README.md                            # Project documentation
```


## Dataset

The dataset contains **48,895 AirBnB listings** from New York City (2019) with the following key features:
- **Price**: Property prices in USD
- **Location**: Hierarchical location data (latitude, longitude, neighbourhood_group, neighbourhood)
- **Listing Details**: room_type, minimum_nights, availability_365
- **Host Information**: host_name, calculated_host_listings_count
- **Review Data**: number_of_reviews, last_review, reviews_per_month
- **Identifiers**: id, name

**Note**: The dataset is automatically loaded from the web in the notebooks, so no manual download is required.


## Learning Objectives

By completing this tutorial, students will learn to:

1. **Analyze Data Distributions**
   - Generate descriptive statistics for numerical and categorical features
   - Create appropriate visualizations (histograms, bar plots, scatter plots)
   - Identify data quality issues and extreme values

2. **Investigate Feature Relationships**
   - Apply Chi-squared tests for categorical-categorical relationships
   - Use Kruskal-Wallis H-tests for categorical-numerical relationships
   - Calculate Spearman/Kendall correlations for numerical-numerical relationships

3. **Clean and Preprocess Data**
   - Select relevant features for modeling
   - Handle missing values using various imputation strategies
   - Address extreme values and outliers appropriately

4. **Engineer Features**
   - Apply one-hot encoding to categorical variables
   - Transform skewed distributions using Box-Cox transformation
   - Create polynomial features to capture non-linear relationships


## Solution Reference

The solution to the MVP notebook can be found in `MVP_solution.ipynb`. The `solution/` folder contains more professional-level implementations with experimentation to evaluate alternative approaches:

- **`01_distributions.ipynb`**: Comprehensive EDA with detailed analysis of each feature
- **`02_correlations.ipynb`**: Statistical testing and relationship analysis
- **`03_data_cleaning.ipynb`**: Systematic comparison of cleaning strategies
- **`04_feature_engineering.ipynb`**: Advanced preprocessing achieving 60% explained variance

Each solution notebook includes:
- Clear goal statements for each section
- Professional visualizations and statistical analysis
- Detailed interpretation of results
- Best practices for data science workflows


## Key Technologies

- **Python 3.8+**
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib & Seaborn**: Data visualization
- **Scikit-learn**: Machine learning and preprocessing
- **SciPy**: Statistical testing
- **Jupyter Notebook**: Interactive development environment


## Contributing

This is an educational repository. Students should work on their forked copies. If you find issues or have suggestions for improvements, please open an issue or submit a pull request.