# Optimization-of-Observation-unit-in-a-hospital

## Hospital Observation Unit Predictive Model
#### Executive Summary
This repository contains the code and documentation for a predictive model developed to identify patients who are more likely to be flipped from observation to inpatient status in a hospital's observation unit. Additionally, the model aims to establish which Diagnosis-Related Group (DRG) codes are associated with longer stays and have a high flip ratio. The model utilizes binary classification and logistic regression techniques with patient information as predictors to achieve these objectives.

#### Problem Description
The primary goal of this study is to create a predictive model that helps hospitals identify high-risk patients who are likely to be transferred from the observation unit to inpatient status. Furthermore, the model aims to determine the DRG codes that lead to longer stays and have a higher probability of flipping. By achieving these objectives, hospitals can make informed decisions in developing a more effective Observation Unit (OU) exclusion list, leading to cost reduction and improved patient outcomes through early intervention for high-risk individuals.

#### Data Cleaning and Preprocessing
The dataset used for model development underwent thorough data cleaning and preprocessing. Missing values in the dataset were handled appropriately by removing rows with missing values, as they had minimal impact on the overall data (only 16 missing values). Unnecessary variables, such as ObservationRecordKey and InitPatientClassAndFirstPostOUClass, were also removed as they did not contribute to the prediction process. Categorical variables, including Gender, Primary Insurance Category, and DRG01, were converted into factors for modeling purposes.

#### Exploratory Data Analysis
Exploratory data analysis was conducted to gain insights from the dataset and identify any patterns or trends. Various visualizations, such as histograms and box plots, were utilized to examine data distributions and identify potential outliers. Statistical tests, such as t-tests and ANOVA, were employed to compare means across different groups. For example, box plots were used to analyze the distribution of OU_LOS_hrs by Flipped and DRG01, while histograms were used to visualize the distribution of Age and OU_LOS_hrs.

#### Modeling
Three different models were developed to address the business problem:

##### Logistic Regression for Patient Flipping Prediction: 
This model predicts which patients are more likely to flip from observation to inpatient status. Significant variables such as OU_LOS_hrs, DRG1558, DRG01780, DRG01786, DRG01787, Pulse, and PrimaryInsuranceCategoryMedicare were identified. The model achieved an accuracy of approximately 77.8% on the test set.

##### Linear Regression for Longer Stays Prediction: 
This model aims to predict which DRG codes are associated with longer stays. The model identified several DRG codes, including DRG01780 and DRG01599, that are related to prolonged stays.

##### Cluster Analysis: 
Cluster analysis, specifically k-means clustering and hierarchical clustering, was used to group patients based on vital signs like blood pressure, pulse rate, and temperature.

#### Model Evaluation
Model performance was evaluated using various metrics such as accuracy, recall, ROC curves, and precision-recall curves. The optimal cutoff point for classifying patients as flipped or not flipped was determined to be 0.5.

#### Results
The model's results indicated the significant variables related to patient flipping and longer stays. Specific DRG codes were identified to have a higher likelihood of flipping, and certain DRG codes were associated with longer stays. Cluster analysis provided valuable insights into patient groups and their vital sign patterns.

#### Recommendations and Conclusion
Based on the findings, we recommend the following actions for the hospital:

Develop a strategy to reduce patient flipping from the observation unit by focusing on high-risk patients identified by the model.

Create an exclusion list based on DRG codes associated with longer stays and higher flipping probabilities.

Regularly review the flip ratio for different DRG codes to identify any trends or changes that may require intervention.

Utilize the cluster analysis to better comprehend patient groups and tailor treatment approaches accordingly.

#### In conclusion, the predictive model developed in this study can serve as a valuable tool for hospitals to make informed decisions, optimize resource utilization, and improve patient care and outcomes.
