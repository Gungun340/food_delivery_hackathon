# 🍽️ Food Delivery Hackathon – Dataset Merging & Analysis

This project is part of a hackathon task where we are given 3 datasets in different formats (CSV, JSON, SQL) and we need to combine them into one final dataset for analysis.

The final dataset created is the **only source of truth** for answering all hackathon questions.

---

## 📌 Problem Statement

We are provided with 3 different files simulating real-world systems:

### 📂 File 1: `orders.csv` (Transactional Data)
Contains order-level details such as:
- `order_id`
- `user_id`
- `restaurant_id`
- `order_date`
- `total_amount`

### 📂 File 2: `users.json` (User Master Data)
Contains user information such as:
- `user_id`
- `name`
- `city`
- `membership` (Gold / Regular)

### 📂 File 3: `restaurants.sql` (Restaurant Master Data)
Contains restaurant information such as:
- `restaurant_id`
- `restaurant_name`
- `cuisine`
- `rating`

---

## ✅ Objective

1. Load all three datasets from different formats.
2. Perform **LEFT JOIN merges** using:
   - `orders.user_id → users.user_id`
   - `orders.restaurant_id → restaurants.restaurant_id`
3. Create a final combined dataset:
   ✅ `final_food_delivery_dataset.csv`

---

## 🔗 Join Logic (Very Important)

### ✅ Join 1: Orders + Users
- Key: `user_id`
- Join Type: **Left Join**
- Reason: We must retain **all orders**, even if a user record is missing.

### ✅ Join 2: Orders + Restaurants
- Key: `restaurant_id`
- Join Type: **Left Join**
- Reason: We must retain **all orders**, even if a restaurant record is missing.

---

## 🧾 Final Dataset Output

The generated final dataset contains:
✅ Order details  
✅ User information  
✅ Restaurant details  

📁 Output file created:
- `final_food_delivery_dataset.csv`

---

## 🛠️ Tools & Technologies Used

- Python 3.x
- Pandas
- JSON (built-in Python library)
- SQLite3 (built-in Python library)
- VS Code (Jupyter Notebook)

---

## 📦 How to Run This Project (Step-by-Step)

### ✅ Step 1: Clone the Repository
```bash
git clone https://github.com/Gungun340/food_delivery_hackathon.git
cd food_delivery_hackathon
