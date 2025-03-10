# Healthcare Appointment No-Show Prediction

## Overview
This project predicts whether a patient will miss their healthcare appointment (no-show) using historical data. The dataset includes patient demographics, appointment details, and medical history. The goal is to help clinics identify high-risk patients and reduce no-show rates.

## Repository Structure
- **`data/`**: Contains the dataset `appointment_data.csv`.
- **`outputs/`**: Stores visualizations and results generated during analysis.
- **`Healthcare_Appointment_NoShow_Prediction.ipynb`**: Jupyter Notebook with the full workflow—EDA, preprocessing, modeling, and evaluation.
- **`requirements.txt`**: Python dependencies.
- **`.gitignore`**: Excludes unnecessary files from version control.

## How to Run the Project
1. **Clone the repository**:
   ```bash
   git clone https://github.com/Edmon02/Healthcare_Appointment_NoShow_Prediction.git
   cd Healthcare_Appointment_NoShow_Prediction
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```
   - Open `Healthcare_Appointment_NoShow_Prediction.ipynb` and run all cells.

4. **Dataset**:
   - Ensure `appointment_data.csv` is in the `data/` folder before running the notebook.

## Approach
- **Exploratory Data Analysis (EDA)**: Analyzed patterns in the data, such as correlations between no-shows, waiting times, and SMS reminders.
- **Preprocessing**: Handled categorical variables, addressed missing data, and engineered features like `TimeOfDay` from appointment timestamps.
- **Modeling**: Trained Logistic Regression, Decision Tree, and Random Forest models, with hyperparameter tuning for the best performer (Random Forest).
- **Evaluation**: Used F1-score and ROC-AUC to measure performance, accounting for class imbalance.

## Key Findings
- Patients with prior no-shows are more likely to miss future appointments.
- Longer waiting times increase no-show probability.
- SMS reminders correlate with lower no-show rates.
- Top predictive features: `PreviousNoShows`, `WaitingTime`, `SMS_received`.

## Deliverables
- A Jupyter Notebook with detailed analysis, visualizations, and model evaluations.
- This `README.md` for project overview and instructions.