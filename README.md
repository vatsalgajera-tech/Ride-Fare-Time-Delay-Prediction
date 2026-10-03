# 🚗 Smart Ride Fare, Estimated Time and Delay Risk Prediction

Python Pandas NumPy Matplotlib Scikit-learn Jupyter Machine Learning

A machine learning project that predicts **ride fare**, **estimated travel time**, and **delay risk** using historical ride, demand, traffic, driver, and ride-related information.

---

## 📌 Project Overview

Ride-hailing services need accurate estimates of fare and travel time while also identifying rides that may have a higher risk of delay.

This project develops a machine learning system for:

- 💰 **Fare Prediction** — estimate the final ride fare
- ⏱️ **Travel Time Prediction** — estimate travel time
- ⚠️ **Delay Risk Prediction** — classify a ride as Low Risk or High Risk

The project includes data preprocessing, exploratory data analysis (EDA), feature preparation, model training, evaluation, and visualization.

---

## 🎯 Key Objectives

- 🧹 Clean and prepare ride-related data
- 📊 Perform exploratory data analysis
- 🔍 Analyze ride, demand, weather, city, and traffic patterns
- 💰 Predict final ride fare using Linear Regression
- ⏱️ Predict estimated travel time using Linear Regression
- ⚠️ Predict delay risk using Logistic Regression
- 📈 Evaluate models using appropriate performance metrics
- 📊 Visualize actual vs predicted values and classification results

---

## 🚀 Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical computation |
| Matplotlib | Data visualization |
| Scikit-learn | Machine learning |
| Jupyter Notebook | Development and analysis environment |

### Machine Learning Models

- **Linear Regression** — Fare Prediction
- **Linear Regression** — Estimated Travel Time Prediction
- **Logistic Regression** — Delay Risk Prediction

### Preprocessing

- Label Encoding
- Standard Scaling
- Train-Test Split

---

## 📂 Dataset Details

### Ride Demand and Fare Prediction Dataset

The project uses the **Ride Demand and Fare Prediction Dataset** containing ride-level records with information related to cities, demand, fare, traffic, drivers, weather, and ride characteristics.

### Important Features

- City
- Date
- Day of Week
- Latitude
- Longitude
- Ride Distance
- Ride Type
- Weather
- Event
- Payment Type
- Available Drivers
- Demand Level
- Demand Score
- Surge Multiplier
- Final Fare
- Hour of Day
- Is Weekend
- Driver Performance Score
- Driver XP
- Ride Priority
- Cancellation Rate
- Time of Day
- Driver Availability
- Traffic Delay
- Cancellation Probability
- Driver Trust Score
- Rider Trust Score
- Leaderboard Rank

---

## 🧠 Target Variables

### 💰 Fare Prediction

**Target:** `Final_Fare`

The model uses ride distance, demand, surge multiplier, traffic, driver performance, driver trust, time-related features, and weekend information to estimate the final fare.

### ⏱️ Estimated Travel Time

**Target:** `Estimated_Travel_Time`

The project derives estimated travel time using:

```text
Base Travel Time = (Ride Distance / Average Speed) × 60

Estimated Travel Time = Base Travel Time + Traffic Delay
```

The average speed used for the derived target is **30 km/h**.

> **Note:** Estimated Travel Time is a derived target rather than an original target column from the dataset. Because Ride Distance and Traffic Delay are also used as model inputs, the resulting travel-time model can achieve a near-perfect fit. This result should therefore be interpreted as reproducing the derived relationship rather than as an independent real-world travel-time benchmark.

### ⚠️ Delay Risk

**Target:** `Delay_Risk`

The target is created from `Traffic_Delay` using the median delay as the threshold:

```text
0 → Low Delay Risk
1 → High Delay Risk
```

`Traffic_Delay` is not directly used as an input feature for the delay-risk model in order to avoid target leakage.

---

## 📊 Exploratory Data Analysis

The project analyzes:

- Number of rides by city
- Ride type distribution
- Weather distribution
- Demand patterns
- Fare-related patterns
- Traffic delay patterns
- Delay risk distribution
- Feature relationships and correlations
- Actual vs predicted values

Visualizations are created using **Matplotlib**.

---

## 🤖 Model Evaluation

### Regression Metrics

For Fare and Travel Time Prediction:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

### Classification Metrics

For Delay Risk Prediction:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

---

## 📈 Current Model Results

### Regression

| Task | Model | MSE | RMSE | R² Score |
|---|---|---:|---:|---:|
| Fare Prediction | Linear Regression | 1032.97 | 32.14 | 0.8881 |
| Travel Time Prediction | Linear Regression | ~0 | ~0 | 1.0000 |

### Classification

| Task | Model | Accuracy | Precision | Recall | F1 Score |
|---|---|---:|---:|---:|---:|
| Delay Risk Prediction | Logistic Regression | 78.55% | 64.98% | 100.00% | 78.77% |

> Results can vary depending on preprocessing, train-test split, and notebook execution state.

---

## 📊 Analysis and Visualizations

The notebook contains visualizations including:

- Number of Rides by City
- Ride Type Distribution
- Weather Distribution
- Delay Risk Distribution
- Actual vs Predicted Fare
- Actual vs Predicted Travel Time
- Travel Time Prediction Residuals
- Delay Risk Confusion Matrix
- True/False Prediction Analysis

---

## 📁 Project Structure

```text
Ride-Fare-Time-Delay-Prediction/
│
├── Smart_Ride_Prediction_Termwork.ipynb
├── fairfare_ride_demand_dataset.csv
├── README.md
├── .gitignore
└── ...
```

### `.gitignore`

Jupyter checkpoint files are excluded from version control:

```text
.ipynb_checkpoints/
__pycache__/
*.pyc
```

---

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/vatsalgajera-tech/Ride-Fare-Time-Delay-Prediction.git
cd Ride-Fare-Time-Delay-Prediction
```

### 2. Install required libraries

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open the notebook

Open:

```text
Smart_Ride_Prediction_Termwork.ipynb
```

Run the cells from top to bottom.

---

## 🔄 Machine Learning Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Cleaning & Preprocessing
   ↓
Exploratory Data Analysis
   ↓
Feature Preparation
   ↓
Train-Test Split
   ↓
Feature Scaling / Encoding
   ↓
Model Training
   ↓
Prediction
   ↓
Model Evaluation
   ↓
Visualization
```

---

## 🔮 Future Enhancements

- 🚕 Real-time ride fare prediction
- ⏱️ More realistic travel-time target from real GPS/route data
- 🌦️ Real-time weather integration
- 🗺️ Route and geographic analysis
- 📊 Interactive dashboard using Streamlit
- ☁️ Deployment using AWS
- 🤖 Testing additional machine learning algorithms
- 📱 API-based prediction system
- 🔄 Real-time delay-risk monitoring

---

## Contributor

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/vatsalgajera-tech">
        <img src="https://github.com/vatsalgajera-tech.png" width="80" style="border-radius:50%"/><br/>
        <b>Vatsal Gajera</b>
      </a><br/>
      <sub>Data Science · Machine Learning</sub>
    </td>
  </tr>
</table>