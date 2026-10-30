# NewX Services – Inventory Management & Spare Parts Forecasting

**Project Reference:** PM-PR-0027
**Domain:** Inventory Management and Predictive Analytics

## Project Overview

This project focuses on analysing historical vehicle service and invoice data from NewX Services to understand service-item patterns and support inventory planning.

The objective is to identify frequently recorded service items, analyse monthly invoice activity, explore demand patterns, and evaluate forecasting approaches that can support better inventory-related decisions.

## Business Problem

Vehicle service centres need to maintain sufficient spare parts and service items to meet customer requirements. Poor inventory planning can result in stock shortages, service delays, or unnecessary inventory costs.

This project uses historical service and invoice records to identify recurring patterns and provide data-driven insights for inventory planning.

## Business Objectives

* Analyse historical vehicle service and invoice records.
* Identify frequently recorded service items.
* Understand monthly invoice activity and trends.
* Explore service-item demand patterns.
* Apply and evaluate forecasting approaches.
* Provide insights to support inventory planning.

## Dataset Description

The dataset was retrieved from the NewX Services project database.

* **Total Records:** 28,482
* **Total Columns:** 7
* **Data Period:** May 2017 – January 2019
* **Source Table:** `service_data`

### Dataset Columns

| Column                  | Description                                         |
| ----------------------- | --------------------------------------------------- |
| `invoice_date`          | Invoice date                                        |
| `job_card_date`         | Vehicle service job card date                       |
| `business_partner_name` | Customer or business partner identifier             |
| `vehicle_no`            | Vehicle registration identifier                     |
| `vehicle_model`         | Vehicle model                                       |
| `current_km_reading`    | Vehicle kilometre reading                           |
| `invoice_line_text`     | Item or service description recorded on the invoice |

## Tools and Technologies

* **Programming Language:** Python
* **Database:** MySQL
* **Libraries:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Database Connectivity:** SQLAlchemy
* **Machine Learning:** Scikit-learn
* **Environment:** Jupyter Notebook

## Project Workflow

1. **Database Connectivity:** Connected to the MySQL database and retrieved service records.
2. **Data Understanding:** Examined dataset structure, data types, missing values, and duplicate records.
3. **Data Cleaning:** Converted date and numeric columns, standardized item descriptions, and handled missing descriptions.
4. **Exploratory Data Analysis:** Analysed service records, item frequencies, vehicle-related patterns, and monthly invoice activity.
5. **Feature Preparation:** Prepared monthly time-based data for forecasting analysis.
6. **Forecasting:** Applied a baseline approach and Linear Regression to analyse monthly invoice-line record trends.
7. **Model Evaluation:** Compared forecasting predictions with actual monthly records using MAE and RMSE.
8. **Business Insights:** Summarized frequently recorded items and provided recommendations for inventory planning.

## Forecasting Evaluation

Monthly invoice-line record frequency was used as the forecasting target.

The forecasting approaches were evaluated on four test months from September to December 2018.

| Model             |    MAE |   RMSE |
| ----------------- | -----: | -----: |
| Baseline Model    | 451.75 | 484.97 |
| Linear Regression | 261.57 | 289.66 |

The Linear Regression model achieved lower MAE and RMSE than the baseline model on the selected test period.

These results indicate that the model performed better than the baseline for predicting monthly invoice-line record frequency on this test split.

## Key Insights

* Historical invoice records provide useful information about frequently recorded service items.
* Monthly invoice activity varies over time.
* Item frequency analysis can help identify service items that appear more often in historical records.
* Forecasting monthly invoice-line activity can provide an additional reference for inventory planning.
* Historical trends can support data-driven discussions about item availability and planning.

## Business Recommendations

* Monitor frequently recorded service items regularly.
* Use historical invoice trends as one input for inventory planning.
* Review item classifications with domain experts.
* Maintain accurate item-level quantity and stock records.
* Combine historical service activity with actual stock and consumption data for more reliable demand forecasting.

## Limitations

The available dataset does not contain explicit item quantity, stock-level, or actual consumption columns.

Therefore, invoice-line record frequency is used as a proxy for recorded item demand. It should not be interpreted as the actual quantity of spare parts sold or consumed.

The forecasting results represent monthly invoice-line activity rather than actual spare-part quantity demand.

Future improvements could include integrating inventory transactions, item quantities, stock availability, and consumption records to develop more accurate spare-parts demand forecasts.

## Conclusion

This project demonstrates how Python, SQL, exploratory data analysis, and forecasting techniques can be used to analyse historical vehicle service records.

By identifying frequently recorded items and examining monthly invoice activity, the project provides useful insights that can support inventory planning and data-driven decision-making at vehicle service centres.

---

**Project Type:** Client Project
**Project Reference:** PM-PR-0027
**Project Title:** NewX Services – Inventory Management & Spare Parts Forecasting
