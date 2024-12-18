# London Atmospheric Emissions Inventory Analysis

This repository contains a Jupyter notebook that tackles the problem of predicting atmospheric emissions in London given the emissions data for 2008, 2010, 2013, and 2020 specifically. The dataset was obtained from this link: https://data.london.gov.uk/dataset/london-atmospheric-emissions-inventory-2013. The dataset focuses on major road emissions only given the ease by which it was to record this information compared to rural roads.


## Notebook Overview

### Key Features:

1. <b>Import Libraries (EDA)</b>:
- Key libraries imported are pandas, numpy, scikit-learn, matplotlib, and torch.

2. <b>Load data and concatenate</b>:

- Individual files were loaded in using pandas
- We concatenated the data together since we plan to train on all the historical data to generate predictions.

3. <b>Format Columns</b>:
- Convert all object type columns to a numeric format by first encoding each label and then converting the values to their encoded value.

4. <b>Split Data</b>:
- Split the dataset so that any data that took place prior to 2020 would be considered historical and will be used for training while the rest of the data will be used as the test set for model evaluation.

5. <b>Train Models</b>:
- Trained a Linear Regression model
- Trained a Decision Tree Regressor model
- Trained a simple feed forward neural network

6. <b>Evaluate model performance</b>
- Used MSE, RMSE, MAE, and R2 score to evaluate model performances.

### Technologies Used:
- Deep Learning for Neural Network architecture and training
- Machine Learning regression algorithms
- Data visualization for interpretability

## Requirements
To run the notebook, install the following Python libraries:

- pandas
- matplotlib
- scikit-learn
- numpy
- torch

You can install the required libraries with:

`pip install pandas matplotlib scikit-learn numpy torch`

### How to Use
1. Clone the repository:

    `git clone https://github.com/Vimal-Raghubir London-Atmospheric-Emissions-Inventory-Analysis.git`

2. Open the Jupyter notebook:

    `jupyter notebook london_atmospheric_emissions_inventory_analysis.ipynb`

3. Follow the structured steps in the notebook to:
- Import the Libraries.
- Load data and concatenate.
- Format Columns.
- Split Data.
- Train Models
- Evaluate model performance

## Future Enhancements

Potential improvements to the notebook could include:

- Trying different regression algorithms like XGBoost.
- Adding more data from previous years not covered in the existing dataset like 2018, 2019, etc.
- Trying bucketing and using classification algorithms to see if it results in improved performance.