# Edunet AQI Prediction

## 🌍 Project Overview
Edunet AQI Prediction is a machine learning-powered web application that predicts **Air Quality Index (AQI)** based on environmental parameters like **PM2.5, PM10, NO2, CO, and O3 levels**. The project incorporates **Random Forest Regression**, **LSTM-based time series forecasting**, and **interactive visualizations** for air quality monitoring.

## 🚀 Features
- **Real-Time AQI Prediction:** Uses machine learning to estimate AQI from environmental data.
- **Hyperparameter Optimization:** Utilizes **Optuna** to fine-tune the **Random Forest model**.
- **Time Series Forecasting:** Implements an **LSTM (Long Short-Term Memory) model** to predict AQI trends.
- **Feature Importance Analysis:** Employs **SHAP** to interpret model predictions.
- **Interactive AQI Visualization:** Uses **Folium** to generate a real-time air quality map.
- **SMS Alerts:** Sends **Twilio-based notifications** when AQI exceeds safe levels.
- **REST API Endpoint:** Provides an API for real-time AQI prediction.

---

## 🛠️ Tech Stack
- **Python** (Flask, Pandas, NumPy, Scikit-Learn, TensorFlow, SHAP, Optuna)
- **Machine Learning** (Random Forest, LSTM)
- **Web Framework:** Flask
- **Visualization:** Matplotlib, Seaborn, Folium
- **SMS Alerts:** Twilio API

---

## 📂 Project Structure
```
Edunet_AQI_Prediction/
│── city_day.csv                # Air quality dataset
│── AQIProject.ipynb            # Jupyter notebook with model development
│── AQIProject_Enhanced.ipynb   # Optimized model with hyperparameter tuning
│── AQIProject_Updated.ipynb    # Final refined model
│── app.py                      # Flask API for real-time predictions
│── requirements.txt            # List of dependencies
│── README.md                   # Project documentation
```

---

## 📦 Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/AbdulSarban/Edunet_AQI_Prediction.git
cd Edunet_AQI_Prediction
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ Run Flask API
```bash
python app.py
```
This starts the API for real-time AQI predictions.

---

## 🎯 Usage
### 🌍 **Predict AQI Using API**
Make a **POST request** with air quality parameters:
```json
{
  "features": [45, 78, 25, 0.7, 30, 5, 3, 0.5, 85, 120]
}
```
**Response:**
```json
{
  "AQI Prediction": [160]
}
```

### 📲 **Enable SMS Alerts (Twilio)**
To receive alerts, set up **Twilio credentials** in `app.py`:
```python
TWILIO_ACCOUNT_SID = "your_twilio_sid"
TWILIO_AUTH_TOKEN = "your_twilio_auth_token"
TWILIO_PHONE_NUMBER = "your_twilio_phone"
USER_PHONE_NUMBER = "recipient_phone_number"
```
When AQI exceeds 200, a warning message is sent automatically.

---

## 📊 Data Visualization
- **SHAP Analysis:** Identifies important features affecting AQI.
- **Folium Map:** Displays air quality in different regions interactively.

---

## 📧 Contact
For queries, feel free to reach out:
- **GitHub:** [AbdulSarban](https://github.com/AbdulSarban)
- **Email:** your_email@example.com

---

## 📜 License
This project is **open-source** under the **MIT License**. Feel free to contribute! 🚀

