# Music & Mental Prediction

This project aims to explore the correlation between music preferences and mental health conditions, including Anxiety, Depression, and Insomnia. The model utilizes a machine learning approach to classify individuals based on their survey responses.

## Project Overview

- **Objective:** Predict mental health conditions (Anxiety, Depression, Insomnia) using features derived from a music preference survey.
- **Dataset:** The dataset consists of various features including age, preferred music genre, BPM (beats per minute), daily listening hours, and psychological responses.
- **Approach:**
  - **Data Preprocessing:** Handling missing values, filtering outliers, and encoding categorical variables.
  - **Feature Engineering:** Creating numerical and categorical features for model input.
  - **Modeling:** Implementing a Random Forest Classifier for prediction.

## Data Preprocessing & Feature Engineering

- **Filtering Data:**
  - Considered individuals below 70 years of age.
  - Restricted daily listening hours to under 14.
  - Filtered BPM values to a maximum of 220.
- **Handling Missing Values:**
  - Imputed missing BPM values with the mean.
  - Filled missing categorical values with the most frequent category.
- **Vectorization & Normalization:**
  - Categorical features encoded using LabelEncoder.
  - Numerical features standardized using StandardScaler.

## Model Implementation

The classification model was implemented using a **Random Forest Classifier**. Each mental health condition (Anxiety, Depression, Insomnia) was predicted separately.

### Performance Metrics:

#### **Classification Report for Anxiety:**
- **Accuracy:** `0.60`
- **F1-Score (0):** `0.32`
- **F1-Score (1):** `0.72`

#### **Classification Report for Depression:**
- **Accuracy:** `0.58`
- **F1-Score (0):** `0.50`
- **F1-Score (1):** `0.64`

#### **Classification Report for Insomnia:**
- **Accuracy:** `0.48`
- **Macro Avg F1-Score:** `0.37`
- **Weighted Avg F1-Score:** `0.41`

## Feature Importance

The top features influencing mental health predictions include:
1. BPM (Beats Per Minute)
2. Hours per day spent listening to music
3. Favorite music genre
4. Age
5. Primary streaming service

## How to Run the Project

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/abhay-2108/Music-and-Mental-Prediction.git
   ```
2. **Install Dependencies:**
   ```bash
   pip install numpy pandas seaborn matplotlib scikit-learn
   ```
3. **Run the Data Processing Script:**
   ```bash
   python preprocess.py
   ```
4. **Train the Model:**
   ```bash
   python train.py
   ```
5. **Evaluate the Model:**
   ```bash
   python evaluate.py
   ```

## Conclusion

This project highlights the relationship between music preferences and mental health, showcasing how machine learning can be used to predict mental health conditions based on survey data. Future enhancements could include deep learning models for improved accuracy and incorporating additional psychological features for better insights.

