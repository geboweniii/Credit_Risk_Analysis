## Overview
Python was used to build and evaluate several machine learning models to predict credit risk.\
This involved oversample the data using RandomOverSampler and SMOTE, undersample the data using ClusterCentroids, an oversampling and undersampling using the SMOTEENN, and comparison of two machine learning models BalancedRandomForestClassifier and EasyEnsembleClassifier. Model results will determine whether they should be used to predict credit risk.

## Resources
- Data Source: LoanStats_2019Q1.csv
- Software: Python 3.9, Jupyter Notebook

## Results

### RandomOverSampler model
<ul>
<li>Balanced accuracy score: 65%.</li>
<li>High_risk precision: about 1% only</li>
<li>Sensitivity: 62%</li>
<li>F1: 2%</li>
</ul>
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.
<br><br>

### SMOTE model
<ul>
<li>Similar results to RandomOverSampler</li>
<li>Balanced accuracy score: 64%</li>
<li>High_risk precision: about 1%</li>
<li>Sensitivity: 63%</li>
<li>F1: 2%</li>
</ul>
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 66%.
<br><br>

### ClusterCentroids model
<ul>
<li>Balanced accuracy score: 52%</li>
<li>High_risk precision: about 1%</li>
<li>Sensitivity: 63%</li>
<li>F1: 1%</li>
</ul>
Due to the high number of false positives, the low_risk sensitivity is only 40%.
<br><br>

### SMOTEENN model
<ul>
<li>Balanced accuracy score: 62%</li>
<li>High_risk precision: about 1%</li>
<li>Sensitivity: 68%</li>
<li>F1: 2%</li>
</ul>
Due to the high number of false positives, the low_risk sensitivity is 57%.
<br><br>

### BalancedRandomForestClassifier model
<ul>
<li>Balanced accuracy score: 79%</li>
<li>High_risk precision: about 4%</li>
<li>Sensitivity: 67%</li>
<li>F1: 7%</li>
</ul>
Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.
<br><br>

### EasyEnsembleClassifier model
<ul>
<li>Balanced accuracy score: 93%</li>
<li>High_risk precision: 7%</li>
<li>Sensitivity: 91%</li>
<li>F1: 14%</li>
</ul>
Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.
<br><br>

## Summary
All models used to perform credit risk analysis show weak precision in determining if a credit risk is high. Ensemble models bear more improvement on the sensitivity of the high risk credits. EasyEnsembleClassifier model shows a recall of 92% detecting almost all high risk credit. However, with low precision low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy impacting its revenue by missing key business opportunities. Therefore no model should be employed by the bank to predict credit risk.
