# Bike-Rental-Demand-Forecasting.

# 🚲 Bike Rental Demand Forecasting using RNN, LSTM & GRU

### 📊 Time Series Forecasting | Deep Learning | Sequential Neural Networks

Predicting future bike rental demand using Deep Learning models — Simple RNN, LSTM, and GRU — based on historical hourly rental data.

---

## 📌 Project Overview

Bike rental services need to understand customer demand to manage bike availability, optimize operations, and improve resource allocation.

This project focuses on **forecasting hourly bike rental demand for the next 24 hours** using historical rental data and three different Recurrent Neural Network architectures:

- 🔹 Simple RNN (Recurrent Neural Network)
- 🔹 LSTM (Long Short-Term Memory)
- 🔹 GRU (Gated Recurrent Unit)

The models learn temporal patterns from the previous seven days of hourly rental data and predict bike rental demand for the following 24 hours.

The project also compares the performance of all three deep learning models against a previous-day baseline forecasting approach.

## 🎯 Project Objectives

- 📈 Analyze historical hourly bike rental demand.
- 🧹 Perform time-series data preprocessing and handle missing hourly observations.
- 🔄 Transform historical data into sequential input-output windows.
- 🧠 Build and train Simple RNN, LSTM, and GRU models.
- 📊 Compare models using MAE and RMSE evaluation metrics.
- ⚡ Analyze model training time and validation performance.
- 🔮 Forecast bike rental demand for the next 24 hours.
- 🏆 Select the best-performing neural network using validation MAE.

## 🛠️ Technologies & Libraries Used

| Technology | Purpose |
|---|---|
| Python | Programming Language |
| NumPy | Numerical Computation |
| Pandas | Data Manipulation |
| Matplotlib | Data Visualization |
| TensorFlow | Deep Learning Framework |
| Keras | Neural Network Development |
| Scikit-learn | Data Scaling and Evaluation |
| Jupyter Notebook | Development Environment |

## 🧠 Deep Learning Models Implemented

### 1. Simple RNN
Implemented a Recurrent Neural Network to learn sequential patterns from historical hourly bike rental data.

### 2. LSTM (Long Short-Term Memory)
Implemented an LSTM network to capture temporal dependencies and learn patterns from historical rental sequences.

### 3. GRU (Gated Recurrent Unit)
Implemented a GRU network to learn sequential relationships using its gating mechanism.

All three architectures use 32 recurrent units followed by a Dense output layer that predicts the next 24 hourly rental values.

## ⚙️ Project Workflow

The project follows a complete time-series forecasting pipeline:

**1. Data Loading**
- Imported the hourly bike-sharing dataset.
- Inspected dataset structure, columns, and missing values.

**2. Data Preprocessing**
- Created timestamps using date and hour information.
- Sorted observations chronologically.
- Constructed a continuous hourly timeline.
- Handled missing historical input observations using forward filling.
- Preserved missing target observations and excluded incomplete forecasting windows.

**3. Exploratory Data Analysis (EDA)**
- Visualized hourly bike rental demand over time.
- Analyzed the first seven days of rental activity.
- Examined average bike rentals by hour of the day.

**4. Time-Series Sequence Preparation**
- Used the previous 7 days (168 hours) as model input.
- Predicted the next 24 hours as output.
- Created separate training, validation, and testing datasets.

**5. Feature Scaling**
- Applied MinMaxScaler to normalize rental counts.
- Fitted the scaler using training-period observations.

**6. Model Development & Training**
- Built Simple RNN, LSTM, and GRU architectures.
- Used Adam optimizer and Mean Absolute Error (MAE) loss.
- Applied EarlyStopping to monitor validation loss.
- Used batch size of 32 and up to 5 training epochs.

**7. Model Evaluation**
- Evaluated models using:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
- Compared neural networks against a previous-day baseline.
- Analyzed training time and validation performance.

**8. Future Demand Forecasting**
- Selected the best neural network based on validation MAE.
- Generated predictions for the next 24 hours.
- Visualized historical rental demand against future predicted demand.

## 📊 Model Evaluation Metrics

The project uses the following evaluation metrics:

| Metric | Description |
|---|---|
| MAE | Measures the average absolute prediction error. |
| RMSE | Measures prediction error while penalizing larger errors more heavily. |

The evaluation compares four forecasting approaches:

- Previous-Day Baseline
- Simple RNN
- LSTM
- GRU

**Note:** Actual model performance and rankings are determined by the notebook's evaluation results.

## 🔍 Key Project Highlights

- ⏳ Time-series forecasting using historical hourly data.
- 🧠 Implementation of three different recurrent neural network architectures.
- 📅 Seven-day historical input window for 24-hour forecasting.
- 🔄 Chronological training, validation, and testing split.
- 📉 Model learning curve visualization.
- ⚖️ Baseline versus deep learning model comparison.
- 🏆 Best-model selection using validation performance.
- 🔮 Future 24-hour bike rental demand prediction.

## 📂 Project Structure

```text
Bike-Rental-Demand-Forecasting/
│
├── Bike Rental Demand Forecasting with RNN, LSTM, and GRU.ipynb
│
├── bike+sharing+dataset/
│   └── hour.csv
│
└── README.md
```

## 🚀 How to Run This Project

**Step 1: Clone the repository**

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

**Step 2: Navigate to the project folder**

```bash
cd Bike-Rental-Demand-Forecasting
```

**Step 3: Install the required libraries**

```bash
pip install numpy pandas matplotlib tensorflow scikit-learn jupyter
```

**Step 4: Download the dataset**

Download the Bike Sharing Dataset from the UCI Machine Learning Repository:

https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset

Extract the dataset and ensure the `hour.csv` file is available at:

```text
bike+sharing+dataset/hour.csv
```

**Step 5: Run Jupyter Notebook**

```bash
jupyter notebook
```

Open the notebook and execute all cells sequentially.

## 📈 Expected Output

After running the notebook, you will get:

- Historical hourly bike rental demand visualization.
- Average rentals by hour of the day.
- Training and validation loss curves.
- Comparison of Simple RNN, LSTM, and GRU.
- MAE and RMSE evaluation results.
- Actual vs predicted rental demand visualization.
- Next 24-hour bike rental demand forecast.

## 💡 Real-World Applications

This project demonstrates how deep learning-based time-series forecasting can support:

- 🚲 Bike-sharing demand management.
- 📍 Bike availability planning.
- 📊 Transportation demand analysis.
- 🏙️ Smart city mobility systems.
- 📦 Resource and inventory optimization.

## 👨‍💻 Author

**Dheeraj Chouhan**

🎓 B.Tech – Information Technology

💻 Aspiring AI/ML Engineer | Deep Learning Enthusiast

### 🔗 Connect With Me

- GitHub: https://github.com/dheeraj24-coder
- LinkedIn: https://www.linkedin.com/in/dheeraj-chouhan-7a6996371/
- Portfolio: https://dheeraj-chouhan-aiml-engineer-portf.vercel.app/

---

⭐ If you find this project interesting, consider giving this repository a star!

**Built with Python, TensorFlow & Deep Learning ❤️**
