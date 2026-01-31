
# 🍽️ Food Delivery Data Analysis Hackathon

## 📌 Objective

The objective of this project is to integrate food delivery data originating from multiple real-world systems and file formats CSV, JSON, and SQL - into a single unified dataset. The consolidated dataset is then used to perform exploratory data analysis to derive meaningful business insights related to order trends, user behavior, membership impact, and revenue performance.

---

## 📂 Files Provided

The project uses three different data files, each representing a real-world data source:

* **orders.csv** – Transactional order data
* **users.json** – User master data
* **restaurants.sql** – Restaurant master data

---

## 📁 Repository Contents

* **Food_Delivery_Data_Integration.ipynb** – Main Jupyter Notebook containing data loading, merging, and analysis
* **final_food_delivery_dataset.csv** – Final merged dataset (single source of truth)
* **orders.csv** – Transactional data
* **users.json** – User master data
* **restaurants.sql** – Restaurant master data
* **README.md** – Project documentation

---

## 🧾 Data Description

* **orders.csv**: Contains order-level transactional details such as order ID, user ID, restaurant ID, order amount, and order date
* **users.json**: Contains user profile details including membership type (Gold / Regular)
* **restaurants.sql**: Contains restaurant metadata including restaurant name, city, cuisine type, and rating

---

## 🔄 Step-by-Step Methodology

### Step 1: Load CSV Data

Loaded transactional data from `orders.csv` using Pandas.

### Step 2: Load JSON Data

Loaded user master data from `users.json`.

### Step 3: Load SQL Data

Loaded restaurant master data from `restaurants.sql` using SQLite.

### Step 4: Merge the Data

Datasets were merged using **LEFT JOINs** to ensure no loss of transactional records:

* `orders.user_id` → `users.user_id`
* `orders.restaurant_id` → `restaurants.restaurant_id`

### Step 5: Create Final Dataset

A consolidated dataset was created containing:

* Order details
* User information
* Restaurant information

📁 **Output File:**
`final_food_delivery_dataset.csv`

---

## 📊 Analysis Performed

The final dataset was used to analyze:

* Order trends over time
* User behavior patterns
* City-wise and cuisine-wise performance
* Membership impact (Gold vs Regular users)
* Revenue distribution and seasonality

📌 **Note:**
The final dataset is treated as the **only source of truth** for answering all analytical and hackathon questions.

---

## 🛠️ Tools and Technologies Used

* **Python**
* **Pandas**
* **SQLite**
* **Matplotlib**
* **Jupyter Notebook**

---

## ▶️ How to Run the Project

1. Clone the repository
2. Open `Food_Delivery_Data_Integration.ipynb` in Jupyter Notebook or Google Colab
3. Run all cells sequentially
4. The final merged dataset will be generated as `final_food_delivery_dataset.csv`

---

## 📦 Output

* **final_food_delivery_dataset.csv**
  This file represents the consolidated dataset and serves as the **single source of truth** for all analyses and answers in this hackathon.

---

## 📝 Notes

* LEFT JOIN strategy ensures all orders are retained
* Repository is public and fully reproducible
* All results are computed directly from the final merged dataset

---

## 👤 Author

Prepared as part of the **Food Delivery Data Analysis Hackathon** submission.
