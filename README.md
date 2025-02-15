# Machine-Learning-Project
EDA and creating 5 ML models to predict if the specific customer will cancel the reservation. Made in Jupyter Notebook (Python).

# Hotel Reservation Cancellation Prediction

## Project Overview
This project aims to develop a machine learning model that predicts whether a customer will cancel a hotel reservation. The objective is to help hotel managers anticipate last-minute cancellations and optimize bookings.

## Dataset
The dataset contains various features related to hotel reservations, such as:
- Number of adults and children in the reservation
- Duration of stay (weekend and weekday nights)
- Type of meal plan selected
- Requirement for car parking
- Room type reserved
- Lead time before arrival
- Market segment type
- Previous cancellations and non-canceled bookings
- Average price per room per day
- Number of special requests

## Target Variable
- **Booking Status**: Whether the reservation was **Canceled** or **Not Canceled**.

## Data Preprocessing
- Removed unnecessary columns (`Booking_ID`, `arrival_date`)
- Checked for missing values (none found)
- Converted categorical features into appropriate formats
- Handled outliers using the mean ± 3 standard deviations approach
- Applied feature scaling and encoding
- Balanced the dataset using **oversampling (SMOTENC)** and **undersampling (RandomUnderSampler)**

## Machine Learning Models
The following machine learning models were implemented:
1. **Naïve Bayes**
2. **Decision Tree**
3. **Random Forest**
4. **Extra Trees (Extremely Randomized Trees)**
5. **Support Vector Machine (SVM)**

### Model Evaluation Metrics
Each model was evaluated using:
- **Accuracy**
- **Sensitivity (Recall)**
- **Precision**
- **Specificity**
- **AUC-ROC Curve**

## Best Performing Model: Extra Trees Classifier
- **Accuracy**: ~89%
- **Sensitivity**: ~84%
- **Specificity**: ~92%
- **Key Parameters**: `min_samples_split=5`, `max_depth=None`, `criterion='entropy'`, `n_estimators=100`
- **Top 3 Features**: `lead_time`, `avg_price_per_room`, `no_of_special_requests`

## Insights & Interpretability
### Ceteris Paribus (PCP) Analysis:
- Longer lead time increases cancellation probability.
- Higher average room price correlates with higher cancellation rates.
- More special requests decrease the likelihood of cancellation.

### Feature Importance (SHAP & Break-down Analysis):
- **Lead Time** has the highest influence on booking status.
- **Market segment type** (Online bookings have higher cancellation rates).
- **Previous cancellations** impact future behavior significantly.

## Conclusion
The **Extra Trees** model outperforms other algorithms, making it the best choice for predicting hotel reservation cancellations. Future work can explore deep learning models or additional features for improved accuracy.

## How to Run the Project
### Prerequisites:
- Python 3.x
- Jupyter Notebook (optional)
- Required libraries:
```bash
pip install pandas numpy seaborn scikit-learn imbalanced-learn matplotlib dalex shap
```

### Running the Model
1. Load the dataset.
2. Perform preprocessing as outlined above.
3. Train models and evaluate performance.
4. Generate feature importance plots and interpret the model.

## Repository Structure
```
├── data/                 # Dataset (not included in the repo)
├── notebooks/            # Jupyter notebooks for analysis
├── models/               # Saved models
├── src/                  # Source code for preprocessing and model training
├── README.md             # Project documentation
```

## Acknowledgments
This project utilizes open-source libraries for machine learning and data visualization. Special thanks to the contributors of **Scikit-Learn, Imbalanced-Learn, SHAP, and Dalex** for their powerful tools.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

