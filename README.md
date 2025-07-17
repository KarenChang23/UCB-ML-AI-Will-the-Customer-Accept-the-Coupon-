# 🚗 Coupon Acceptance Analysis

## 📌 Project Overview

This project explores the question: **Will a customer accept a driving coupon?**

Using a dataset from the UCI Machine Learning Repository (collected via Amazon Mechanical Turk), we analyze different driving scenarios (destination, time, weather, passenger, etc.) to understand the key factors influencing whether a driver accepts a digital coupon for various services (e.g., coffee, restaurants, bars).

This assignment is part of the UC Berkeley Machine Learning Certificate Program.

---

## 🎯 Objective

To apply **exploratory data analysis**, **visualization**, and **statistical summarization** using Python in order to distinguish between customers who accepted or rejected coupons.

Accepted responses include:
- "Right away"
- "Later, before the coupon expires"

These are coded as `Y = 1`. Rejections are coded as `Y = 0`.

---

## 📁 Dataset Summary

The dataset includes:
- **User attributes** (age, gender, education, income, occupation)
- **Driving context** (passenger type, destination, weather, time)
- **Coupon details** (type, expiration)

Coupon types analyzed:
- 🍽️ Restaurants (under \$20 and \$20–\$50)
- ☕ Coffee House
- 🍱 Carryout & Takeaway
- 🍸 Bar

---

## 🧪 Analysis Performed

### ✅ General Steps:
- Loaded and cleaned the dataset
- Visualized coupon distributions and temperature ranges
- Calculated overall acceptance rate
- Focused on **Bar coupons** for in-depth segmentation:
  - Compared users based on bar visit frequency, age, passenger type, and marital status
  - Found **consistently low acceptance (~23%)** regardless of user segmentation

### ✅ Independent Investigation:
We selected **inexpensive restaurant coupons** (`Restaurant(<20)`) and tested the following hypothesis:

> **Young (under 35), solo drivers earning < \$50,000 are more likely to accept inexpensive restaurant coupons.**

Results:
- 📈 This group had **100% acceptance rate** (3/3 cases)
- Other users had ~68% acceptance
- Indicates potential marketing value in targeting this segment

---

## 🖥️ Technologies Used

- Python 3
- pandas
- matplotlib
- seaborn
- Jupyter Notebook

---

## 📌 Key Takeaway

**Targeting solo, young, low-income drivers with inexpensive food coupons may yield higher conversion rates.**  
Bar coupon acceptance was low regardless of segmentation, suggesting different strategies may be needed for bars.

---

## 📂 Repository Structure
├── prompt.ipynb # Jupyter notebook with full analysis

├── coupons.csv # Dataset (UCI ML Repository)

├── restaurant_coupon_acceptance_rate.png # Bar chart of acceptance rate (independent investigation)

└── README.md # This file
