# Blood-Pressure-Prediction-Based-on-LSTM-Model

This repository implements a pipeline using Long Short-Term Memory (LSTM) networks to predict Systolic Blood Pressure (SBP) and Diastolic Blood Pressure (DBP) from Photoplethysmogram (PPG) and Electrocardiogram (ECG) signals. By leveraging time-series data from these two physiological signals, this model aims to provide accurate blood pressure estimations without the need for traditional cuff-based measurements.

<p align="center">
  <img src="https://github.com/qdh-2002/Blood-Pressure-Prediction-Based-on-LSTM-Model/blob/main/img/model.png" alt="Description of the image" width="500">
</p>

## Introduction

📶 **Photoplethysmogram (PPG)**:
Photoplethysmography (PPG) is a non-invasive optical technique used to measure the blood volume changes in the microvascular bed of tissue. It works by emitting light (usually from an LED) into the skin and detecting the variations in light absorption due to blood flow. These changes are used to capture the pulse waveform, providing information about heart rate and the cardiovascular system. PPG sensors are widely used in wearable devices such as smartwatches and fitness trackers for monitoring heart rate, blood oxygen levels, and respiratory rate.

📶 **Electrocardiogram (ECG)**:
Electrocardiography (ECG) records the electrical activity of the heart over time, captured through electrodes placed on the skin. It provides a detailed view of the heart's rhythm and functionality, enabling detection of arrhythmias, heart rate, and other heart-related conditions. ECG is widely considered a gold standard for measuring heart health, and it’s used in both medical and research settings to monitor and diagnose cardiovascular conditions.

<p align="center">
  <img src="https://github.com/qdh-2002/Blood-Pressure-Prediction-Based-on-LSTM-Model/blob/main/img/schematic%20diagram.png" alt="Description of the image" width="500">
</p>

In this project, we fully utilized PPG and ECG to predict Systolic Blood Pressure (SBP) and Diastolic Blood Pressure (DBP), enhancing the accuracy and robustness of blood pressure estimation.

## Key Features
✅ **LSTM Network**:

The LSTM model is designed to handle time-series data by maintaining an internal memory of previous inputs. This allows the model to capture long-term dependencies between the PPG and ECG signals and their impact on blood pressure.
LSTM's ability to avoid vanishing gradient problems, which are common in standard recurrent neural networks (RNNs), makes it effective for modeling the sequential nature of physiological signals over extended time windows.

✅ **Dual Output Prediction**:

The model is constructed to predict both Systolic Blood Pressure (SBP) and Diastolic Blood Pressure (DBP) simultaneously using two parallel output layers. This allows for comprehensive monitoring and estimation of the user's blood pressure.

        
## Usage

## Install



## Contributing

See [the contributing file](CONTRIBUTING.md)!


