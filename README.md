# **eCommerce Transactions Analysis Project**

This project involves exploratory data analysis (EDA), building a Lookalike Model, and performing customer segmentation using an eCommerce transactions dataset. The goal is to derive actionable business insights, build predictive models, and group customers into meaningful segments.

---

## **Project Overview**
The project is divided into three main tasks:
1. **Exploratory Data Analysis (EDA):** Analyze the data to uncover trends and derive business insights.
2. **Lookalike Model:** Build a model to recommend similar customers based on their profile and transaction history.
3. **Customer Segmentation:** Use clustering techniques to group customers into segments for targeted marketing strategies.

---

## **Dataset Description**
The dataset consists of three files:
1. **`Customers.csv`:**
   - `CustomerID`: Unique identifier for each customer.
   - `CustomerName`: Name of the customer.
   - `Region`: Continent where the customer resides.
   - `SignupDate`: Date when the customer signed up.

2. **`Products.csv`:**
   - `ProductID`: Unique identifier for each product.
   - `ProductName`: Name of the product.
   - `Category`: Product category.
   - `Price`: Product price in USD.

3. **`Transactions.csv`:**
   - `TransactionID`: Unique identifier for each transaction.
   - `CustomerID`: ID of the customer who made the transaction.
   - `ProductID`: ID of the product sold.
   - `TransactionDate`: Date of the transaction.
   - `Quantity`: Quantity of the product purchased.
   - `TotalValue`: Total value of the transaction.
   - `Price`: Price of the product sold.

---

## **Task 1: Exploratory Data Analysis (EDA)**
### **Steps Performed**
- Merged datasets to create a consolidated view of transactions.
- Analyzed trends in sales, customer behavior, and product performance.
- Identified high-value customers and popular products.

### **Key Business Insights**
1. **Top-Selling Regions:** Regions with the highest sales volume and revenue were identified, helping target regional marketing efforts.
2. **Peak Sales Periods:** Sales trends revealed peak seasons and times for transactions.
3. **High-Value Customers:** Customers contributing significantly to revenue were identified for loyalty programs.
4. **Popular Products:** Products with the highest sales volume and revenue were highlighted.
5. **Spending Patterns:** Insights into average customer spending by region and category were derived.

---

## **Task 2: Lookalike Model**
A Lookalike Model was developed to find similar customers based on their profile and transaction history.

### **Methodology**
- Customer profiles were created using aggregated metrics like average spending, purchase frequency, and preferred product categories.
- Cosine similarity was used to measure the similarity between customer profiles.

### **Output**
- Generated a file, `Lookalike_Output.csv`, mapping the top 3 similar customers with similarity scores for the first 20 customers (`C0001` to `C0020`).

---

## **Task 3: Customer Segmentation**
### **Objective**
To group customers into meaningful clusters based on their demographic and transactional data.

### **Methodology**
- Features like customer region, spending patterns, and product preferences were used.
- K-Means clustering was applied, and the optimal number of clusters was determined using the Davies-Bouldin Index (DB Index).

### **Results**
- **Number of Clusters:** (e.g., 4 clusters)
- **DB Index Value:** (e.g., 0.75)
- Visualized clusters using scatter plots and heatmaps to understand segmentation.

---

## **Technologies Used**
- **Programming Language:** Python
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn

---

## **File Structure**
```
eCommerce_Analysis_Project/
│
├── Updated_Customers.csv         # Updated customer dataset
├── Updated_Products.csv          # Updated product dataset
├── Updated_Transactions.csv      # Updated transaction dataset
├── analysis_script.py            # Main script for the project
├── Lookalike_Output.csv          # Output of the Lookalike Model
├── clustering_visualizations/    # Folder for clustering plots
└── README.md                     # Project description
```

---

## **How to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/eCommerce_Analysis_Project.git
   ```
2. Navigate to the project folder:
   ```bash
   cd eCommerce_Analysis_Project
   ```
3. Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the script:
   ```bash
   python analysis_script.py
   ```

---

## **Future Enhancements**
- Implement advanced recommendation systems using collaborative filtering or deep learning.
- Incorporate time-series analysis for better sales forecasting.
- Explore customer churn prediction using transactional and profile data.


