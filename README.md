**HEART DISEASE PREDICTION USING MACHINE LEARNING**

**Project Overview:**

Preventing heart disease has become more important than ever. Data-driven systems for predicting heart conditions can significantly enhance research and prevention efforts, ultimately helping more people lead healthier lives. This is where machine learning proves invaluable. By leveraging machine learning techniques, we can accurately predict the likelihood of heart disease, enabling early intervention and better healthcare outcomes. This project focuses on predicting the presence of heart disease based on clinical features using three machine learning models:

• Logistic Regression

• Decision Tree

• Random Forest

The model is trained and evaluated on a publicly available dataset that includes patient health metrics and diagnoses.

**Objective:**

To develop and compare machine learning models that can accurately classify patients as either having or not having heart disease based on clinical attributes.

**Dataset Description:**

• Source: Kaggle Heart Disease Dataset

• Total Records: 1025

• Attributes: 13 input features + 1 target

**Feature Description:**

age ----> Age of the patient

sex ----> Gender (1 = male, 0 = female)

cp----> Chest pain type (4 values)

trestbps----> Resting blood pressure

chol ----> Serum cholesterol

fbs ----> Fasting blood sugar > 120 mg/dl

restecg ----> Resting electrocardiographic results

thalach ----> Maximum heart rate achieved

exang----> Exercise-induced angina

oldpeak ----> ST depression induced by exercise relative to rest

slope ----> Slope of peak exercise ST segment

ca ----> Number of major vessels (0–3) colored by fluoroscopy

thal----> Thalassemia

target ----> 0 = no disease, 1 = disease

**Exploratory Data Analysis (EDA):**

• No missing values were found in the dataset.

• Data distribution was visualized using:

 - Count plots (target distribution, chest pain type)

 - Heatmap of feature correlation

 - Scatter plot (age vs max heart rate)

 - Pair plots grouped by target class

**Key insights:**

• Certain features like cp, thalach, slope, and oldpeak showed strong correlations with heart disease.

**Data Preprocessing:**

• Features and target were split (X and Y).

• Data was divided into training and testing sets using an 80:20 split.

• Stratified sampling ensured balanced representation of classes in both sets.

**Model Development:**

Three models were trained and evaluated:

**Logistic Regression**

• Suitable for binary classification.

• Simpler model with interpretable coefficients.

• Training Accuracy: 84.8%

• Testing Accuracy: 80.4%

**Decision Tree Classifier**

• Max depth limited to avoid overfitting.

• More flexible and intuitive.

• Training Accuracy: 93.7%

• Testing Accuracy: 88.3%

**Random Forest Classifier**

• Ensemble of decision trees.

• Tuned using parameters like n_estimators, max_depth, and min_samples_split.

• Most accurate among the three.

• Training Accuracy: 93.5%

• Testing Accuracy: 91.2%

• Cross-validation Accuracy: 90.2%

**Evaluation Metrics:**

Each model was evaluated using:

• Accuracy

• Precision, Recall, F1-Score

• Classification Reports

• Confusion Matrix

The Random Forest model showed the best overall performance with the highest F1 score and balanced precision/recall.

**Prediction Pipeline:**

The model can predict heart disease for new data samples using:

python

input_data = (50, 0, 0, 110, 254, 0, 0, 159, 0, 0.0, 2, 0, 2)

input_array = np.asarray(input_data).reshape(1, -1)

prediction = model.predict(input_array)

**Output:**

• 1: Heart Disease Present

• 0: No Heart Disease

**Visualizations:**

• Heatmap to show correlations between features.

• Bar Chart comparing model accuracy.

• Count Plots to observe target class balance.

• Pair Plot for multi-feature visual exploration.

These visualizations help understand both the data and model behavior.

**Conclusion:**

• The project effectively demonstrates how machine learning can assist in medical diagnostics.

• The Random Forest model yielded the best results and is suitable for deployment.

• Feature analysis and visualization provided useful clinical insights.
