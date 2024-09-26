How to Use the Program

    Open the Application: Run the Python script to launch the GUI application.

    Select the Table:
        In the first dropdown menu, select the table (Table VII to Table XV) corresponding to the logistic model you want to use.

    Select the Model:
        After selecting the table, use the second dropdown menu to choose a specific model from that table.

    Enter Input Variables:
        Once a model is selected, the input fields corresponding to the required variables will appear.
        Enter the values for each input variable based on the measurement units described below.

    Calculate the Probability:
        After entering the variables, click the "Calculate Probability" button.
        The program will compute the mortality probability using the selected logistic model and display it.

Input Variable Descriptions and Units

    Ventilatory Ratio (VR): A dimensionless ratio, used to assess ventilation efficiency.
    Glucose: Blood glucose level, measured in mg/dL.
    Hypertension (HAS): Indicator of hypertension status (0 = No, 1 = Yes).
    COVID-19: COVID-19 status (0 = Negative, 1 = Positive).
    Tidal Volume (VT): Volume of air displaced during ventilation, measured in mL/kg.
    Age: Age of the patient in years.
    Time: Time in the Intensive Care Unit (ICU), measured in days.
    DHL (Lactate Dehydrogenase): Blood lactate dehydrogenase levels, measured in U/L.
    Platelets: Platelet count, measured in x10^3/µL.
    Creatinine: Blood creatinine levels, measured in mg/dL.
    Plateau Pressure (Pres Plat): Plateau pressure in the lungs during mechanical ventilation, measured in cm H2O.
    Driving Pressure (DP): Difference between plateau pressure and PEEP, measured in cm H2O.
    PEEP (Positive End-Expiratory Pressure): Measured in cm H2O.
    BMI (Body Mass Index): Measured in kg/m².
    Diabetes Mellitus (DM): Indicator of diabetes mellitus status (0 = No, 1 = Yes).
    Vasopressor Use: Indicator of vasopressor use (0 = No, 1 = Yes).

System Requirements

    Python 3.x: Ensure Python 3 is installed on your system.
    Required Libraries: The program uses the following libraries:
        tkinter: For the GUI.
        numpy: For numerical operations.
        ttk: For dropdown menus and UI components.

You can install the required libraries using:
pip install tkinter numpy

