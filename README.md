# predicting_obesity

# Predicting ___ with ___

# Elevator Pitch

![image](link)


#### Project by: Lucas Wilkerson
#### Date: 

## Project Overview


## Business Understanding (Problem/Stakeholder)

Obesity is a significant public health concern in the United States and globally that contributes to adverse effects on an individual's health and places a great economic burden on healthcare systems. Addressing obesity requires a comprehensive understanding of its determinants and what various lifestyle factors and influencers seem to contribute to its prevalence. 

With obesity being significant issue that can have problematic implications, a team of public health professionals is seeking to understand what various factors contribute to obesity and could predict the development of obesity diagnosis. By understanding the various lifestyle, diet and demographic factors that lead to obesity, they can develop plans and interventions to both reduce obesity rates and improve overall health. 

To help determine the best areas of focus, this project aims to investigate the various diet, demographic and lifestyle factors that contribute to obesity rates within the US population by exploring the Behavioral Risk Factor Surveillance System (BRFSS) dataset. I plan to use exploratory data analysis to understand the data and help determine what factors best contribute to obesity. From there, predictive modeling will be incorporated to develop a model to predict or classify obesity based on the data and the features uncovered. 

The findings from this analysis will be able to help inform and guide public health strategies, interventions, and policies aimed at reducing obesity rates and promoting healthier lifestyles. 



## Data Understanding (make sure to add link to dataset)

The primary dataset for this project is from the Behavioral Risk Factor Surveillance System (BRFSS) dataset, available on Kaggle and also found on the CDC's website. The BRFSS is done annually via telephone surveys, and provides comprehensive data that is collected from U.S. residents regarding their health-related risk behaviors, chronic health conditions, their use of preventive services, and other various diet and lifestyle factors. The dataset includes variables such as demographics (age, gender, race/ethnicity), physical activity levels, health indicators (obesity status), and other various factors. 

This dataset from the 2022 BRFSS contains 445132 entries and have 326 columns representing the multiple features. For this analysis, I plan to use a subset of the columns representing a variety of features that could be linked with obesity or may be interesting to explore in relation to the target variable.  


- Data Source: Behavioral Risk Factor Surveillance System (BRFSS) dataset from Kaggle (https://www.kaggle.com/datasets/ariaxiong/behavioral-risk-factor-surveillance-system-2022/data)
- 
![Behavioral Risk Factor Surveillance System (BRFSS)](https://www.kaggle.com/datasets/ariaxiong/behavioral-risk-factor-surveillance-system-2022/data)

- Link to original data source from the CDC on Data.gov ( https://www.cdc.gov/brfss/annual_data/annual_2022.html)

![Behavioral Risk Factor Surveillance System (BRFSS)](https://www.cdc.gov/brfss/annual_data/annual_2022.html)
 
- For additional feature information and description along the code description for the values, those can be found at the CDC's link for the 2022 BRFSS (https://www.cdc.gov/brfss/annual_data/annual_2022.html)

![BRFSS Codebook](https://www.cdc.gov/brfss/annual_data/annual_2022.html)


![dataset_name](link)

![image](link)

## Data Preparation 

Before building the model, the data underwent several preprocessing steps including:

- Filtering columns down to including necessary columns for anlaysis
- Cleaning data to remove missing/null values and placeholder values
- Data distribution analysis to understand the class balance or imbalance
- Visualizing different features to understand distribution and relationship with variable

  
During data preparation and preprocessing data was prepared for modeling by the following:

- Data was rescaled and normalized to the range [0,1] for modeling 
- Class imbalance was accounted for by utilizing SMOTE
- The data was also subsampled for the modeling process to allow for shorter computation run times. Twenty-five percent of the data was used for training.


## Modeling 

### Baseline Model/ Model 1:

A Baseline Logistic Regression model was constructed for this project. The model was a simplae logistic regression model with defualt parameters. The main metrics used to evaluate model performance included accuracy, recall and f1 score. The baseline model had a test accuracy of 0.6993, test recall of 0.9226, and a test f1 score of 0.6719.

- Model's Accuracy Score: 0.6993164651483386
- Model's F1 Score: 0.6718796521194077
- Model's Recall Score: 0.9226200723016009


### Best Performing Model/ Model 2:
The Best Model had the.



## Evaluation

Evaluation
The Best Model is the ideal model to choose here because it performs better at correctly classifying/ predicting individuals as shown by the slight improvement in test accuracy, test recall, and f1-score. While this model is higher with recall and correctly identifying those with obesity, there is the chance for more false positive results (individuals being classified as having obesity who in fact do not). This is more ideal because we would rather correctly identify positive cases than to not identify someone with obesity because interventions or recommendations that are usually geared towards addressing obesity are generally good recommendations for anyone to partake in or be aware of for health in general.

![image](link)


![image](link)


## Conclusion/ Recommendations 



## Limitations


## Contact Information

- Email: ldwilker10@gmail.com

- GitHub: https://github.com/ldwilker10

- LinkedIn: https://www.linkedin.com/in/lucasdukewilkerson/ 

## Repository Structure

├── folder                                                                                                                                 
├── draft_models     
├── images   
├── .gitignore                                                                                                                   
├── [README.md](link)                                          
├── [notebook.ipynb](link)       
└── [presentation.pdf](link)   