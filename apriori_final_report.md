# Final Report

## Project Title

Global Pollution Analysis and Energy Recovery using Apriori Algorithm

## Author

Sagnik Patra

## Objective

The goal of this project is to analyze global pollution data to understand the relationship between pollution levels such as air, water, and soil pollution and energy recovery across different countries.

The Apriori Algorithm is used to uncover hidden associations between pollution factors, energy consumption, and energy recovery patterns. A CNN model is also implemented to classify pollution severity using engineered image-like features.

## Dataset

Dataset used: Global_Pollution_Analysis.csv

The raw dataset is not included in the final submission package as per assignment recommendations.

## Phase 1: Data Preprocessing and Feature Engineering

The dataset was loaded and cleaned. Missing numerical values were handled using mean imputation, and categorical missing values were handled using mode imputation.

Preprocessing steps:

- Missing value handling
- Duplicate removal
- Categorical encoding
- Pollution index normalization
- Feature engineering
- Pollution severity categorization

Created features:

- Energy_Recovered_Per_Capita
- Energy_Consumption_Efficiency
- Average_Pollution_Index
- Air_Severity
- Water_Severity
- Soil_Severity
- Overall_Severity
- Energy_Recovery_Level
- Energy_Consumption_Level

## Phase 2: Apriori Algorithm

The Apriori Algorithm was applied to discover frequent itemsets and association rules.

Minimum Support: 0.05

Minimum Confidence: 0.40

Association rule metrics:

- Support
- Confidence
- Lift
- Leverage
- Conviction

## Top Association Rules

```text
                                                                                            antecedents                                                               consequents  antecedent support  consequent support  support  confidence     lift  representativity  leverage  conviction  zhangs_metric  jaccard  certainty  kulczynski
                                                         Water_Severity_Water_Low, Air_Severity_Air_Low                                              Overall_Severity_Overall_Low               0.060               0.210    0.060    1.000000 4.761905               1.0  0.047400         inf       0.840426 0.285714   1.000000    0.642857
                                                           Soil_Severity_Soil_Low, Air_Severity_Air_Low                                              Overall_Severity_Overall_Low               0.105               0.210    0.075    0.714286 3.401361               1.0  0.052950    2.765000       0.788827 0.312500   0.638336    0.535714
                              Air_Severity_Air_Medium, Water_Severity_Water_Low, Soil_Severity_Soil_Low                                              Overall_Severity_Overall_Low               0.135               0.210    0.090    0.666667 3.174603               1.0  0.061650    2.370000       0.791908 0.352941   0.578059    0.547619
                                                                           Overall_Severity_Overall_Low Air_Severity_Air_Medium, Water_Severity_Water_Low, Soil_Severity_Soil_Low               0.210               0.135    0.090    0.428571 3.174603               1.0  0.061650    1.513750       0.867089 0.352941   0.339389    0.547619
                                                                                   Air_Severity_Air_Low                                              Overall_Severity_Overall_Low               0.145               0.210    0.095    0.655172 3.119869               1.0  0.064550    2.291000       0.794706 0.365385   0.563509    0.553777
                                                                           Overall_Severity_Overall_Low                                                      Air_Severity_Air_Low               0.210               0.145    0.095    0.452381 3.119869               1.0  0.064550    1.561304       0.860093 0.365385   0.359510    0.553777
                                                  Air_Severity_Air_Medium, Overall_Severity_Overall_Low                          Soil_Severity_Soil_Low, Water_Severity_Water_Low               0.110               0.275    0.090    0.818182 2.975207               1.0  0.059750    3.987500       0.745943 0.305085   0.749216    0.572727
Soil_Severity_Soil_Low, Water_Severity_Water_Low, Energy_Consumption_Level_Consumption_High_Consumption                                              Overall_Severity_Overall_Low               0.100               0.210    0.060    0.600000 2.857143               1.0  0.039000    1.975000       0.722222 0.240000   0.493671    0.442857
                                                                                   Air_Severity_Air_Low                      Soil_Severity_Soil_Low, Overall_Severity_Overall_Low               0.145               0.190    0.075    0.517241 2.722323               1.0  0.047450    1.677857       0.739961 0.288462   0.404002    0.455989
                                                                                   Air_Severity_Air_Low                    Water_Severity_Water_Low, Overall_Severity_Overall_Low               0.145               0.155    0.060    0.413793 2.669633               1.0  0.037525    1.441471       0.731481 0.250000   0.306264    0.400445
```

## Phase 3: Model Evaluation and Validation

The Apriori rules were validated using train-test split and 5-fold cross-validation.

Apriori Average Rule Accuracy:

0.44206273776133465

## Phase 4: CNN Classification

A CNN model was trained by converting tabular pollution features into image-like matrices.

CNN Accuracy:

0.925000011920929

Random Forest Accuracy:

1.0

## Generated Visualizations

- Pollution trend graph
- Correlation heatmap
- Frequent itemsets graph
- Association rules scatter graph
- Association rules lift graph
- Apriori cross-validation graph
- CNN confusion matrix
- CNN accuracy graph
- CNN loss graph
- CNN ROC curve
- CNN actual vs predicted graph
- Model comparison graph

## Key Findings

- Apriori provides explainable rules between pollution severity and energy recovery.
- CNN provides predictive classification of pollution severity.
- Random Forest provides a baseline comparison.
- Support, confidence, and lift help evaluate rule strength and usefulness.
- Rule-based learning and CNN-based prediction together provide stronger environmental analysis.

## Actionable Recommendations

- Prioritize high pollution regions with poor energy recovery.
- Improve renewable and waste-to-energy recovery systems.
- Use association rules to identify repeated pollution-energy patterns.
- Use CNN predictions for pollution severity monitoring.
- Apply cross-validation to ensure rule reliability before policy use.

## Conclusion

This project successfully applies Apriori Association Rule Mining, CNN classification, and validation techniques to analyze pollution and energy recovery relationships.