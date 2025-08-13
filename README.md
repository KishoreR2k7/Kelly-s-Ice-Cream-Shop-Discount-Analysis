# Kelly-s-Ice-Cream-Shop-Discount-Analysis
## Project Overview
This project analyzes transactions from Kelly's Ice Cream Shop to identify customer purchasing patterns, calculate discounts, and generate insights.
## Dataset
- **customer_id** – Unique ID for each customer
- **transaction_id** – Unique ID for each transaction
- **amount** – Purchase amount in currency units
### **1. Data Loading & Cleaning**
- Loaded CSV file with **Pandas**.
- Checked for missing values and duplicates.
- Verified column names, data types, and shape.

### **2. Exploratory Data Analysis (EDA)**
- Counted transactions per customer.
- Found the **3rd transaction** for each customer based on `transaction_id` ordering.
- Identified customers receiving **33% discounts**.
- Plotted histograms for:
  - Original purchase amounts (3rd transactions)
  - Discounted amounts (3rd transactions)

### **3. Statistics**
- Calculated average purchase amount: **54.85**
- Average discounted amount for 3rd transactions: **23.69**
- Computed probability of a random transaction being a discounted 3rd purchase.

### **4. Linear Algebra & NumPy**
- Represented amounts as NumPy arrays.
- Created a **discount vector** (0.33 for 3rd purchases, else 0).
- Performed element-wise multiplication to compute discounts.
- Calculated **total discount given** (dot product).
- Computed weighted sum for non-discounted & discounted transactions.

### **5. Calculus**
- Derived formula for `Discounted_Amount` w.r.t `Amount`.
- Interpreted: The rate of change is `1 - DiscountRate`.

### **6. Feature Engineering**
- Added:
  - `Transaction_Rank` – Purchase sequence per customer
  - `Discount_Applied` – 1 if 3rd purchase, else 0
  - `Discounted_Amount` – 33% off if discount applied
  - `Savings` – Difference between amount and discounted amount

### **7. SQL Simulation**
- Selected only transactions where discount applied.
- Queried specific columns (`customer_id`, `transaction_id`, `amount`, `Discounted_Amount`).
- Sorted results by `customer_id`.

### **8. Insights**
- **Largest Discount**: Customer **1005** – 32.34
- **Total Discount Given**: **118.47**
- **Average Saving per Customer**: **53.67**
- **Customer Spending Most After Discount**: Customer **1005**
