Week 4: Predictive Modeling and Optimization in Logistics Systems
Project Overview
This project uses Python and machine learning to predict shipment delivery time from a hypothetical logistics dataset. It compares regression models and presents practical recommendations for improving delivery planning and logistics efficiency.
Objectives
- Prepare logistics data for predictive modeling.
- Predict delivery time in days.
- Train and compare Linear Regression, Decision Tree, and Random Forest models.
- Evaluate models using MAE, RMSE, and R² score.
- Apply five-fold cross-validation and Random Forest hyperparameter tuning.
- Suggest data-driven logistics optimization strategies.
Dataset
The project uses week3_hypothetical_logistics_dataset.csv, the hypothetical logistics dataset prepared for the previous week's analysis.

Target variable: delivery_time_days

Input features:
- distance_km
- shipment_volume_units
- transport_cost_inr
- promised_delivery_days
- transport_mode
- region
Identifiers and outcome-derived fields are not used as model inputs.
Models Used
1. Linear Regression — baseline model that is easy to interpret.
2. Decision Tree Regressor — captures non-linear relationships.
3. Random Forest Regressor — combines multiple decision trees and is tuned using GridSearchCV.
Methodology
1. Load and inspect the dataset.
2. Select the target and relevant input features.
3. Split the data into training and test sets (80/20).
4. Handle missing values, scale numeric features, and one-hot encode categorical features using a preprocessing pipeline.
5. Train the three regression models.
6. Compare model performance using a held-out test set and five-fold cross-validation.
7. Tune Random Forest hyperparameters using GridSearchCV on the training data.
8. Review predictions and develop optimization recommendations.
Evaluation Metrics
- MAE (Mean Absolute Error): average absolute prediction error, measured in days.
- RMSE (Root Mean Squared Error): error metric that gives greater weight to larger prediction errors, measured in days.
- R² score: measures how well the model explains variation in delivery time.
- Five-fold cross-validation RMSE: helps assess performance stability across different training/validation folds.
Run the notebook or script to generate the model results. Make sure any metrics included in the report match the latest run.
Optimization Recommendations
- Flag shipments when predicted delivery time may exceed the promised delivery window.
- Review long-distance shipments and transport modes or regions with higher observed delivery times.
- Consider delivery performance and transportation cost together when comparing options.
- Collect additional real-world features such as route, weather, dispatch time, vehicle capacity, and hub delays.
- Test proposed changes on a small pilot and compare delivery time, on-time delivery rate, and cost before wider rollout.
Project Files
- Week4_Predictive_Modeling_Logistics.ipynb — notebook for Google Colab/Jupyter.
- week4_predictive_modeling.py — standalone Python script.
- Week4_Predictive_Modeling_Logistics_Report.docx — detailed project report.
- Week4_Short_Logistics_Report.docx — short project report.
- week4_model_comparison.csv — model comparison results.
- week4_test_predictions.csv — actual and predicted test values.
- week4_model_comparison.png — model comparison visualization.
- week3_hypothetical_logistics_dataset.csv — input dataset used by the Week 4 project.
How to Run
Google Colab
1. Upload Week4_Predictive_Modeling_Logistics.ipynb to Google Colab.
2. Upload week3_hypothetical_logistics_dataset.csv when the notebook requests it, or update the dataset path in the notebook.
3. Run all cells from top to bottom.
4. Review the model comparison, evaluation metrics, and test predictions.
Local Python
1. Install Python and the required libraries:pip install pandas numpy matplotlib scikit-learn
2. Keep the Python script and dataset in the same folder, or update the dataset path in the script.
3. Run:python week4_predictive_modeling.py
Limitations
The dataset is hypothetical and limited in size. Its results demonstrate the machine-learning workflow and may not reflect actual logistics operations. Validate model performance and recommendations using real shipment data before applying them in practice.
Conclusion
This project demonstrates a predictive workflow for delivery-time forecasting, compares three regression models, and suggests ways to use predictions for logistics planning. Real operational data and further validation are required before deployment.
