# Wake County Housing Analysis

## Overview

This was a team-based data analytics project completed as a part of the Data Analytics Club at NC State. The project focused on analyzing the Wake County housing market, with the goal of identifying factors that influence housing prices and properties with potential investment opportunities.

The project used housing data through a Zillow-scraper, Python for data cleaning and analysis, geospatial clustering, and an XGBoost regression model to predict housing prices.

## Research Questions

- What factors are most important when evaluating a property?
- What housing features are associated with higher housing prices?
- Which properties appear to be priced under their model-predicted value?

## Data

The dataset was collected through the use of a Zillow search scraper and cleaned using Python.

The analysis included housing and geographic variables such as:

- City/Town
- Interior Square Footage
- Number of Baths
- Number of Beds
- X Coordinate
- Y Coordinate
- Geographic Cluster
- Walk Index
- Price

The target variable for the XGBoost model was the log-transformed housing price.

(The Zillow scraped dataset is not included due to data-source and redistribution restrictions).

## Programming Languages, Libraries, & Algorithms Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- GeoPandas
- K-Means Clustering

## Methodology

### 1. Data Cleaning

Housing data was cleaned through Python by removing missing values, zero-price observations, and outliers.

### 2. Geographic Clustering

To group properties based on their geographic locations, K-Means clustering was used. These geographic clusters were then integrated into the housing price model.

### 3. XGBoost Regression

An XGBoost regression model was used to predict housing prices.

Variables included:

- City/Town
- Interior Square Footage
- Number of Baths
- Number of Beds
- X Coordinate
- Y Coordinate
- Geographic Cluster
- Walk Index
- Price

The target variable was log-transformed price.

### 4. Investment Analysis

Actual housing prices from Zillow were compared with the model-predicted prices to identify properties that appeared to be priced lower than their predicted value.

An estimated ROI metric was calculated using the difference between the predicted and actual price.

## Model Performance

The XGBoost model achieved:

- Training R-squared: 0.8614
- Testing R-squared: 0.8257

The testing R-squared shows that the model explained 82.57% of the variation in the log-transformed housing prices in the test dataset.

## Findings

Geographic Cluster was the strongest factor in the model, with City and Interior Square Footage also having an impact.

Feature Importance:

1. Geographic Cluster - 38%
2. City - 30%
3. Interior Square Footage - 22%
4. X-Coordinate - 3%
5. Baths - 3%
6. Y-Coordinate - 2%
7. Walk Index - 1%
8. Beds - 1%

These findings suggest that the geographic location and interior square footage of a property have a signifigant impact on predicting housing prices.

## Investment Analysis

Additionally, the model was used to compare actual housing prices from Zillow with predicted prices.

The properties with predicted prices considerably higher than their actual prices were determined as potential investment opportunites.

Note: This analysis should be interpreted as "model-estimated potential upside", rather than a guaranteed return on investment.

## Limitations

- Accuracy of the model may decrease when applied to counties other than Wake County.
- The model doesn't take into account the qualitative factors that affect property price.
- The housing market is volatile, as changes in mortgage rates and new development can affect the housing market's conditions.
