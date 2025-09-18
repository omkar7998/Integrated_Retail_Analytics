# Integrated_Retail_Analytics

# Sales Prediction ML Project

## **Project Overview**
This project aims to **predict weekly sales** for retail stores using machine learning. It includes **data preprocessing, feature engineering, model building, hyperparameter tuning, and model evaluation**. The final goal is to build an accurate and interpretable ML model that can help businesses make **data-driven decisions** like inventory planning, promotions, and staffing.

---

## **Dataset**
The project uses three datasets:  
1. `Features_cleaned.csv` – Store features such as temperature, fuel price, markdowns, CPI, unemployment, and holiday information.  
2. `sales data-set.csv` – Weekly sales for each store.  
3. `stores data-set.csv` – Store type and size information.

---

## **Project Steps**

### 1. **Data Preprocessing**
- Handling **missing values** (mean for numeric, mode for categorical).  
- Treating **outliers** using IQR capping.  
- **Encoding categorical variables** using Label Encoding.  
- **Scaling numeric features** using StandardScaler.  
- Saving the preprocessed dataset as `Features_preprocessed.csv`.

### 2. **Feature Engineering**
- Creating new features where necessary.  
- Selecting important features to avoid overfitting.

### 3. **Model Implementation**
- Implemented **3 ML models**:
  - Random Forest Regressor
  - XGBoost Regressor
  - Gradient Boosting Regressor
- Evaluated using **Mean Squared Error (MSE)** and **R² Score**.

### 4. **Hyperparameter Tuning**
- Used **GridSearchCV** to find the best parameters for Gradient Boosting Regressor.  
- Achieved **improved performance** (higher R², lower MSE).

### 5. **Model Explainability**
- Used **feature importances** and **SHAP values** to interpret which features influence sales predictions.

### 6. **Model Deployment**
- Saved the best model using **pickle** and **joblib** (`best_model.pkl` and `best_model.joblib`).  
- Demonstrated predicting on **unseen data** as a sanity check.

---

## **Evaluation Metrics**
| Metric | Description | Business Impact |
|--------|-------------|----------------|
| MSE    | Measures average prediction error | Lower MSE → more accurate sales predictions → better inventory & financial planning |
| R²     | Measures variance explained by the model | Higher R² → model captures trends effectively → data-driven decisions |

---

## **Results**
- **Best Model:** Gradient Boosting Regressor  
- **Top Features:** Store, Temperature, Fuel Price, CPI, Unemployment  
- **Performance:** MSE and R² indicate strong predictive capability for weekly sales.

---

## **Future Work**
- Deploy the model in a web or API application for real-time sales predictions.  
- Incorporate additional external features such as promotions, local events, or competitor data for better accuracy.  
- Explore advanced ensemble methods or neural networks for improved performance.

---

## **How to Use**
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/Sales-Prediction-ML.git
