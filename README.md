
# ⚡ Electricity Consumption Forecasting

This project aims to forecast monthly electricity consumption using time series analysis. It compares the performance of two powerful models—**ARIMA** and **LSTM**—to evaluate their effectiveness in predicting future consumption trends.

---

## 📌 Project Overview

The dataset spans **397 months** of electricity consumption records. Using this historical data, the project applies **ARIMA** (a traditional statistical model) and **LSTM** (a deep learning model) to forecast future electricity usage and evaluate their relative performances.

---

## 📂 Table of Contents

- [Project Overview](#-project-overview)  
- [Dataset](#-dataset)  
- [Models](#-models)  
- [Installation](#-installation)  
- [Usage](#-usage)  
- [Results](#-results)  
- [Contributing](#-contributing)  
- [License](#-license)

---

## 🗃️ Dataset

The dataset includes:

- **Date**: Timestamps (mostly the 1st of each month and a few specific additional days).
- **Consumption**: Monthly electricity usage in kilowatt-hours (kWh).

---

## 🤖 Models

### 1. **ARIMA** (Auto-Regressive Integrated Moving Average)

- **Description**: A statistical model effective for **stationary time series** with discernible trends and seasonality.
- **Key Features**: Uses differencing, autoregressive terms, and moving averages to model patterns.

### 2. **LSTM** (Long Short-Term Memory)

- **Description**: A deep learning model suitable for **non-linear, sequential data**.
- **Key Features**: Leverages LSTM layers to learn long-term dependencies and capture complex patterns in the time series.

---

## ⚙️ Installation

To set up the project:

\`\`\`bash
git clone <repository-url>
cd electricity-consumption-forecasting
pip install -r requirements.txt
\`\`\`

> ✅ Make sure you're using **Python 3.8+**

### Key Dependencies

- \`numpy\`  
- \`pandas\`  
- \`matplotlib\`  
- \`tensorflow\`  
- \`statsmodels\`  

---

## 🚀 Usage

### 1. **Data Preprocessing**

- Clean and prepare the dataset.  
- Run \`data_preprocessing.ipynb\` for exploration and preprocessing.

### 2. **Model Training**

- **ARIMA**:  
  - Run \`train_arima.py\` or \`arima_training.ipynb\`
  
- **LSTM**:  
  - Run \`train_lstm.py\` or \`lstm_training.ipynb\`

### 3. **Evaluation**

- Use metrics like **MAE**, **RMSE**, and **MAPE**.  
- Compare models to determine forecasting performance.

### 4. **Forecasting**

- Generate and save predictions in the \`results/\` directory.  
- Visualize and analyze trends.

---

## 📊 Results

This project provides a side-by-side comparison of ARIMA and LSTM in terms of:

- **Forecast Accuracy**
- **Generalization Capabilities**
- **Handling Trends and Seasonality**

Visualizations and evaluation metrics are available in the \`results/\` folder.

---

## 🤝 Contributing

Contributions are welcome!  
Feel free to **open issues** or **submit pull requests** to enhance the project.

---

## 📄 License

This project is licensed under the **MIT License**.
See the [LICENSE](./LICENSE) file for details.  
