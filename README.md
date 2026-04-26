
# GW-Signal-Feature-Extractor
### Machine Learning for Gravitational Wave Parameter Estimation

## 🌌 Project Overview
This repository contains a proof-of-concept Python pipeline designed to detect and classify **Gravitational Wave (GW)** signals from neutron star mergers. 

The project addresses a core challenge in modern astrophysics: extracting physical information from complex, noisy signals. While traditional methods are computationally expensive, this project demonstrates how **Machine Learning (ML)** can be used for fast, data-driven inference of binary merger signatures.

## 🚀 Key Features
* **Synthetic Signal Generation:** Uses NumPy to simulate "chirp" waveforms where frequency increases over time ($f_0 \to f_1$).
* **Noise Modeling:** Injects Gaussian noise to simulate the sensitivity limits of ground-based interferometers like LIGO.
* **ML Classification:** Implements a **Random Forest Classifier** to distinguish between signal-bearing data and stochastic noise.
* **Visualization:** Includes plotting scripts to visualize the "hidden" signal within the noisy time-series data.

##  Technical Stack
* **Language:** Python 3.x
* **Mathematical Libraries:** NumPy
* **Machine Learning:** Scikit-Learn
* **Data Visualization:** Matplotlib

##  Methodology
1.  **Waveform Simulation:** I modeled a 1-second merger event with a sampling rate of 2048 Hz. The "chirp" is modeled as a frequency-modulated sine wave.
2.  **Dataset Construction:** Created a balanced dataset of 1,000 samples (500 GW signals + Noise, 500 Pure Noise).
3.  **The Pipeline:**
    * **Pre-processing:** Flattening time-series arrays for vector-based classification.
    * **Training:** Using an ensemble of 100 decision trees (Random Forest) to learn frequency patterns.
    * **Evaluation:** Testing the model on unseen data to ensure generalization.

##  Results
The current model achieves an accuracy of ~**95%** in binary classification. This highlights the effectiveness of ensemble learning in recognizing the structural patterns of gravitational waves even when the Signal-to-Noise Ratio (SNR) is low.

##  Conclusion & Future Directions
This project serves as a foundational step toward more complex parameter estimation. My next goals for this pipeline include:
* Transitioning from **Random Forest** to **Convolutional Neural Networks (CNNs)** for better spatial feature extraction.
* Attempting to predict the **Chirp Mass** and **Equation of State (EoS)** directly from the waveform.

---
**Author:** Fatima Zahra 
**Objective:** Developed as a technical demonstration for research applications in Computational Astrophysics and Machine Learning.
