# 🌫️ AQI (Air Quality Index) Prediction Dashboard
This application is designed to predict the Air Quality Index (AQI) based on the concentration of pollutants **PM2.5** and **NO2** using various intelligent system approaches, including Manual **Fuzzy Inference System (FIS)**, **GA-Tuned FIS**, and **Adaptive Neuro-Fuzzy Inference System (ANFIS)**.

This dashboard is developed as part of a Midterm Project (UTS) for the Soft Computing course.

---

## 🚀 How to Run the Application Locally

### 1. Prerequisites
Ensure you have installed `uv` (Python Package Manager). If not, install it using:
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### 2. Install Dependencies
Open a terminal in the `web_app` directory and run:
```bash
uv sync
```

### 3. Run the Dashboard
After synchronization is complete, run the following command:
```bash
uv run streamlit run app.py
```
The application will automatically open in your browser (usually at `http://localhost:8501`).

---

## 🛠️ Feature Usage Guide

### 🏠 1. Main Dashboard
- **Trend Visualization**: View historical air quality data for Delhi.
- **Quick Statistics**: Summary of average AQI, PM2.5, and NO2 from the dataset.

### 🔮 2. Single Prediction
- Manually enter **PM2.5** and **NO2** values.
- Click the **Predict** button to see a comparison of prediction results from all three models simultaneously.
- Equipped with a **Gauge Chart** and standard AQI color categories (Good, Moderate, Unhealthy, etc.).

### 📊 3. Batch Evaluation
- Test model performance on multiple rows of data at once.
- Displays **Actual vs Predicted** graphs to see how accurately the models follow the original data trends.
- Data sampling features (Start, End, or Random).

### 📈 4. Model Comparison
- This menu is crucial for scientific analysis.
- Displays key performance metrics:
    - **MAE (Mean Absolute Error)**: Average error difference (lower is better).
    - **RMSE (Root Mean Squared Error)**: Penalty for large errors.
    - **R² Score**: Percentage of data variance successfully explained (closer to 1.0 is better).
- Includes a performance **Heatmap** to identify which model performs best.

### 🔬 5. Membership Functions
- Visualization of the logic behind the models.
- You can see how the **Low**, **Medium**, and **High** sets are defined for PM2.5 and NO2.
- Compare differences between manually created parameters and parameters automatically learned by the **Genetic Algorithm (GA)** and **ANFIS**.

---

## 🧠 Models Used
1. **Manual FIS**: Uses parameters based on human intuition (Stage 1).
2. **GA-Tuned FIS**: Uses a genetic algorithm to find optimal curve widths and rule weights (Stage 2).
3. **ANFIS**: Uses a Neural Network to train Gaussian membership functions (Stage 3).

---
**Development Team:**
- Francisco Gilbert Sondakh (140810230004)
- Wilson Angelie Tan (140810230024)
- Theophilus Samuel Ghozalli (140810230054)
