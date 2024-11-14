# COVID-19 Data Modeling

**Description:**
This project models and analyzes COVID-19 trends using the `covid19-sir` library. It focuses on tracking infection phases, estimating parameters, and forecasting short- and long-term trends for selected countries, such as Poland and Singapore. The analysis includes trend detection, phase analysis, and predictive simulations with visualizations.

---

## Objectives

1. **Trend Detection:**
   - Analyze and identify trends in infection rates for selected countries.

2. **Parameter Estimation:**
   - Use the SIRF model to estimate parameters for each phase of infection.

3. **Forecasting:**
   - Predict COVID-19 trends for 7, 30, and longer durations based on historical data.

4. **Visualization:**
   - Provide graphs and tables to illustrate infection trends and predictions.

---

## Features

1. **Data Analysis:**
   - Load and preprocess COVID-19 datasets from Johns Hopkins University.
   - Analyze infection rates for specific countries.

2. **Model Implementation:**
   - Apply the SIRF model to estimate infection and recovery rates.
   - Simulate future scenarios based on current trends.

3. **Graphical Representation:**
   - Visualize trends, phase analysis, and forecasts with detailed graphs.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/COVID-19-Data-Modeling.git
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Python scripts or Jupyter Notebook:
   ```bash
   python main.py
   ```

---

## Usage

1. Load the dataset and create a scenario:
   ```python
   pln_scenario = cs.Scenario(country="Poland")
   pln_scenario.register(jhu_data)
   ```
2. Detect trends and phases:
   ```python
   pln_scenario.trend()
   ```
3. Estimate parameters for each phase:
   ```python
   pln_scenario.estimate(cs.SIRF, timeout=120)
   ```
4. Forecast trends for specific durations:
   ```python
   pln_scenario.add(days=30)
   pln_scenario.simulate()
   ```

---

## Results

- **Trend Analysis:** Detected key phases in infection rates for Poland and Singapore.
- **Parameter Estimation:** Successfully estimated parameters like infection and recovery rates.
- **Forecasting:** Predicted infection trends for short- and long-term periods.

---

## Author

- **Name:** Olha Nemkovych
- **Group:** FI-94

