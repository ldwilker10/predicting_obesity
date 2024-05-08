# predicting_obesity

# Predicting Obesity with Demographic and Lifestyle Factors

# Elevator Pitch
Obesity is a pressing global issue affecting millions. Leveraging the comprehensive BRFSS dataset, our model accurately predicts obesity based on lifestyle and demographic factors. With crucial insights, we can empower individuals and policymakers to make informed decisions, ultimately combating the obesity epidemic effectively.

![obesity_header](https://github.com/ldwilker10/predicting_obesity/blob/main/images/health_obesity_header_image.jpg)


#### Project by: Lucas Wilkerson
#### Date: 5/10/2024

## Project Overview


## Business Understanding (Problem/Stakeholder)

Obesity is a significant public health concern in the United States and globally that contributes to adverse effects on an individual's health and places a great economic burden on healthcare systems. Addressing obesity requires a comprehensive understanding of its determinants and what various lifestyle factors and influencers seem to contribute to its prevalence. 

With obesity being significant issue that can have problematic implications, a team of public health professionals is seeking to understand what various factors contribute to obesity and could predict the development of obesity diagnosis. By understanding the various lifestyle, diet and demographic factors that lead to obesity, they can develop plans and interventions to both reduce obesity rates and improve overall health. 

To help determine the best areas of focus, this project aims to investigate the various diet, demographic and lifestyle factors that contribute to obesity rates within the US population by exploring the Behavioral Risk Factor Surveillance System (BRFSS) dataset. I plan to use exploratory data analysis to understand the data and help determine what factors best contribute to obesity. From there, predictive modeling will be incorporated to develop a model to predict or classify obesity based on the data and the features uncovered. 

The findings from this analysis will be able to help inform and guide public health strategies, interventions, and policies aimed at reducing obesity rates and promoting healthier lifestyles. 



## Data Understanding 

The primary dataset for this project is from the Behavioral Risk Factor Surveillance System (BRFSS) dataset, available on Kaggle and also found on the CDC's website. The BRFSS is done annually via telephone surveys, and provides comprehensive data that is collected from U.S. residents regarding their health-related risk behaviors, chronic health conditions, their use of preventive services, and other various diet and lifestyle factors. The dataset includes variables such as demographics (age, gender, race/ethnicity), physical activity levels, health indicators (obesity status), and other various factors. 

This dataset from the 2022 BRFSS contains 445132 entries and have 326 columns representing the multiple features. For this analysis, I plan to use a subset of the columns representing a variety of features that could be linked with obesity or may be interesting to explore in relation to the target variable. Upon data cleaning and preparation the final dataset had 209405 entries with 39 columns. 


- Data Source: Behavioral Risk Factor Surveillance System (BRFSS) dataset from Kaggle (https://www.kaggle.com/datasets/ariaxiong/behavioral-risk-factor-surveillance-system-2022/data)
- 
![Behavioral Risk Factor Surveillance System (BRFSS)](https://www.kaggle.com/datasets/ariaxiong/behavioral-risk-factor-surveillance-system-2022/data)

- Link to original data source from the CDC on Data.gov ( https://www.cdc.gov/brfss/annual_data/annual_2022.html)

![Behavioral Risk Factor Surveillance System (BRFSS)](https://www.cdc.gov/brfss/annual_data/annual_2022.html)
 
- For additional feature information and description along the code description for the values, those can be found at the CDC's link for the 2022 BRFSS (https://www.cdc.gov/brfss/annual_data/annual_2022.html)

![BRFSS Codebook](https://www.cdc.gov/brfss/annual_data/annual_2022.html)

Obesity Prevalence in cleaned dataset:

![obesity_prevalence](https://github.com/ldwilker10/predicting_obesity/blob/main/images/obesity_prevalence.png)



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

The best model of the adjusted/tuned nerual network model had an architecture made of multiple dense layers with adjustments made to the learning rate, number of filters, class balance, batch size and number of epochs. Learning rate was adjust to 0.001 and batch size was equal to 50 with total epochs being 5. The Best Model had a test accuracy of 0.7006 and test recall of 0.9324, which indicates that out of all of the individuals with obesity, the model correctly labeled ~93.24% of the individuals that actually. Performance with test recall and test accuracy were improved compared to baseline, however f1 score was slightly lower. 

With the best performing model (tuned neural network) the scores were:

- Model's Accuracy Score: 0.7005801200866699
- Model's F1 Score: 0.6671204566955566
- Model's Recall Score: 0.9323569536209106




## Evaluation

The adjusted/tuned neural network model is the ideal model to choose here because it performs better at correctly classifying/ predicting individuals as shown by the slight improvement in test accuracy, test recall, and f1-score. While this model is higher with recall and correctly identifying those with obesity, there is the chance for more false positive results (individuals being classified as having obesity who in fact do not). This is more ideal because we would rather correctly identify positive cases than to not identify someone with obesity because interventions or recommendations that are usually geared towards addressing obesity are generally good recommendations for anyone to partake in or be aware of for health in general.

![image](link)


![image](link)


## Conclusion/ Recommendations 

The tuned neural network model showed the best performance in identifying those with obesity based on the various features and demogrpahics and lifestyle factors. The model showed that out of all individuals with obesity, it could correctly identify 93.23 % of those individuals. This can provide great benefit for public health professionals by increasing detection and allowing targeted and specific interventions. By adressing this health concern early, this can improve an individuals quality of life and overall health outcomes by preventing accerleration of disease and negative health consequences while also decreasing the load on the healthcare system and the providers.

Recommendations:

- Public health professionals should utilize this model as an additional tool when determining public health initiatives/ interventions aimed at obesity. 

- While this model is not an official diagnostic tool for obesity, this model can be utilized for identification. Using this model, preventative health methods, such as dietary education or exercise recommendations, could be implemented early on before disease progression or development of other co-morbidities.

- Public Health Policy makers should also utilize this model and information to develop targeted interventions based on the most influence features that seem to contribute to obesity.

- In the context of identifying obesity status and risk, public health education and interventions should take into account an individuals ethnicity/race and/ or cultural customs, the individuals number of children and also their past medical history related to heart condition. 


## Limitations

While the model can be useful to predicting individuals with obesity based on various health and lifestyles factors, the model is not perfect and does have it's limitations.

- False positives: When individuals actually have obesity, the model correctly identifies those indiviudals approximiately 93.23% of the time. With having a higher recall, there is an increased risk of mislabeling indiviudals without obesity as having obesity. While there is this increased chance, having an increased risk of incorrectly identifying someone as having obesity is a better trade off in this situation that incorrectly labeling someone as not having obesity when they in fact do have obesity. If someone is labeled as a false positive, recommending lifestyle interventions to address obesity could still be good advice as a preventative thought to a healthy normal weight individiual. 

- Data loss: the initial dataset was very large with more columns and numerous missing values. To less the burden on computation power and speed up run times, numerous null values were dropped and the dataset was subsampled to run models on a smaller training percentage. 

- Numerous Features: Only a subset of features/ columns were explore leading other features to no be accounted for which could potentially have affects on the target variable. 


## Contact Information

- Email: ldwilker10@gmail.com

- GitHub: https://github.com/ldwilker10

- LinkedIn: https://www.linkedin.com/in/lucasdukewilkerson/ 

## Repository Structure

├── data                                                                                                                                 
├── draft_notebooks     
├── images   
├── .gitignore                                                                                                                   
├── [README.md](https://github.com/ldwilker10/predicting_obesity/blob/main/README.md)                                          
├── [notebook.ipynb](https://github.com/ldwilker10/predicting_obesity/blob/main/notebook_final.ipynb)       
└── [presentation.pdf](link)   