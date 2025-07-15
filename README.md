README.txt

Project Title: ARDS Mortality Prediction GUI Suite

Overview:
----------
This repository contains the source code for the *Mortality Prediction Suite*, a Python-based graphical user interface (GUI) developed to predict mortality probability in ICU patients with ARDS (Acute Respiratory Distress Syndrome) due to viral pneumonia (COVID-19 or H1N1). The suite is based on a series of interpretable logistic regression models developed and validated in our study:  
"Development of an Enhanced ARDS Severity Scoring Model Using Logistic Regression and Machine Learning-Based Feature Selection Techniques" (Scientific Reports, 2025).

This application supports rapid bedside use and enables clinicians to input early clinical data to obtain an estimated mortality risk using validated logistic models.

Features:
----------
- Two integrated modules:
    1. **Top Logistic Models Tab**: Contains 10 pre-selected logistic regression models (1 to 10 variables) based on feature importance (VR, glucose, COVID-19, etc.).
    2. **Tables VII–XV Models Tab**: Provides access to 55 logistic models derived from all valid combinations of the top 10 predictors (1 to 10 variables × 5 models each).
- Easy-to-use GUI with dropdown selectors for model type and number of variables.
- Field entry for patient name, ID, and clinical variables.
- Outputs mortality probability and saves results to a local CSV file.
- Built using `tkinter` for maximum portability and no external dependencies beyond standard libraries.

Requirements:
--------------
- Python ≥ 3.7
- No external libraries required beyond:
    * tkinter (standard)
    * numpy
    * csv
    * datetime
    * os

Files:
-------
- `main.py`: Main launcher. Integrates both logistic model tabs into a unified notebook GUI.
- `calc_top.py`: Backend and GUI code for the top 10 logistic regression models derived from feature ranking (Tables I–VI).
- `calc_general.py`: Backend and GUI code for the exhaustive model list described in Tables VII–XV.


Usage:
-------
1. Run the application:

2. Enter patient information.
3. Select a model tab:
- **Top Logistic Models** for predefined models (1–10 variables).
- **Tables VII–XV Models** to select from exhaustive logistic models (up to 55).
4. Choose the model number from the dropdown and enter clinical variable values.
5. Click **"Calculate Mortality Probability"**.
6. A message box will display the result, and it will be appended to `mortality_results.csv` or `mortality_results_v2.csv`.

Model Information:
-------------------
All models were derived from logistic regression analysis of 241 ARDS patients using data from the first 6 hours of ICU admission. Variables include:
- Ventilatory Ratio (VR)
- Glucose
- COVID-19 status
- Creatinine
- Hypertension (HAS)
- Age, Time since symptom onset
- Vasopressor use
- Tidal Volume (VT)
- Platelets, PEEP, BMI, etc.

The best model (10 variables) achieved an AUC of 0.924, significantly outperforming traditional SOFA scores.

Citation:
----------
If you use this tool, please cite:

Carmen Hernandez Cardenas, et al. *Development of an Enhanced ARDS Severity Scoring Model Using Logistic Regression and Machine Learning-Based Feature Selection Techniques*. Scientific Reports, 2025.

Contact:
---------
For questions or access to clinical datasets (subject to IRB approval), contact:
Gerardo Lugo-Torres  
glugot2022@cic.ipn.mx

License:
---------
This project is released for academic and clinical research use only under the MIT License.

Repository:
------------
https://github.com/Lugo1025/ARDS
