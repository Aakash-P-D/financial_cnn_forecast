# 📊 Financial Time Series Forecasting using CNN & STFT

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg"/>
  <img src="https://img.shields.io/badge/Python-3.10-blue"/>
  <img src="https://img.shields.io/badge/TensorFlow-CNN-orange"/>
</p>

## 🔹 Run on Google Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Aakash-P-D/financial_cnn_forecast/blob/main/financial_cnn_forecasting.ipynb)

____


## 📑 Table of Contents
- [Author](#-author)
- [Project Overview](#-project-overview)
- [Motivation](#-motivation)
- [System Pipeline](#-system-pipeline)
- [Features](#-features)
- [Technologies Used](#-technologies-used)
- [Workflow](#-workflow)
- [Model Architecture](#-model-architecture)
- [Project Structure](#-project-structure)
- [Spectrogram (Time-Frequency Representation)](#-spectrogram-time-frequency-representation)
- [Predicted Stock Prices](#-predicted-stock-prices)
- [How to Run](#-how-to-run)
- [Data Sources](#-data-sources)
- [References](#-references)
- [Expected Outcome](#-expected-outcome)
- [Results](#-results)
- [Limitations](#-limitations)
- [Future Improvements](#-future-improvements)
- [License](#-license)

---

## 🔹 Author
**Name:** Aakash P D

**University Register Number:** TCR24CS001

---

## 🔹 Project Overview
This project predicts **future stock prices** using **financial time series data**.  
It combines **time-frequency signal processing** (Short-Time Fourier Transform) and **Convolutional Neural Networks (CNN)** for prediction.

We use multiple financial features as input:
- Stock price vs time  
- Revenue vs quarter  
- Profit vs quarter  
- Market index (Sensex) vs time  
- USD–INR exchange rate vs time  

The multivariate signal is transformed into a **time-frequency representation (spectrogram)**, which is then fed into a CNN for forecasting.

---

## 🔹 Motivation

Financial markets are highly dynamic and complex.  
Traditional time series models often fail to capture hidden patterns.

This project explores how **signal processing + deep learning (CNN)** can improve stock price prediction using **time-frequency representations**.

---

## 🔹 System Pipeline

```text
📈 Time Series Data  →  🔊 STFT  →  🖼️ Spectrogram  →  🤖 CNN  →  💰 Predicted Stock Price
```
- Time Series Data: Collected from Yahoo Finance, NSE, BSE, RBI, or Kaggle
- STFT (Short-Time Fourier Transform): Converts signal into spectrogram
- CNN: Learns patterns in spectrograms for regression (predicting future price)

---

## 🔹 Features

↳ Multi-feature financial input

↳ Time-frequency analysis with STFT

↳ CNN-based regression for forecasting

↳ Visualization of spectrograms and predictions

↳ End-to-end pipeline implementation 

---

## 🔹 Workflow

↳ Collect financial time series data  
↳ Normalize and preprocess the data  
↳ Convert signal using STFT  
↳ Generate spectrogram  
↳ Feed spectrogram into CNN  
↳ Train model  
↳ Predict future stock price  
↳ Visualize results  

---

## 🔹 Model Architecture

The Convolutional Neural Network (CNN) consists of:

↳ Convolution layers for feature extraction  
↳ MaxPooling layers for dimensionality reduction  
↳ Fully connected (Dense) layers for prediction  
↳ Dropout layer to reduce overfitting  

The model takes **spectrogram images as input** and predicts the next stock price.

---

## 🔹 Project Structure
```text
financial-cnn-forecast/
├── financial_cnn_forecasting.ipynb     # Main notebook with code & outputs
├── financial_cnn_forecasting.py        # Optional clean Python code
├── outputs/                            # Folder with generated images
│   ├── prediction.png
│   ├── spectrogram.png
├── README.md                            # This file
├── requirements.txt                     # Python dependencies
```
---
## 🔹 Spectrogram (Time-Frequency Representation)

The spectrogram is a **2D time-frequency representation** of the financial signal.

- **Horizontal axis:** Time  
- **Vertical axis:** Frequency  
- **Intensity (color):** Signal energy  

**Interpretation:**

- **Low-frequency components:** Represent long-term trends  
- **High-frequency components:** Represent short-term fluctuations  

**Example:**  

![Spectrogram](outputs/spectrogram.png)  

---
## 🔹 Predicted Stock Prices

This plot shows the comparison between **predicted** and **actual** stock prices.

- **Comparison:** Predicted vs actual stock prices  
- **Evaluation:** Model performance is measured using **Mean Squared Error (MSE)**  
- **Interpretation:** Shows how effectively the CNN model learned patterns from the spectrogram  

**Example:**  

![Prediction](outputs/prediction.png)

---

## 🔹 How to Run

1. **Clone the repository:**

```bash
git clone https://github.com/yourusername/financial-cnn-forecast.git
cd financial-cnn-forecast
```
2. **Install dependencies:**
```bash
pip install -r requirements.txt
```
3. **Open the notebook in Google Colab or Jupyter:**
```bash 
jupyter notebook financial_cnn_forecasting.ipynb
```
4. **Run all cells** → Outputs (images, predictions) will be generated in the outputs/ folder.

---

## 🔹 Data Sources

The financial time series data can be collected from:

↳ **Yahoo Finance:** https://finance.yahoo.com

↳ **NSE India:** https://www.nseindia.com

↳ **BSE India:** https://www.bseindia.com

↳ **RBI Database:** https://www.rbi.org.in

↳ **Kaggle:** https://www.kaggle.com

---

## 🔹 References
**1.** Y. Zhang and C. Aggarwal, “Stock Market Prediction Using Deep Learning,” IEEE Access
**2.** A. Tsantekidis et al., “Deep Learning for Financial Time Series Forecasting”
**3.** S. Hochreiter and J. Schmidhuber, “Long Short-Term Memory,” Neural Computation, 1997
**4.** A. Borovykh et al., “Conditional Time Series Forecasting with CNNs”

---

## 🔹 Expected Outcome
- Financial time series can be analyzed as signals
- Spectrograms reveal hidden patterns in stock price data
- CNN models can learn useful representations from spectrograms to predict future stock prices
- Generated images:
  ↳ `outputs/spectrogram.png ` → shows time-frequency representation
  
  ↳ `outputs/prediction.png` → shows predicted vs actual stock prices

---
## 🔹 Results

↳ The model successfully learns patterns from spectrogram data  
↳ Predicted prices follow the trend of actual prices  
↳ Demonstrates feasibility of CNN-based forecasting  

**Note:** Accuracy can be improved with more data and tuning.

---

## 🔹 Limitations

↳ Limited dataset used for training  
↳ CNN may not capture long-term dependencies fully  
↳ Financial markets are highly unpredictable  
↳ Model performance depends on data quality  

---

## 🔹 Technologies Used

↳ Python  
↳ NumPy, Pandas  
↳ Matplotlib  
↳ SciPy (STFT)  
↳ Scikit-learn  
↳ TensorFlow / Keras  
↳ Yahoo Finance API  

---



## 🔹 Future Improvements

↳ Use LSTM + CNN hybrid model  
↳ Add more financial indicators (RSI, MACD)  
↳ Improve prediction accuracy with more data  
↳ Deploy as a web application  
↳ Real-time prediction using APIs  

---

## 🔹 License

This project is licensed under the MIT License.

This project was developed for academic and educational purposes, but is free to use, modify, and distribute under the MIT License.

---
⭐ If you found this project useful, consider giving it a star!

---

## 🔹 Contributing

Contributions are welcome! Feel free to fork this repository and submit a pull request.
  
fff
