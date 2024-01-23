# Airline Passenger Satisfaction Classifier: Project Overview
- Produced a model that accurately predicts the satisfaction of airline passengers
- Uncovered patterns within the data after data cleaning and created insightful, descriptive data visualizations
- Explored various classifiers, including Random Forest, K-Nearest Neighbors, Gradient Booster, and others, using different scoring metrics to identify the optimal model for this scenario
- Conducted hyperparameter tuning on the best-fitting model, which was the XGBoost Classifier
  
This model could aid airlines in identifying dissatisfied passengers, allowing for targeted improvements to enhance their experience and overall satisfaction. Engaging with these passengers for feedback can inform strategies to elevate the airline's appeal, fostering customer loyalty, a positive brand image, and increased revenues.

## Tools Used
**IDE:** Jupyter Notebook

**Language:** Python

**Packages:** Pandas, Numpy, Seaborn, Matplotlib, Scikit-learn, Sci-Py, Plotly

**Dataset:** https://www.kaggle.com/datasets/yakhyojon/customer-satisfaction-in-airline?resource=download

## Data Cleaning
Problems in the initial dataset were encountered that posed challenges to data readability and comprehension. Due to these, the following adjustments were implemented: 
- Correctly assigned numerical, categorical, and binary features to separate lists
- Dropped rows with null values
- Removed outliers
  
## Exploratory Data Analysis
Generated a multitude of different graphs and dataframes to bring to light specific aspects of the data.

Graph A: Satisfied passengers generally exhibited higher average ratings in all categories, except for gate location and departure/arrival time convenience.
![image](https://github.com/kyle-flores/Airline-Passenger-Satisfaction-Classifier/assets/153465652/ad97271f-ed2f-4fcd-9b41-851d3518ad0f)

DataFrame B: The most significant differences in ratings between dissatisfied and satisfied customers were found in inflight entertainment, ease of online booking, and online support.
![image](https://github.com/kyle-flores/Airline-Passenger-Satisfaction-Classifier/assets/153465652/c735bd1c-d0a3-44fe-ad4a-300edc8f4320)

## Data Preprocessing
After data cleaning, the data still had some complexities that were addressed before modeling. Preprocessing changes included:
- Applied a logarithmic transformation to address right-skewed features that
- Transformed categorical variables into dummy variables
- Split dataset into training and test sets of 80-20 splits

## Model Building
To predict passenger satisfaction, a diverse set of classification models was explored, leveraging the unique characteristics of the dataset. The following classification models were considered: Gradient Boosting, Random Forest, XGB, Logistic Regression, and others.

## Model Performance

Model performance was evaluated using multiple metrics, each offering unique insights into the classifier's effectiveness. The four primary metrics considered were:

1. **Accuracy:**
   - **Definition:** The ratio of correctly predicted instances to the total instances.
   - **Interpretation:** Measures overall correctness but may be misleading in the presence of imbalanced classes.

2. **Precision:**
   - **Definition:** The ratio of correctly predicted positive observations to the total predicted positives.
   - **Interpretation:** Indicates the model's ability to avoid false positives.

3. **Recall:**
   - **Definition:** The ratio of correctly predicted positive observations to the all observations in actual class.
   - **Interpretation:** Reflects the model's capability to capture all relevant instances of the positive class.

4. **F1 Score:**
   - **Definition:** The harmonic mean of precision and recall.
   - **Interpretation:** Especially useful when dealing with imbalanced datasets, as it balances the trade-off between precision and recall.

### Metric Importance

While all metrics provide valuable information, particular emphasis was placed on the F1 score. Because of the uneven distribution of classes in the dataset, the F1 score was a robust metric for evaluating the model's effectiveness across both classes. The F1 score provides a balanced measure of precision and recall, making it well-suited for scenarios where class distributions are imbalanced.

## Model Performance

All models exhibited a fine performance, as illustrated in the table below:

![Model Performance Table](https://github.com/kyle-flores/Airline-Passenger-Satisfaction-Classifier/assets/153465652/1992b326-6a44-4bf4-9147-8fdb5e84564d)

### Interpretation of Model Performance

The table provides a comprehensive overview of the performance metrics for each classification model. Key insights include:

- **Random Forest Classifier:** Boasted the highest mean performance across metrics
- **XGBoost Classifier:** Displayed the highest F1 score and demonstrated lower sensitivity to overfitting compared to the Random Forest 

## Best Performing Models

While the Random Forest Classifier demonstrated the highest overall mean performance, the choice for the best-performing model was guided by specific considerations. The XGBoost Classifier, with its superior F1 score and apparent less proneness to overfitting, was selected as the optimal model for further tuning.

### Insights and Implications

The best-performing model achieved approximately 96% precision, recall, and F1 score. With the use of increased computational power, fine-tuning the model parameters could push these scores closer to 100%, optimizing its predictive capabilities.

## Conclusion

This project that developed a classifier presents a valuable tool for airlines seeking to enhance passenger satisfaction. By leveraging the insights gleaned from this model, airlines can tailor targeted strategies to address specific areas of improvement. The implementation of personalized services and proactive measures in response to identified patterns can have a profound impact on overall customer experience.

This project not only provides a robust predictive model but also opens avenues for continuous improvement in airline services. As the industry evolves, the integration of such data-driven approaches can contribute to elevated customer satisfaction, brand loyalty, and sustained business growth.

The success of this project highlights the potential of data science in shaping and optimizing customer-centric strategies within aviation.
