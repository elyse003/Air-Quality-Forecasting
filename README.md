# Air Quality Forecasting with RNN/LSTM

This project implements Recurrent Neural Networks (RNNs) and Long Short-Term Memory (LSTM) models to forecast PM2.5 air pollution concentrations in Beijing using historical air quality and weather data.

## Project Overview

Air pollution, particularly PM2.5, is a critical global issue impacting public health and urban planning. This project uses time series forecasting techniques to predict PM2.5 concentrations, enabling governments and communities to take timely mitigation actions.

## Dataset

The dataset contains historical air quality and weather data for Beijing:
- **train.csv**: Training data with features and PM2.5 target values
- **test.csv**: Test data for generating predictions
- **sample_submission.csv**: Submission format template

## Project Structure

```
.
├── data/                    # Directory for dataset files (train.csv, test.csv, sample_submission.csv)
├── notebooks/               # Jupyter notebooks
│   └── air_quality_forecasting_starter_code.ipynb
├── outputs/                 # Generated predictions and visualizations
│   └── best_model_training_history.png
│   └── experiment_results.png
│   └── experiment_results.csv
│   └── submission.csv
├── requirements.txt         
└── README.md               
```

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Installation

1. Clone this repository:
```bash
git clone <https://github.com/elyse003/Air-Quality-Forecasting.git>
cd air-quality-forecasting
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

3. Download the dataset from Kaggle:
   - Access the competition: [Air Quality Forecasting Challenge](https://www.kaggle.com/competitions/air-quality-forecasting)
   - Download `train.csv`, `test.csv`, and `sample_submission.csv`
   - Place them in the `data/` directory

### Running the Notebook

1. Start Jupyter Notebook:
```bash
jupyter notebook
```

2. Open `notebooks/air_quality_forecasting_starter_code.ipynb`

3. Execute all cells to:
   - Load and explore the data
   - Preprocess the data
   - Train RNN/LSTM models
   - Generate predictions for submission

## Model Architecture

The project implements multiple LSTM architectures with various hyperparameters:

- **Input Layer**: Sequence of historical features (air quality and weather data)
- **LSTM Layers**: One or more LSTM layers with dropout for regularization
- **Dense Layers**: Fully connected layers for final prediction
- **Output Layer**: Single neuron predicting PM2.5 concentration

## Experiments

The notebook includes 15+ experiments with variations in:
- Number of LSTM layers and units
- Dropout rates
- Learning rates and optimizers
- Batch sizes
- Sequence lengths (time windows)
- Activation functions

Results are tracked in an experiment table comparing RMSE across configurations.

## Results

Model performance is evaluated using Root Mean Squared Error (RMSE):
- **Target**: RMSE < 4000
- **Exemplary**: RMSE < 3000

## Submission

1. Generate predictions using the trained model
2. Format predictions according to `sample_submission.csv`
3. Submit to Kaggle competition: [Air Quality Forecasting Challenge](https://www.kaggle.com/competitions/air-quality-forecasting)

## Key Features

- Comprehensive data exploration and visualization
- Robust preprocessing pipeline with missing value handling
- Time series sequence creation for RNN/LSTM input
- Multiple model architectures with hyperparameter tuning
- Experiment tracking and result analysis
- Well-documented code with explanations

## Report

A comprehensive report includes:
- Introduction and problem description
- Data exploration and preprocessing details
- Model architecture justification
- Experiment table with 15+ configurations
- Results analysis and discussion
- Conclusions and future improvements

## Citation

This project is part of the Machine Learning Techniques I course assignment on Time Series Forecasting using RNN/LSTM models.

## License

This project is for educational purposes only.
