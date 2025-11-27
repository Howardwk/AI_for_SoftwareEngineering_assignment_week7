# AI Ethics Assignment
## Designing Responsible and Fair AI Systems 🌍⚖️

This repository contains the complete submission for the AI Ethics assignment, covering theoretical understanding, case study analysis, practical bias auditing, and ethical reflection.

---


## 🚀 Setup Instructions

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)
- Jupyter Notebook or JupyterLab

### Installation

1. **Clone or download this repository**

2. **Create a virtual environment (recommended)**:
   ```bash
   python -m venv venv
   
   # On Windows:
   venv\Scripts\activate
   
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

5. **Open the notebook**:
   - Navigate to `ai_ethics_assignment.ipynb`
   - Run all cells to execute the bias audit analysis

---

## 📋 Assignment Components

### Part 1: Theoretical Understanding (30%)
- **Content**:
  - Short answer questions on algorithmic bias, transparency/explainability, and GDPR
  - Ethical principles matching exercise

### Part 2: Case Study Analysis (40%)
- **Content**:
  - Case 1: Amazon's Biased Hiring Tool
    - Bias source identification
    - Three proposed fixes
    - Fairness evaluation metrics
  - Case 2: Facial Recognition in Policing
    - Ethical risks analysis
    - Policy recommendations

### Part 3: Practical Audit (25%)
- **Content**:
  - COMPAS dataset bias analysis using AI Fairness 360
  - Fairness metrics computation
  - Visualizations of bias disparities
  - Bias mitigation using reweighing algorithm
  - 300-word summary report

### Part 4: Ethical Reflection (5%)
- **Content**:
  - Personal reflection on ensuring ethical AI principles in projects

---

## 🔧 Technical Details

### Libraries Used

- **AI Fairness 360 (aif360)**: IBM's comprehensive toolkit for bias detection and mitigation
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib & Seaborn**: Data visualization
- **Scikit-learn**: Machine learning models and metrics

### Dataset

The notebook attempts to load the COMPAS dataset from ProPublica's repository. If the download fails, it creates a synthetic dataset that replicates the bias patterns found in ProPublica's analysis.

**Note**: For the actual assignment, you should use the real COMPAS dataset from:
- ProPublica's GitHub: https://github.com/propublica/compas-analysis
- Direct CSV: https://raw.githubusercontent.com/propublica/compas-analysis/master/compas-scores-two-years.csv

### Fairness Metrics Computed

1. **Statistical Parity Difference**: Measures demographic parity
2. **Equal Opportunity Difference**: Measures difference in true positive rates
3. **Average Odds Difference**: Average of TPR and FPR differences
4. **Theil Index**: Measures inequality
5. **False Positive Rate (FPR)**: Rate of incorrectly predicting recidivism
6. **False Negative Rate (FNR)**: Rate of incorrectly predicting no recidivism
7. **True Positive Rate (TPR)**: Rate of correctly identifying recidivism

---

## 📊 Expected Outputs

After running the notebook, you should see:

1. **Console Output**:
   - Dataset statistics and race distribution
   - Fairness metrics analysis
   - Model performance metrics
   - Bias mitigation results

2. **Visualizations**:
   - `fairness_analysis.png`: Four-panel visualization showing:
     - Risk score distribution by race
     - Average risk scores by race
     - False positive rate comparison
     - Fairness metrics summary
   - `confusion_matrices.png`: Confusion matrices for African-American and non-African-American groups

3. **Summary Report**: Included in the notebook's final markdown cell

---

## 🎯 Key Findings (Summary)

The COMPAS bias audit reveals:

- **Risk Score Disparity**: African-American defendants receive higher average risk scores
- **False Positive Rate Disparity**: Higher FPR for African-American defendants means more false alarms
- **Statistical Parity Issues**: Significant differences in positive prediction rates between groups
- **Mitigation Potential**: Reweighing algorithms can partially reduce but not eliminate bias

---

## 📚 References

- **AI Fairness 360**: https://github.com/Trusted-AI/AIF360
- **ProPublica COMPAS Analysis**: https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing
- **EU Ethics Guidelines for Trustworthy AI**: https://digital-strategy.ec.europa.eu/en/library/ethics-guidelines-trustworthy-ai
- **GDPR**: https://gdpr.eu/

---

## ⚠️ Important Notes

1. **Dataset Access**: The notebook includes error handling to create a synthetic dataset if the real COMPAS data cannot be downloaded. For the actual assignment, ensure you can access the real dataset.

2. **Fairness Metrics**: Different fairness definitions may conflict (e.g., demographic parity vs. equalized odds). The notebook demonstrates multiple metrics to provide a comprehensive view.

3. **Bias Mitigation**: The reweighing algorithm is one of many possible interventions. Other techniques include adversarial debiasing, threshold optimization, and fairness constraints.

4. **Ethical Considerations**: This analysis is for educational purposes. Real-world bias audits should be conducted with proper ethical oversight and community engagement.

---


## 🆘 Troubleshooting

### Common Issues

1. **Import Errors**:
   - Ensure all packages are installed: `pip install -r requirements.txt`
   - Restart Jupyter kernel after installation

2. **Dataset Download Fails**:
   - Check internet connection
   - The notebook will create a synthetic dataset as fallback
   - For real data, manually download from ProPublica's repository

3. **Visualization Not Displaying**:
   - Ensure `%matplotlib inline` is executed
   - Check that matplotlib backend is properly configured

4. **AIF360 Errors**:
   - Ensure aif360 version >= 0.5.0
   - Some versions may have compatibility issues with newer pandas versions

---


