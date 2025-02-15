# Hotel Reservation Cancellation Prediction 🏨💡

## Project Overview 🚀
This project aims to develop a machine learning model that predicts whether a customer will cancel a hotel reservation. The objective is to help hotel managers anticipate last-minute cancellations and optimize bookings.

## Dataset 📊
The dataset contains various features related to hotel reservations, such as:
- Number of adults and children in the reservation 👨‍👩‍👦
- Duration of stay (weekend and weekday nights) 🏠
- Type of meal plan selected 🍽️
- Requirement for car parking 🚗
- Room type reserved 🏢
- Lead time before arrival 📅
- Market segment type 📈
- Previous cancellations and non-canceled bookings ❌✅
- Average price per room per day 💰
- Number of special requests ✨

Dataset comes from Kaggle: https://www.kaggle.com/datasets/ahsan81/hotel-reservations-classification-dataset. Thanks for creating and sharing it!

## Target Variable 🎯
- **Booking Status**: Whether the reservation was **Canceled** or **Not Canceled**.

## Data Preprocessing ⚙️
- Removed unnecessary columns (`Booking_ID`, `arrival_date`)
- Checked for missing values (none found)
- Converted categorical features into appropriate formats
- Handled outliers using the mean ± 3 standard deviations approach
- Applied feature scaling and encoding
- Balanced the dataset using **oversampling (SMOTENC)** and **undersampling (RandomUnderSampler)**

## Machine Learning Models 🤖
The following machine learning models were implemented:
1. **Naïve Bayes**
2. **Decision Tree**
3. **Random Forest**
4. **Extra Trees (Extremely Randomized Trees)**
5. **Support Vector Machine (SVM)**

### Model Evaluation Metrics 📏
Each model was evaluated using:
- **Accuracy**
- **Sensitivity (Recall)**
- **Precision**
- **Specificity**
- **AUC-ROC Curve**

## Best Performing Model: Extra Trees Classifier 🏆
- **Accuracy**: ~89%
- **Sensitivity**: ~84%
- **Specificity**: ~92%
- **Key Parameters**: `min_samples_split=5`, `max_depth=None`, `criterion='entropy'`, `n_estimators=100`, `Oversampling`

## Insights & Interpretability - Images in Interpretability Section!!! 🔍
### Ceteris Paribus (PCP) Analysis (based on 1 observation):
### Feature Importance (SHAP & Break-down Analysis):
🖼️ **Images in Interpretability Section** 📸
- **Lead Time** has the highest influence on booking status.
- **Market segment type** (Online bookings have higher cancellation rates).
- **Previous cancellations** impact future behavior significantly.
### Shap values and break-down charts

## Conclusion ✅
The **Extra Trees** model outperforms other algorithms, making it the best choice for predicting hotel reservation cancellations. 

## Polish & English Versions 🌍📝
This project documentation is available in both **Polish** and **English** versions.

## Acknowledgments 🙌
This project utilizes open-source libraries for machine learning and data visualization. Special thanks to the contributors of **Scikit-Learn, Imbalanced-Learn, SHAP, and Dalex** for their powerful tools.

