# AMI-Risk-Prediction
**Overview:**  
This project demonstrates predicting **Acute Myocardial Infarction (AMI)** risk from patient biomarkers using a **Random Forest machine learning model**, inspired by:

> de Capretz, P.O., Björkelund, A., Björk, J. et al. Machine learning for early prediction of acute myocardial infarction or death in acute chest pain patients using electrocardiogram and blood tests at presentation. BMC Med Inform Decis Mak 23, 25 (2023). https://doi.org/10.1186/s12911-023-02119-1

**Dataset:**  
I used the **PTB-XL ECG dataset**, publicly available on PhysioNet:  
[https://physionet.org/content/ptb-xl/1.0.1/](https://physionet.org/content/ptb-xl/1.0.1/)

**Workflow:**  
1. Load the dataset (download from PhysioNet).  
2. Preprocess features and biomarkers.  
3. Train a Random Forest Classifier.  
4. Predict AMI risk for sample patients.  
5. Visualize high-risk biomarkers and patient risk distribution.

**Tools:**  
Python, Pandas, NumPy, scikit-learn, Matplotlib, Seaborn

**Usage Example:**  
```python
import pandas as pd
import joblib

# Load trained model
model = joblib.load("ami_model.pkl")

# Load patient data (downloaded PTB-XL CSV or processed file)
sample_patients = pd.read_csv("sample_patients.csv")

# Predict AMI risk
predictions = model.predict(sample_patients)
