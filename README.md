# E-Commerce-Product-Delivery-Prediction
This project predicts whether e-commerce products will be delivered on time using machine learning. By analyzing customer behavior, product details, shipment methods, and discounts, it identifies key factors affecting delivery performance and helps improve customer satisfaction and logistics efficiency.

# 📦 E-Commerce Product Delivery Prediction

## 📌 Project Overview

The rapid growth of e-commerce has increased the importance of timely product delivery. Delayed deliveries can negatively impact customer satisfaction and business performance. This project aims to predict whether a product will be delivered on time using machine learning techniques.

By analyzing customer behavior, product characteristics, shipment methods, and discount patterns, the project identifies the key factors influencing delivery performance.

---

## 🎯 Project Objective

The objective of this project is to:

- Predict whether a product will be delivered on time.
- Identify factors affecting delivery delays.
- Analyze customer behavior and shipment patterns.
- Compare multiple machine learning models.
- Improve delivery efficiency through data-driven insights.

---

## 📂 Dataset Overview

- **Total Records:** 10,999 rows
- **Total Features:** 12 columns
- **Target Variable:** `Reached.on.Time_Y.N`

### Target Variable

| Value | Meaning |
|-------|---------|
| 1 | Delivered On Time |
| 0 | Delivery Delayed |

### Key Attributes

| Feature | Description |
|---------|-------------|
| Warehouse_block | Source warehouse of shipment |
| Mode_of_Shipment | Transport method (Ship, Flight, Road) |
| Customer_care_calls | Number of customer service calls |
| Cost_of_the_Product | Product price |
| Discount_offered | Promotional discounts |
| Product_importance | Low, Medium, High |
| Weight_in_gms | Product weight |
| Reached.on.Time_Y.N | Delivery status |

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 🔄 Data Preprocessing

The following preprocessing steps were performed:

- Checked for missing values.
- No missing values were found.
- Converted categorical variables into numerical values using encoding techniques.
- Applied encoding for:
  - Warehouse Block
  - Product Importance
  - Gender
- Normalized numerical features such as:
  - Cost of Product
  - Weight in grams
- Split the dataset into:
  - **Training Set:** 80%
  - **Testing Set:** 20%

---

## 📊 Exploratory Data Analysis (EDA)

### Gender Distribution

- Nearly equal representation of male and female customers (~50%).

### Product Insights

- Products weighing **2500–3500 grams** are more likely to be delivered on time.
- Products costing below **$250** are more likely to arrive on time.

### Customer Behavior

- High customer care calls often indicate delayed deliveries.
- Repeat customers generally experience better delivery outcomes.

### Discount Impact

- Minimal discounts (0–10%) lead to more late deliveries.
- Higher discounts (>10%) correlate with timely deliveries.

---

## 🔥 Correlation Analysis

### Positive Correlation

- **Product Cost ↔ Customer Care Calls**
  - Higher-value products generate more customer inquiries.

### Negative Correlation

- **Discount Offered ↔ Delivery Delays**
  - Higher discounts improve delivery punctuality.

A correlation heatmap was used to visualize the relationships among numerical variables.

---

## 🤖 Machine Learning Models

### 1. Decision Tree Classifier

- Hyperparameter tuning using Grid Search.
- Best Parameters:
  - Max Depth: 8
  - Minimum Samples Split: 2

### 2. Random Forest Classifier

- Ensemble learning approach.
- Improved prediction performance.

### 3. Logistic Regression

- Used to interpret linear relationships between features.

### 4. K-Nearest Neighbors (KNN)

- Distance-based classification algorithm.

---

## 📈 Model Evaluation

### Training Accuracy

- Ranged between **63% – 78%**

### Testing Accuracy

- Ranged between **63% – 69%**

### Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-Score

---

## 🏆 Model Performance

| Model | Test Accuracy |
|------|--------------|
| Decision Tree Classifier | 69% |
| Random Forest Classifier | 68% |
| K-Nearest Neighbors | 65% |
| Logistic Regression | 63% |

---

## 🔍 Key Findings

- Products weighing between **2500–3500 grams** had higher on-time delivery rates.
- High-value products (**>$250**) experienced more delays.
- Warehouse operations significantly affect delivery performance.
- Frequent customer care calls indicate possible delivery issues.
- Repeat customers tend to receive more reliable deliveries.
- Discounts greater than **10%** improve delivery punctuality.

---

## ✅ Conclusion

The objective of this project was to predict whether e-commerce products would reach customers on time and identify factors influencing delivery performance.

Exploratory analysis revealed that product weight, product cost, discounts, and customer behavior play important roles in delivery outcomes.

Among all machine learning models, the **Decision Tree Classifier** achieved the highest accuracy of **69%**, making it the best-performing model for this dataset.

These insights can help e-commerce companies optimize logistics, improve customer satisfaction, and reduce delivery delays.

---

## 🚀 Future Improvements

- Perform advanced feature engineering.
- Implement boosting algorithms such as XGBoost and LightGBM.
- Deploy the model using Streamlit or Flask.
- Integrate real-time logistics data.
- Improve model performance through advanced hyperparameter tuning.

---

## 📁 Project Structure

```bash
E-Commerce-Product-Delivery-Prediction/
│
├── dataset/
│   └── E_Commerce.csv
│
├── notebooks/
│   └── E-commerce product delivery prediction.ipynb
│
├── presentation/
│   └── E-Commerce Capstone.pptx
│
├── README.md
│
└── requirements.txt
