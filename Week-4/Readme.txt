Week 4: Predictive Modeling and Optimization in Logistics Systems

Objective
Predict shipment delivery time in days and evaluate how model outputs can support logistics planning.

Dataset
Uses the hypothetical dataset created for Week 3: week3_hypothetical_logistics_dataset.csv.

Target
delivery_time_days

Features
distance_km, shipment_volume_units, transport_cost_inr, promised_delivery_days, transport_mode, and region.

Models
- Linear Regression (baseline)
- Decision Tree Regressor
- Random Forest Regressor

Evaluation
Uses MAE, 
RMSE, 
R-squared, 
five-fold cross-validation on training data,  
GridSearchCV for Random Forest tuning. 
A held-out 20% test split is kept for final evaluation.

Files
- Week4_Predictive_Modeling_Logistics.ipynb: Google Colab notebook
- week4_predictive_modeling.py: standalone Python script
- Week4_Predictive_Modeling_Logistics_Report.docx: detailed report
- week4_model_comparison.csv: model comparison results
- week4_test_predictions.csv: actual and predicted test values
- week3_hypothetical_logistics_dataset.csv: input dataset

Important limitation
The data is hypothetical and small. Metrics demonstrate a workflow and should not be interpreted as real-world model guarantees. Validate any operational changes on actual shipment data before deployment.