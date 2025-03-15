# **Predicting Sales for Luther's Scoops Using Machine Learning**

## **📌 Project Overview**
I love ice creame! This project builds and evaluates machine learning models to **predict daily ice cream sales** for **Luther's Scoops** - my all time favourite ice cream shop in Melbourne. By analyzing historical sales data, I identify key factors that drive sales and optimize pricing, promotions, and inventory management.

## **📊 Dataset**
- **Source:** Luther's Scoops sales data.
- **Size:** 17,532 entries, 16 columns.
- **Key Features:**
  - **Date-based:** Date, Weekday, Season
  - **Product-based:** Flavor, Price per scoop, Promotion
  - **Weather-based:** Temperature, Rainfall
  - **Event-based:** Special events, Customer traffic, Social media sentiment
  - **Target Variable:** `units_sold` (number of scoops sold per day)

## **⚙️ Methodology**
### **1️⃣ Data Preprocessing & Feature Engineering**
✔ Handled missing values (dropped missing target values, imputed categorical data).  
✔ Removed `total_revenue` to prevent **data leakage**.  
✔ Created new features (extract Date feature to 3 features Day, Month, Year).  
✔ Automated the data preprocessing for ML using **Scikit-Learn Transformation Pipelines** (for standardized numerical features and encoded categorical variables).

### **2️⃣ Model Training & Evaluation**
✅ **Tried 3 models:**  
- **Linear Regression** ✅ (Best-performing model)
- **Decision Tree Regressor**
- **Random Forest Regressor**

✅ **Evaluation Metric:** Root Mean Squared Error (RMSE)
- **Train RMSE:** 5.9
- **Test RMSE:** 6.0 (**Good generalization!**)

## **📈 Key Findings**
🔹 **Price Sensitivity:** Higher prices **decrease** sales (-0.29 coefficient).  
🔹 **Event Days Drive Sales:** `event_Yes` **strongly increases** sales (+9.72).  
🔹 **Promotions Are Not Always Effective:** `promotion_No` **increases** sales more than `promotion_Yes`.  
🔹 **Seasonality Matters:** Fall has **higher sales**, while Winter has **lower sales**.  
🔹 **Weather Affects Sales:** Rain negatively impacts sales (-0.64).  

## **🚀 Future Improvements**
🔸 Try **Regularized Models (Ridge, Lasso, ElasticNet)** to handle correlated features.  
🔸 Test **Price Elasticity Models** to find optimal pricing.  
🔸 Use **Time Series Forecasting (ARIMA, Prophet, LSTMs)** for seasonal trends.  
🔸 Implement **Feature Selection** to remove unimportant variables.  

## **💻 Installation & Usage**
### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/yourusername/luthers-scoops-sales-prediction.git
cd luthers-scoops-sales-prediction
```

### **2️⃣ Install Required Packages**
```sh
pip install -r requirements.txt
```

### **3️⃣ Run the Jupyter Notebook**
```sh
jupyter notebook
```

## **📬 Contact**
If you have any questions or suggestions, feel free to reach out!
- **LinkedIn:** [Your LinkedIn Profile](linkedin.com/in/anquach01)
