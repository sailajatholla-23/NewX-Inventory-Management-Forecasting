# NewX Services – Inventory Management & Spare Parts Forecasting

## Project Overview

This project focuses on analysing historical vehicle service and invoice records to identify service activity patterns and explore forecasting approaches that can support inventory planning.

The project involves data cleaning, exploratory data analysis, monthly trend analysis, item-level frequency analysis, and forecasting model evaluation using Python and Machine Learning techniques.

## Project Objectives

* Analyse historical vehicle service and invoice records.
* Identify frequently recorded service-item descriptions.
* Understand monthly service activity and trends.
* Explore item-level record frequency for inventory planning.
* Compare forecasting approaches and evaluate their performance.

## Dataset Description

* Total Records: 28,482
* Unique Invoice-Line Descriptions: 495
* Data Period: May 2017 – January 2019
* Data Source: MySQL Database

The dataset contains vehicle service and invoice-related information.

## Technologies Used

* Python
* SQL
* MySQL
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* SQLAlchemy

## Project Workflow

1. **Data Collection:** Retrieved vehicle service and invoice records from the MySQL database.
2. **Data Cleaning:** Inspected missing values, data types, duplicate records, and prepared the dataset for analysis.
3. **Exploratory Data Analysis:** Examined service trends, invoice records, vehicle models, and frequently recorded descriptions.
4. **Trend Analysis:** Analysed monthly service activity and item-level record frequencies.
5. **Feature Preparation:** Prepared monthly record-frequency data for forecasting.
6. **Model Development:** Implemented and evaluated Linear Regression against a baseline forecasting approach.
7. **Model Evaluation:** Compared model performance using MAE and RMSE.
8. **Insights:** Summarised findings relevant to inventory planning.

## Key Findings

* Analysed 28,482 vehicle service and invoice records.
* Identified 495 unique invoice-line descriptions.
* ENGINE OIL, CHAIN LUBRICATION, and GENERAL SERVICE were among the frequently recorded descriptions.
* December 2018 recorded the highest monthly frequency, with 2,260 records.
* Selected 10 possible spare-part descriptions for item-level monthly analysis.
* Linear Regression achieved better MAE than the baseline for 7 of the 10 selected item series.

### Forecasting Model Performance

| Model             |    MAE |   RMSE |
| ----------------- | -----: | -----: |
| Baseline          | 451.75 | 484.97 |
| Linear Regression | 402.04 | 436.50 |

Linear Regression achieved lower MAE and RMSE than the baseline for the overall monthly record-frequency series.

## Data Scope and Considerations

The available dataset contains vehicle service and invoice records but does not include actual spare-parts quantities, stock levels, consumption records, or supplier lead times.

Therefore, invoice-line record frequency was used as a proxy for recorded service activity during the forecasting process. The resulting forecasts provide insights into historical service-item frequency patterns and can support preliminary inventory planning analysis.

For more accurate spare-parts demand forecasting, future analysis could incorporate actual consumption quantities, inventory records, stock availability, and supplier lead-time information.

## Future Improvements

* Incorporate actual spare-parts consumption and quantity data.
* Integrate inventory and stock availability information.
* Include supplier lead times and stockout history.
* Explore additional forecasting techniques.
* Validate models using a longer historical period.

## Project Structure

* `NewX_Inventory_Management_Forecasting.ipynb` – Project implementation and analysis.
* `README.md` – Project documentation.
* `requirements.txt` – Required Python libraries.

## Author

**Sailaja Tholla**

B.Tech – Computer Science and Engineering


