# AirBnB Data Analysis & Preprocessing Tutorial

A comprehensive tutorial on exploratory data analysis (EDA) and data preprocessing using real AirBnB NYC 2019 dataset. This repository contains both assignment materials for bootcamp students and complete solution notebooks demonstrating professional data science workflows.

## Overview

This project guides students through the complete data preprocessing pipeline using real-world AirBnB listing data from New York City. Students will learn essential data science skills including:

- **Exploratory Data Analysis (EDA)**: Understanding data distributions, identifying patterns, and spotting anomalies
- **Feature Relationships**: Analyzing correlations and interactions between different types of variables
- **Data Cleaning**: Handling missing values, outliers, and data quality issues
- **Feature Engineering**: Encoding categorical variables, scaling features, and creating synthetic features
- **Statistical Testing**: Applying appropriate statistical methods for different data types

## Repository Structure

```
├── notebooks/
│   ├── MVP.ipynb                    # Assignment notebook for students
│   ├── MVP_solution.ipynb           # Competed MVP
│   └── instructions.md              # Detailed assignment instructions
├── solution/
│   ├── 01_distributions.ipynb       # EDA and feature distributions
│   ├── 02_correlations.ipynb        # Feature relationships analysis
│   ├── 03_data_cleaning.ipynb       # Data cleaning strategies
│   ├── 04_feature_engineering.ipynb # Advanced preprocessing
│   ├── functions.py                 # Helper functions
├── data/
│   └── processed/                   # Cleaned datasets 
└── requirements.txt                 # Python dependencies
```

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

## Getting Started

### Option 1: GitHub Codespaces (Recommended)

1. **Fork this repository** to your GitHub account:
   - Click the "Fork" button in the top-right corner of this repository
   - Select your GitHub account as the destination

2. **Start a GitHub Codespace**:
   - Go to your forked repository
   - Click the green "Code" button
   - Select the "Codespaces" tab
   - Click "Create codespace on main"
   - Wait for the environment to set up (2-3 minutes)

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Start working**:
   - Open `notebooks/MVP.ipynb` to begin the assignment
   - Refer to `notebooks/instructions.md` for detailed requirements
   - Check the `solution/` folder for complete examples

### Option 2: Local Setup

1. **Clone your forked repository**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/gperdrizet-data-preprocessing-project-tutorial.git
   cd gperdrizet-data-preprocessing-project-tutorial
   ```

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

## Dataset

The project uses the **AirBnB NYC 2019** dataset containing 48,895 listings with the following features:

- **Location**: `latitude`, `longitude`, `neighbourhood_group`, `neighbourhood`
- **Listing Details**: `room_type`, `price`, `minimum_nights`, `availability_365`
- **Host Information**: `host_name`, `calculated_host_listings_count`
- **Review Data**: `number_of_reviews`, `last_review`, `reviews_per_month`
- **Identifiers**: `id`, `name`

The dataset is automatically loaded from the web in the notebooks, so no manual download is required.

## Assignment Instructions

### For Students:

1. **Start with `notebooks/MVP.ipynb`** - This is your main assignment notebook
2. **Read `notebooks/instructions.md`** - Contains detailed requirements and hints
3. **Complete each section systematically**:
   - Section 1: Analyze individual feature distributions
   - Section 2: Investigate relationships between features
   - Section 3: Clean and preprocess the data
   - Section 4: Engineer new features

### Key Requirements:

- **Appropriate statistical methods**: Use the right tests for different data types
- **Clear visualizations**: Label axes, use appropriate scales, add titles
- **Justified decisions**: Explain your choices for handling missing values and outliers
- **Code documentation**: Comment your code and explain your reasoning

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

## Tips for Success

1. **Start Early**: This is a comprehensive assignment that requires time and thought
2. **Read the Instructions**: The `instructions.md` file contains important hints and requirements
3. **Understand the Data**: Spend time exploring the dataset before making decisions
4. **Justify Your Choices**: Data cleaning decisions should be based on domain knowledge and analysis goals
5. **Check the Solutions**: Use the solution notebooks as references, but try to solve problems independently first
6. **Experiment**: Try different approaches and compare their effectiveness

## Contributing

This is an educational repository. Students should work on their forked copies. If you find issues or have suggestions for improvements, please open an issue or submit a pull request.

---

**Happy Learning!**

This tutorial provides hands-on experience with real-world data science challenges. Take your time, experiment with different approaches, and don't be afraid to make mistakes - they're part of the learning process!
