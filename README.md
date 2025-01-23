# Sticker Sales Forecasting

This repository contains code and resources for participating in the Kaggle competition "Forecasting Sticker Sales."

## Competition Overview

The objective of the competition is to forecast sticker sales across various countries. Participants are required to predict the target variable `num_sold` for each `id` row in the test dataset. 

### Evaluation
The evaluation metric used is Mean Absolute Percentage Error [(MAPE)](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_percentage_error.html).

### Dataset Description
- **train.csv**: The training set with sales data for each `date-country-store-item` combination.
- **test.csv**: The test set for which predictions are to be made. The public leaderboard scores are based on the first year of the test data, while the private leaderboard scores on the remaining.
- **sample_submission.csv**: A sample file showing the correct format for submission.

### Submission Format
Each submission must include a header and adhere to the following format:
```
id,num_sold
230130,100
230131,100
230132,100
...
```
`
### Key Features of the Dataset
- **Synthetic Data**: The dataset is generated artificially but mimics real-world scenarios, including:
  - Weekend and holiday effects
  - Seasonality
  - Other real-world patterns

For more information, visit the [competition page](https://kaggle.com/competitions/playground-series-s5e1).

## Repository Structure and Notes

This repository includes:

1. **Exploratory Data Analysis (EDA)**
   - Visualization of seasonality, trends, and country-specific behaviors.
   - Analysis of weekend and holiday effects on sales.

2. **Model Development**
   - Various forecasting models tested, such as Linear Regression, Random Forest, and LightGBM.
   - Implementation of hyperparameter tuning to improve MAPE scores.

3. **Submission Pipeline**
   - A robust pipeline to generate submission files in the required format.

### Notes
- ? Holidays and weekends significantly impact sales trends; incorporating these features into the model improves performance.
- ? Feature engineering plays a crucial role in capturing seasonality and trends.
- ? Early experiments show that ensemble methods outperform standalone models.

## Getting Started
To reproduce the results, follow these steps:
1. Clone the repository:
   ```bash
   git clone <repo_url>
   cd <repo_name>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook or script for training and submission:
   ```bash
   python train_and_submit.py
   ```

## Citation
If you use this work, please cite the competition:
> Walter Reade and Elizabeth Park. Forecasting Sticker Sales. https://kaggle.com/competitions/playground-series-s5e1, 2025. Kaggle.

