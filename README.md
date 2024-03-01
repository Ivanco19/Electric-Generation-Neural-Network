# Electricity Generation Prediction

## Introduction

This project aims to forecast electricity generation trends in Mexico using deep learning, specifically a recurrent neural network (RNN). Data from the Centro Nacional de Control de Energia (CENACE) was utilized to analyze and forecast electricity generation, with a focus on combined cycle technology. The dataset spans from 2021 to 2023, capturing recent trends and patterns.

## Contents
- `electric_analysis_preprocessing.ipynb`: Data cleaning, visualization and preprocessing steps.
- `neural_network_model.ipynb`: Model definition, training, and saving. Making predictions using the trained model.
- `electric_generation_cenace_2018-2023.csv`: Raw dataset.
- `electric_generation_model.csv`: Preprocessed dataset.
- `model_rnn.h5`: Saved trained model.

## Preprocessing

### Data Source
The dataset, obtained from the Centro Nacional de Control de Energía (CENACE), offers comprehensive insights into electricity generation across diverse technologies.

### Data Overview
* Visualizations indicate a consistent upward trajectory in electricity generation.
* A notable inflection point in 2020 is observed, potentially linked to the COVID-19 pandemic.
* Analysis highlights the dominance of combined cycle technology, contributing around 60% of total electricity generation.
* The neural network model is tailored to predict electricity generation for combined cycle plants.
* Utilizing data from the recent three years (2021-2023) ensures the model captures contemporary patterns.

## Project Structure

### 1. Preprocessing of Data:
* Loading and describing the dataset.
* Initial data visualization.
* Preprocessing steps, including sequence creation and MinMax scaling.
* Division into training and testing sets.

### 2. Neural Network Design and Training:
* Architecture Details:
    * Four layers with a dropout of 10% in each layer.
    * Initial layer: 50 neurons.
    * Second layer: 80 neurons.
    * Third layer: 50 neurons.
    * Final dense layer with one neuron.

* Compilation and Training:
    * Utilization of LSTM layers for sequence modeling.
    * Compilation and training of the model.
    * Visualization of error evolution over epochs.

### 3. Analysis of Results:
* Model predictions and creation of a DataFrame with real values and predictions.
* Calculation of relative errors and visualization.
* Performance evaluation metrics: 
    * RMSE = 417.304
    * R² = 97.7%
* Histogram depicting the distribution of relative errors.

### 4. Saving the trained model in h5 format.
* Saving the trained model in h5 format.
* Instructions on loading and using the model in the future.


## Conclusion

This project, employing deep learning techniques, delivers a comprehensive analysis and prediction of electricity generation in Mexico. The customized RNN model, focused on combined cycle technology, ensures accurate forecasts based on recent data. With an R² of 97.7% and an RMSE of 417.304, the model showcases remarkable predictive capabilities. The histogram illustrates that 80% of relative errors fall within the 0-2% range, demonstrating the model's high precision.
