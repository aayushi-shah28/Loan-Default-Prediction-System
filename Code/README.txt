# Loan Default Prediction System using Machine Learning

## Project Contents
- Report.pdf                      : Final project report
- dataset/train.csv               : Dataset used (Kaggle Loan Prediction)
- code/notebook.ipynb             : Google Colab notebook (implementation)
- code/notebook_export.py         : Python script exported from notebook
- code/requirements.txt           : Required Python packages
- code/model/rf_model.joblib      : Trained RandomForest model (tuned)
- code/model/scaler.joblib        : Fitted StandardScaler
- code/assets/*.png               : Figures/screenshots used in report

## How to run (locally)
1. Clone/extract the ZIP file.
2. Create a virtual environment (optional but recommended):
   - Windows (Powershell):
     `python -m venv venv`
     `.\venv\Scripts\activate`
   - Mac/Linux:
     `python3 -m venv venv`
     `source venv/bin/activate`

3. Install dependencies:
   `pip install -r code/requirements.txt`

4. To re-run the notebook:
   - Open `code/notebook.ipynb` in Jupyter/Colab and run the cells.
   - Or run `python code/notebook_export.py` (note: script may need small edits to run outside Colab).

5. To use the saved model for prediction:
```python
import joblib
model = joblib.load('code/model/rf_model.joblib')
scaler = joblib.load('code/model/scaler.joblib')
