# 🏨 Project: Hotel Booking Analysis

### 🔗 Source: [DataCamp Code Along – Exploratory Data Analysis in Python for Absolute Beginners](https://docs.google.com/presentation/d/1Ki0FjUzZs0-vttPcjlZqd60O7P-kdkQkb3OfsmmDhFo/edit?slide=id.g9d046048cf_0_8#slide=id.g9d046048cf_0_8)
👨‍🏫 Instructor: **Filip Schouwenaars**

---

## 📌 Overview
This project explored **hotel booking data** to uncover insights into **cancellation behavior** and **deposit types**.
The focus was on understanding **why bookings get cancelled** and identifying **patterns that threaten revenue**.

---

## 🛠️ Tools & Libraries
- **Python**
- **Pandas** – data wrangling & cleaning
- **Plotly** – interactive data visualization

---

## 🎯 Goal of the Project
Analyze hotel booking data to answer:
- *“How do deposit types affect cancellation rates?”*
- *“Are current policies hurting revenue and operations?”*

---

## 📊 Key Finding: Deposit Types vs Cancellation Rates
- **Full Deposit Made** → ❌ ~99% cancellation rate
- **No Deposit Made** → ~28% cancellation
- **Partial Deposit Made** → ~22% cancellation

<img width="600" alt="Cancellation Rates by Deposit Type" src="https://github.com/user-attachments/assets/da8fdb58-98c7-40b9-ba78-2ccc3941f9f5" />

---

## ⚠️ Business Implications
1. **Revenue Risk** – Fake bookings threaten financial stability.
2. **Operational Issues** – Rooms blocked by cancellations reduce availability.
3. **Policy Gap** – Suggests **deposit enforcement failure** or exploitation.

---

## ❓ Possible Causes
- Misconfigured **system logic** for deposits
- Abuse by **third-party booking agents/OTAs**
- **Fraudulent behavior** by guests (refunds/chargebacks)
- **Data quality errors** in deposit labeling

---

## ✅ Recommendations
- **Audit & enforce deposit rules** (check if payments are actually processed).
- **Segment cancellations by booking channel** (OTAs vs direct).
- **Temporarily suspend** “Full Deposit” until verified.
- **Investigate fraud signals** (IPs, booking sources, repeat patterns).
- **Improve system logging** for deposit verification.

---

## 🚀 Key Skills Demonstrated
- Exploratory Data Analysis (**EDA**)
- Business-driven data storytelling
- Data cleaning & wrangling with Pandas
- Interactive visualization with Plotly

---

## 📌 Conclusion
This analysis revealed that the **“Full Deposit Made” option is broken** – almost all customers cancel, making it a **priority risk**.
The findings show how **data analysis directly drives business decisions** by preventing **revenue loss and fraud exposure**.

---
