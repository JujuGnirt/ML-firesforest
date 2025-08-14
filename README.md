# ML-firesforest

**Context**
With the ongoing environmental crisis, temperatures in many parts of the world continue to rise. As a result, forest fires are becoming more frequent and significantly harder to extinguish.

**🎯Prediction**

Develop a machine learning model to predict the likelihood of a forest fire based on weather conditions and Fire Weather Index (FWI components, helping improve early warning systems and resource allocation.

- 🛠 GitHub Repository: [project-ml-forest-fires] (https://github.com/JujuGnirt/ML-firesforest/tree/main)

- Presentation: [Canva] https://www.canva.com/design/DAGv2s8ACWE/-EqeNi_0ZcvOMJXpCqbrRg/edit?utm_content=DAGv2s8ACWE&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton 


# Main dataset
Small dataset which is not ideal for training machine learning model.

Features: Temperature, humidity, wind speed, rainfall, and FWI sub-indices (FFMC, DMC, DC, ISI, BUI, FWI).
Target: Burn area (tranform to a bool (0 = no fire ; 1 = fire))
Source: [UCI Machine Learning] https://archive.ics.uci.edu/dataset/162/forest+fires

# Solutions for the dataset issues

Dropping as less as possible.
Dealing with skewed data applying log(x+1) (also because a lot of 0 value present in the dataset column.)
Checking for outliers.
Normalized data.

# Models Tested
Logistic Regression (baseline)
Decision Tree Classifier
K-Nearest Neighbors (KNN)
Bagging with Logistic Regression

Evaluated using accuracy, precision, recall, F1-score, precision-recall curve and ROC-AUC.

# Ensemble model tested 
Using Decision Tree and Logistic regression, I tested :
- Stacking Classifier
- Voting Classifier

Evaluated using accuracy, precision, recall, F1-score, ROC-AUC, precision-recall curve and confusion matrix.

# Insights 
After hyperparameter tuning and cross-validation with Voting Classifer, we can observe that the only two features that matters was DC and DMC which are link to the moisture in layers. 
This is one of the expected outcomes, because of a small dataset and that fires are mostly initiated because of human related activities and recklessness. The model created didn't predict the occurence of the fire as well as expected, giving at most 65%.

# Futur Works and Improvement
Expand the dataset to include human activity and the type of vegatation on the land.
Expend the data with forest fires from 2003 to now.
Combining the models results with a regression model on the same topics by University of Minho which focus on the area burned.


# Repository Structure

```

ml-forestfires/
├── data/                        # Raw and cleaned CSV files
├── notebooks/                   # Python notebooks with analysis
├── slides/                      # Presentation
├── README.md                    # Introduction of the purpose of this project
├── .gitignore                   # 
├── 

```


##  Tools Used
 
- Python (Pandas, sklearn)  
- Jupyter Notebooks  
- Git & GitHub  
- Trello (for task planning)  
- Visual Studio Code IDE & plugins
  
---