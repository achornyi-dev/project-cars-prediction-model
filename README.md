# Used Car Price Prediction Project 

##  Project Overview
This project focuses on building a machine learning model to predict the selling price of used cars. By analyzing technical specifications and market data, the model provides an accurate estimation of a vehicle's value.

---

##  Data Analysis & Insights
Based on the provided dataset (carsdata.csv), the following key insights were discovered:
* *Year of Manufacture:* Newer cars show a significant premium in price.
* *Engine Power (max_power):* This is the strongest predictor of price; more horsepower directly correlates with higher value.
* *Mileage (km_driven):* There is a clear inverse relationship - higher mileage leads to lower prices.

---

##  Data Preprocessing
To prepare the data for the Machine Learning model, we performed several critical steps:
1. *Cleaning:* Stripped technical units (like bhp, cc, kmpl) from string values.
2. *Type Conversion:* Converted technical data into float types for mathematical processing.
3. *Handling Missing Values:* Dropped rows with null values to maintain data quality.
4. *Feature Selection:* Selected the most impactful variables: year, km_driven, mileage, engine, and max_power.

---

##  Model Justification
We implemented the **Random Forest Regressor**. 

**Why Random Forest?**
* It handles *non-linear relationships* better than simple linear models.
* It is robust against *outliers* (e.g., very expensive luxury cars).
* It reduces the risk of *overfitting* by averaging multiple decision trees.

---

##  Performance Analysis
The model was evaluated on a test dataset, showing excellent results:

| Metric | Value |
| :--- | :--- |
| **R² Score** | **0.98** |
| **Mean Absolute Error (MAE)** | **2444** |

### **Visual Result:**
The "Real vs Predicted" scatter plot confirms that the model's predictions align almost perfectly with actual prices, as most data points sit directly on the diagonal regression line.

---

##  Conclusion
The project successfully developed a high-accuracy model (**98% precision**). This system can be used by car dealerships or individual sellers to determine the fair market price of used vehicles automatically.

---

##  How to Run
1. Clone the repository.
2. Install dependencies: pip install -r requirements.txt.
3. Run the Jupyter Notebook: notebooks/CarsRealvsPredicted.ipynb.
