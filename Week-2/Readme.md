# Week 2: Data Collection, Cleaning, and Preprocessing for Logistics Analysis

## Project Overview

This project focuses on preparing logistics data for analysis using Python. It includes dataset inspection, data cleaning, date conversion, delivery-time calculation, outlier detection, data scaling, visualization, and exporting the processed dataset.

The main goal is to improve data consistency and prepare the dataset for further logistics analysis.

## Objectives

- Inspect the dataset structure and data types.
- Identify missing values and duplicate records.
- Remove exact duplicate rows.
- Convert date columns into datetime format.
- Calculate delivery duration in days.
- Detect potential outliers using the IQR method.
- Apply Min-Max normalization and Z-score standardization.
- Visualize delivery-time distribution.
- Verify and export the processed dataset.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

## Dataset

The notebook expects a CSV file named `logistics_sample_data.csv`.

Expected Google Drive path:

`/content/drive/MyDrive/CSV/logistics_sample_data.csv`

The dataset includes date fields and numerical logistics features used for preprocessing. The exact dataset source and license should be added after verifying where the CSV file originated.

## Project Workflow

### 1. Data Inspection
Inspect dataset dimensions, sample records, data types, missing values, duplicate rows, and descriptive statistics.

### 2. Data Cleaning
Remove exact duplicate records and check missing values.

### 3. Date Conversion
Convert `order_date`, `actual_delivery_date`, and `promised_date` into datetime format.

### 4. Feature Engineering
Calculate delivery duration in days using the order date and actual delivery date.

### 5. Outlier Detection
Use the Interquartile Range (IQR) method to flag potential outliers in:
- `distance_km`
- `delivery_time_days`
- `delivery_cost`
- `unit_cost`

Potential outliers are flagged for investigation and are not automatically removed.

### 6. Data Scaling
Apply:
- **Min-Max Normalization** to scale values, generally between 0 and 1.
- **Z-Score Standardization** to transform values based on their mean and standard deviation.

### 7. Visualization
Create a histogram of delivery duration using Matplotlib to examine the distribution of delivery times.

### 8. Export
Verify the processed dataset and export it as:

`logistics_cleaned_preprocessed.csv`

## How to Run the Project

1. Open the notebook in Google Colab.
2. Upload `logistics_sample_data.csv` to the expected Google Drive folder, or update the dataset path in the notebook.
3. Mount Google Drive if required.
4. Run the notebook cells in order.
5. Review the cleaning, outlier detection, scaling, and visualization outputs.
6. Download the generated CSV file from the Colab Files panel.

## Expected Output

- A cleaned and preprocessed logistics dataset.
- Delivery-duration feature.
- Potential outlier counts for selected numerical columns.
- Normalized and standardized numerical features.
- A histogram showing delivery-time distribution.
- An exported CSV file.

Actual row counts, missing-value counts, and outlier counts should be documented after successfully running the notebook.

## Limitations

- The original dataset source and license must be verified.
- Invalid dates may result in missing delivery-duration values.
- Potential outliers may represent genuine logistics events.
- Further analysis is required to explain delivery delays and evaluate operational performance.

## Conclusion

This project demonstrates a practical logistics data-preprocessing workflow using Python. The techniques help improve data consistency and prepare logistics records for further analysis, delivery performance evaluation, and supply chain decision-making.

