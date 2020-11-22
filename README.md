# Anomaly-Detection
Anomaly Detection in Time Series Data using LSTM Autoencoders in Keras. In this context, anomaly implies sudden prices changes in the stock market.

## Learning Objectives

- Build an LSTM Autoencoder in Keras
- Detect anomalies with Autoencoders in time series data
- Create interactive charts and plots with Plotly and Seaborn

## Walkthrough

- Import Libraries
- Load and Inspect the S&P 500 Index Data
- Data Preprocessing
- Temporalize Data and Create Training-Test Splits
- Build an LSTM Autoencoder
- Train the Autoencoder
- Plot Metrics and Evaluate the Model
- Detect Anomalies in the S&P 500 Index Data

## Approach

- First train an autoencoder on data with no anomalies.
- Take a new data point and reconstruct it using the trained autoencoder.
- If the reconstruction error for the new data point is above some threshold, we can label it as anomaly.

## Logic

When we train an autoencoder on data with no anomalies, with more epochs and training time, the model keeps getting better in reconstructing outputs similar to the data it is trained upon. 
In our case this data is the one containing no anomalies, hence the model becomes efficient in reconstructing data with no anomalies.

When you provide new data(no anomaly) to the model for reconstruction, then based on the trained weights, the model will be able to recontruct it back very well since this is the kind of data it has been trained upon.
This would result in less reconstruction error.

However, if the new data being given contains anomaly then the model won't be able to reconstruct it back efficiently resulting in a higer reconstruction error.

We finally set a threshold on the reconstruction error beyond which the new data point would be labelled as "Anomaly".

## Outcome 

You will be able to design and build an LSTM autoencoder in Keras to detect anomalies in time series data.
