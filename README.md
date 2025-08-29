# Uber Request Data Analysis

## Overview
This project analyzes Uber request data to identify patterns in ride requests, cancellations, and cases where no cars were available. The workflow includes **data cleaning, feature engineering, exploratory visualization, and classification**.

## Dataset
- Uber request dataset with details such as:
  - Request timestamp
  - Drop timestamp
  - Pickup point (City / Airport)
  - Driver ID (if assigned)
  - Status (Trip Completed, Cancelled, No Cars Available)

## Data Cleaning & Feature Engineering
- Removed null columns that carried no useful information.
- Split dataset into three subsets: **Completed, Cancelled, No Cars Available**.
- Extracted features like: **hour, day of week, and date** from timestamps.

## Machine Learning Approach
- Used **Decision Tree Classifier** for simplicity and interpretability.
- Encoded categorical variables using **Label Encoding / One-Hot Encoding**.
- Train-test split performed to evaluate generalization.
- Achieved high accuracy after dropping leakage columns and keeping only valid request-time features.

## Results
- Identified **peak demand periods** where cancellations and no-car cases were high.
- Showed clear differences between **Airport vs City pickup patterns**.
- Decision tree classification yielded strong performance, though simpler baselines (like rules on pickup location + hour) could already explain much of the variance.

## How to Run
1. Open the notebook in **Google Colab** or Jupyter.
2. Install requirements if needed:
   ```bash
   pip install pandas scikit-learn matplotlib seaborn
   ```
3. Run cells step by step for cleaning, visualization, and modeling.

## Files
- `Uber Dataset Analysis.ipynb`  Jupyter notebook with full analysis.
