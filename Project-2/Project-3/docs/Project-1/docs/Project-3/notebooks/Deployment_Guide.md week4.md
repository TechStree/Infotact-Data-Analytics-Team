# Deployment Guide: Supply Chain Analytics Pipeline

## Project Overview
This guide provides the necessary instructions to deploy and run the "Supply Chain Analytics – Demand Forecasting & Anomaly Detection" project. The repository contains a series of Jupyter Notebooks that guide the user from raw data exploration to advanced predictive modeling.

## System Requirements
* **Operating System:** Windows, macOS, or Linux
* **Memory (RAM):** 8 GB minimum (16 GB recommended for large dataset processing)
* **Storage:** At least 500 MB of free disk space

## Python Version
* **Python 3.8 or higher** is required to ensure compatibility with the latest data science libraries.

## Required Libraries
To execute the notebooks, the following Python packages must be installed:
* `pandas` (Data manipulation)
* `numpy` (Numerical computations)
* `matplotlib` & `seaborn` (Data visualization)
* `scikit-learn` (Machine learning & Anomaly detection)
* `statsmodels` (Time series forecasting / ARIMA)
* `jupyter` (Notebook environment)

## Installation Steps
1. **Clone the Repository / Extract Files:** Ensure all `.ipynb` files and the dataset are in the same primary project folder.
2. **Open Terminal / Command Prompt:** Navigate to the project directory.
3. **Create a Virtual Environment (Optional but recommended):**
   ```bash
   python -m venv supply_chain_env
   source supply_chain_env/bin/activate  # On macOS/Linux
   supply_chain_env\Scripts\activate     # On Windows