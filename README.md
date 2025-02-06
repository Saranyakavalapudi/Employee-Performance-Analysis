
# Employee Performance Analysis

## Project Overview:
The goal of this project is to predict employee performance ratings based on various features from the dataset. We aim to analyze employee performance, identify factors affecting it, and build a predictive model that can forecast performance ratings.

### Business Case & Project Goal:
Given an employee dataset, the objective is to predict the performance rating of employees based on different attributes. These insights will help in improving hiring decisions and guiding strategies to enhance overall employee performance.

## Key Insights and Goals:
1. **Department-wise Performance Analysis**  
   Identify the top 3 factors affecting employee performance across different departments.

2. **Predictive Model**  
   Create a model that can predict an employee's performance based on available data. This model will help in recruitment decisions and performance management.

3. **Actionable Recommendations**  
   Provide suggestions based on data-driven insights to improve employee performance within the organization.

## Dataset Overview:
The dataset consists of 1,200 rows and 28 features, including both quantitative and qualitative attributes. These features are classified into:
- **Quantitative**: 19 features (11 numerical, 8 ordinal)
- **Qualitative**: 8 features
The "EmpNumber" column, containing alphanumeric data, was excluded as it doesn't affect the performance rating.

### Important Features:
- **Target Variable**: PerformanceRating (Ordinal)
- **Categorical Features**: Gender, Education Background, Marital Status, etc.
- **Numerical Features**: Age, Distance From Home, Salary, Work Experience, etc.
- **Ordinal Features**: Job Satisfaction, Job Involvement, Work-Life Balance, etc.

## Data Analysis:

### 1. **Univariate, Bivariate & Multivariate Analysis**:
- **Univariate Analysis**: Analyzed individual feature distributions (e.g., age, salary).
- **Bivariate Analysis**: Examined the relationship between features and the target variable (performance rating).
- **Multivariate Analysis**: Analyzed the relationship between two or more variables with respect to the target.

### Conclusion:
- **Positively Correlated Features**: Employee Environment Satisfaction, Salary Hike Percentage, Work-Life Balance.

## Exploratory Data Analysis (EDA):

### 2. **Feature Distribution**:
- **Age Distribution**: Most employees are aged between 30 and 40 years.
- **Experience**: Majority of employees have worked 1-5 years at the company.
- **Salary Hike**: Most employees received a salary hike between 11% to 15%.

### 3. **Skewness and Kurtosis**:
- **Skewed Data**: "Years Since Last Promotion" is positively skewed.
- **Kurtosis**: The data distribution is relatively normal, with some slight peaks and tails.

### 4. **Data Preprocessing**:
- **Missing Values**: No missing values found in the dataset.
- **Categorical Data Encoding**: Used Manual and Frequency encoding to convert categorical features into numerical data.
- **Outliers**: Handled using Interquartile Range (IQR) method.
- **Feature Transformation**: Applied square root transformation to correct skewness in the "Years Since Last Promotion" feature.
- **Scaling**: Standardized data using StandardScaler to ensure features are on a similar scale.

## Feature Selection:
1. **Dropped Unique and Constant Features**: Removed "EmpNumber" as it was irrelevant and "YearsSinceLastPromotion" due to square root transformation.
2. **Correlation Check**: Ensured there were no highly correlated features.
3. **PCA**: Reduced the dataset to 25 features using Principal Component Analysis (PCA) to improve model performance.

## Machine Learning Model Creation & Evaluation:

### 5. **Data Balancing**:
Since the dataset was imbalanced, we used SMOTE (Synthetic Minority Oversampling Technique) to balance the classes.

### 6. **Model Training**:
We trained and evaluated the following machine learning models:
1. **Support Vector Machine (SVM)**: Achieved 98.28% accuracy on the training set, but overfitting was observed with 94.66% on the test set.
2. **Random Forest**: Perfect accuracy on the training set, but slightly lower on the test set (95.61%).
3. **Artificial Neural Network (ANN)**: Best performing model with 95.80% accuracy on the test set.

### Final Model Selection:
- Based on performance, we selected the **Artificial Neural Network (ANN)** model for predicting employee performance ratings.

## Saving the Model:
The trained model was saved using the **Pickle** library for future use and deployment.

## Tools and Libraries Used:
### Tools:
- **Jupyter Notebook**

### Libraries:
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Pickle

---

### Key Insights and Recommendations:

1. **Department-wise Performance**:
   - **Sales**: Performance rating 3 is most common in this department. Male employees perform slightly better than females.
   - **Human Resources (HR)**: Female employees tend to perform better, while older employees show lower performance.
   - **Development**: Most employees perform at level 3, with no significant gender-based difference.
   - **Data Science**: The highest performance rating (level 3) is common here, with male employees slightly outperforming females.
   - **Research & Development (R&D)**: Performance is consistent across different age groups, with female employees excelling.
   - **Finance**: Employee performance decreases as age increases, with male employees performing better overall.

2. **Top 3 Factors Affecting Employee Performance**:
   - **Employment Environment Satisfaction**
   - **Employee Salary Hike Percentage**
   - **Experience Years in Current Role**

   These features have the most significant impact on the employee performance rating. Improving these factors will likely boost performance.

3. **Model Accuracy**:
   - **SVM**: 98.28% (training), 94.66% (testing)
   - **Random Forest**: 100% (training), 95.61% (testing)
   - **Artificial Neural Network (ANN)**: 98.95% (training), 95.80% (testing)

4. **Recommendations for Improving Employee Performance**:
   - Focus on **employee environment satisfaction**, as it has a significant impact on performance.
   - Offer **salary hikes** (11-19%) to improve performance ratings.
   - Promote employees every 6 months to keep them motivated.
   - Improve **work-life balance** to positively affect performance ratings.
   - In **HR recruitment**, consider female candidates, as they tend to perform better in certain departments.
   - **Development** and **Sales** departments are performing well overall, so strategies from these departments can be adopted elsewhere.
   - Employees who report low or medium satisfaction in **Job Satisfaction** and **Relationship Satisfaction** tend to perform excellently. These employees should be nurtured and supported.

---
