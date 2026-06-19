
# Global Pollution Analysis and Energy Recovery using Apriori Algorithm

## Objective
The objective of this project is to analyze global pollution data and discover hidden associations between pollution levels, energy consumption, and energy recovery using the Apriori Algorithm.

## Dataset
Dataset used:
C:\Users\NXTWAVE\Downloads\Global Pollution Analysis and Energy Recovery using Apriori Algorithm\Global_Pollution_Analysis.csv

Total records: 200
Total features: 22

## Phase 1: Data Preprocessing
The dataset was loaded, cleaned, and processed. Missing values were handled using mean imputation for numerical columns and mode imputation for categorical columns.

## Feature Engineering
The following features were created:
- Energy_Recovered_Per_Capita
- Average_Pollution_Index
- Energy_Efficiency_Score
- Air_Severity
- Water_Severity
- Soil_Severity
- Overall_Severity
- Energy_Recovery_Level
- Energy_Consumption_Level

## Phase 2: Apriori Algorithm
The Apriori Algorithm was applied to identify association rules among pollution severity, energy recovery, and energy consumption.

Minimum Support: 0.05  
Minimum Confidence: 0.4

## Top Association Rules
                                                                                antecedents                                                               consequents  antecedent support  consequent support  support  confidence     lift  representativity  leverage  conviction  zhangs_metric  jaccard  certainty  kulczynski
                                             Water_Severity_Water_Low, Air_Severity_Air_Low                                              Overall_Severity_Overall_Low               0.060               0.210    0.060    1.000000 4.761905               1.0  0.047400         inf       0.840426 0.285714   1.000000    0.642857
                                               Soil_Severity_Soil_Low, Air_Severity_Air_Low                                              Overall_Severity_Overall_Low               0.105               0.210    0.075    0.714286 3.401361               1.0  0.052950    2.765000       0.788827 0.312500   0.638336    0.535714
                  Air_Severity_Air_Medium, Water_Severity_Water_Low, Soil_Severity_Soil_Low                                              Overall_Severity_Overall_Low               0.135               0.210    0.090    0.666667 3.174603               1.0  0.061650    2.370000       0.791908 0.352941   0.578059    0.547619
                                                               Overall_Severity_Overall_Low Air_Severity_Air_Medium, Water_Severity_Water_Low, Soil_Severity_Soil_Low               0.210               0.135    0.090    0.428571 3.174603               1.0  0.061650    1.513750       0.867089 0.352941   0.339389    0.547619
                                                                       Air_Severity_Air_Low                                              Overall_Severity_Overall_Low               0.145               0.210    0.095    0.655172 3.119869               1.0  0.064550    2.291000       0.794706 0.365385   0.563509    0.553777
                                                               Overall_Severity_Overall_Low                                                      Air_Severity_Air_Low               0.210               0.145    0.095    0.452381 3.119869               1.0  0.064550    1.561304       0.860093 0.365385   0.359510    0.553777
                                      Air_Severity_Air_Medium, Overall_Severity_Overall_Low                          Water_Severity_Water_Low, Soil_Severity_Soil_Low               0.110               0.275    0.090    0.818182 2.975207               1.0  0.059750    3.987500       0.745943 0.305085   0.749216    0.572727
Energy_Consumption_Level_High_Consumption, Soil_Severity_Soil_Low, Water_Severity_Water_Low                                              Overall_Severity_Overall_Low               0.100               0.210    0.060    0.600000 2.857143               1.0  0.039000    1.975000       0.722222 0.240000   0.493671    0.442857
                                                                       Air_Severity_Air_Low                      Soil_Severity_Soil_Low, Overall_Severity_Overall_Low               0.145               0.190    0.075    0.517241 2.722323               1.0  0.047450    1.677857       0.739961 0.288462   0.404002    0.455989
                                                                       Air_Severity_Air_Low                    Water_Severity_Water_Low, Overall_Severity_Overall_Low               0.145               0.155    0.060    0.413793 2.669633               1.0  0.037525    1.441471       0.731481 0.250000   0.306264    0.400445

## Phase 3: Validation
Train-test validation and 5-fold cross-validation were used to validate Apriori rules.

Average Apriori Rule Accuracy:
0.44206273776133465

## CNN Model
A CNN model was trained by converting tabular pollution features into image-like matrices.

CNN Accuracy:
0.8999999761581421

## Random Forest Baseline
Random Forest Accuracy:
1.0

## Key Insights
- Apriori rules help identify relationships between pollution severity and energy recovery.
- High pollution categories can be associated with different recovery and consumption levels.
- CNN provides classification capability for pollution severity prediction.
- Rule mining provides interpretability, while CNN provides predictive performance.

## Recommendations
- Countries with high pollution and low recovery should improve renewable energy adoption.
- Energy recovery strategies should be prioritized in high air and water pollution regions.
- Association rules can help policymakers identify recurring pollution-energy patterns.
- Machine learning models can support future pollution severity prediction.

## Generated Outputs
- Cleaned dataset
- Normalized dataset
- Encoded dataset
- Frequent itemsets CSV
- Association rules CSV
- Apriori validation CSV
- Cross-validation CSV
- CNN model H5 file
- CNN prediction CSV
- Confusion matrix
- ROC curve
- Correlation heatmap
- Frequent itemset graph
- Association rule graphs
- Model comparison graph
