# Blood-Pressure-Prediction-Based-on-LSTM-Model
[![license](https://img.shields.io/github/license/:user/:repo.svg)](LICENSE)
[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

This repository implements a pipeline using Long Short-Term Memory (LSTM) networks to predict Systolic Blood Pressure (SBP) and Diastolic Blood Pressure (DBP) from Photoplethysmogram (PPG) and Electrocardiogram (ECG) signals. By leveraging time-series data from these two physiological signals, this model aims to provide accurate blood pressure estimations without the need for traditional cuff-based measurements.

<p align="center">
  <img src="https://github.com/qdh-2002/Blood-Pressure-Prediction-Based-on-LSTM-Model/blob/main/img/model.png" alt="Description of the image" width="450">
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

        
## Details
### Dataset

The dataset used in this project is sourced from [this Kaggle repository](https://www.kaggle.com/code/stephenmugisha/bloodpressure-analysis). 

PPG signals, ECG signals and BP signals all have a sampling rate of Fs = 125Hz, where PPG signals were obtained using fingertip, ECG signals coming from electrocardiogram from channel II, and BP signals are invasive arterial blood pressure.

### Filtering
Biological artifacts in physiological signals, such as ECG and PPG, can arise from muscle movements, electrical interference, or poor electrode contact. Additionally, external electromagnetic interference from power lines or electronic devices contributes to environmental noise in recordings. Motion artifacts are also prevalent, especially in wearable devices, where the subject's movement can distort the signals. Furthermore, equipment errors, including calibration issues, sensor malfunctions, or software bugs, can lead to inaccuracies in the recorded data, underscoring the need for effective artifact removal techniques.

<p align="center">
  <img src="https://github.com/qdh-2002/Blood-Pressure-Prediction-Based-on-LSTM-Model/blob/main/img/filter.png" alt="Description of the image" width="500">
</p>

A random Gaussian noise was introduced into the signal to simulate real-world noise. In order to tackle with this noise, a fourth-order elliptic bandpass filter was used, with a passband set from 0.5 to 5 Hz. The figure shows the comparison between the signal with noise and the filtered signal.

### Results
For DBP, the Root Mean Squared Error (RMSE) is 5.92. For SBP, RMSE is 9.38. Note that this model was trained on 256488 samples (125 timepoints each sample).

<p align="center">
  <img src="https://github.com/qdh-2002/Blood-Pressure-Prediction-Based-on-LSTM-Model/blob/main/img/results_dbp.png" alt="Description of the image" width="500">
</p>

<p align="center">
  <img src="https://github.com/qdh-2002/Blood-Pressure-Prediction-Based-on-LSTM-Model/blob/main/img/results_sbp.png" alt="Description of the image" width="500">
</p>



## Contributing

See [the contributing file](CONTRIBUTING.md)!


