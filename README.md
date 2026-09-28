# Logistics Delivery Delay Analysis

## Project Overview

This project analyzes logistics and delivery data to identify factors that contribute to delivery delays and operational bottlenecks.

The analysis focuses on delivery performance across different delivery partners, transport modes, regions, weather conditions, package types, and shipment characteristics.

A **Random Forest classification model** is developed to predict whether a shipment is likely to be delayed.

## Objectives

* Clean and validate the logistics dataset
* Perform exploratory data analysis
* Calculate delivery delay duration
* Analyze delivery performance across transport modes
* Identify delivery partners with higher delay rates
* Investigate the relationship between shipment volume and delays
* Analyze the effect of weather and region on delivery performance
* Identify important factors contributing to delivery delays
* Build and evaluate a Random Forest classification model
* Generate a prioritized list of shipments based on predicted delay probability
* Recommend practical operational improvements

## Dataset

The dataset contains **25,000 delivery records** with information including:

* Delivery ID
* Delivery Partner
* Package Type
* Vehicle Type
* Delivery Mode
* Region
* Weather Condition
* Distance
* Package Weight
* Actual Delivery Time
* Expected Delivery Time
* Delay Status
* Delivery Status
* Delivery Rating
* Delivery Cost

## Machine Learning Algorithm

**Random Forest Classifier**

The model predicts:

```text
0 → On Time
1 → Delayed
```

The model is evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Confusion Matrix

## Project Workflow

```text
Data Collection
      ↓
Data Cleaning & Validation
      ↓
Exploratory Data Analysis
      ↓
Delay Duration Calculation
      ↓
Transport Mode Analysis
      ↓
Delivery Partner Bottleneck Analysis
      ↓
Shipment Volume Analysis
      ↓
Random Forest Model
      ↓
Model Evaluation
      ↓
Feature Importance
      ↓
Delay Priority List
      ↓
Operational Recommendations
```

## Visualizations

The project includes four major visualizations:

1. Distribution of Delivery Status
2. Average Delivery Time by Transport Mode
3. Average Delay by Delivery Partner
4. Shipment Volume vs Average Delay

Additional analysis is performed for weather conditions, regions, vehicle types, and other operational factors.

## Key Outputs

### 1. Random Forest Model

A trained Random Forest model is used to predict delivery delays.

### 2. Feature Importance

Feature importance is analyzed to identify the variables that contribute most to delay prediction.

### 3. Bottleneck Analysis

Delivery partners are compared using:

* Average delivery time
* Average delay
* Shipment volume
* Delay rate

### 4. Prioritized Delay List

Shipments are ranked according to their predicted probability of being delayed.

The output file is:

```text
prioritized_delay_list.csv
```

### 5. Bottleneck Analysis File

Operational partner-level analysis is saved as:

```text
delivery_partner_bottleneck_analysis.csv
```

## Dataset Limitation

The selected dataset does not contain individual warehouse identifiers or separate pickup, sorting, and dispatch timestamps.

Therefore, **delivery partner** is used as the operational unit for bottleneck analysis, while actual delivery time and expected delivery time are used to calculate delivery delay.

The analysis therefore focuses on delivery-level and operational-partner bottlenecks rather than individual warehouse-stage bottlenecks.

## Practical Recommendations

Based on the analysis, logistics operations can:

* Monitor delivery partners with consistently high delay rates
* Review transport modes associated with longer delivery times
* Monitor shipment volume for potential operational overload
* Consider weather conditions when planning deliveries
* Prioritize shipments with high predicted delay probability
* Use model feature importance to identify areas requiring operational attention
* Continuously update the model using new delivery records

## Files

```text
DS_Day01_24_Logistics_Delay_Analysis.ipynb
prioritized_delay_list.csv
delivery_partner_bottleneck_analysis.csv
README.md
```

## Conclusion

This project applies data analysis and Random Forest machine learning to logistics delivery data to understand delivery delays and identify operational bottlenecks. The resulting analysis provides insights into delivery performance and produces a prioritized list of shipments that may require proactive monitoring.
