# :hotel: Hotel Booking Analysis :hotel:
you can find all the detailed information about this project in DataCamp Code Along section 
# :video_camera: Source : [Exploratory Data Analysis in Python for Absolute Beginners ](https://docs.google.com/presentation/d/1Ki0FjUzZs0-vttPcjlZqd60O7P-kdkQkb3OfsmmDhFo/edit?slide=id.g9d046048cf_0_8#slide=id.g9d046048cf_0_8)
- Teacher : Filip Schouwenaars
## :wrench: Tools :
- Pandas
- Plotly
## Goad of this Project : 
<img width="1042" height="628" alt="image" src="https://github.com/user-attachments/assets/316ebe9e-5a31-416d-885f-67ffc13937dc" />

# 📊 Hotel Booking Analysis – Deposit Types and Cancellation Rates

## 🔑 Key Finding
- Bookings with **“Full Deposit Made”** have an **extremely high cancellation rate of ~99%**.  
- In comparison:  
  - **No Deposit Made** → ~28% cancellation  
  - **Partial Deposit Made** → ~22% cancellation  

---

## ⚠️ Implications
1. **Revenue Risk** – Almost all customers who select “Full Deposit Made” cancel, threatening cash flow.  
2. **Operational Distortion** – Fake/temporary bookings block room inventory, reducing true availability.  
3. **Policy/Process Flaw** – Suggests either deposits are not actually charged or the option is being abused.  

---

## ❓ Possible Causes
- **System Misconfiguration** → “Full Deposit” not enforced properly at booking time.  
- **Third-Party Exploitation** → OTAs or agents mass-book then cancel.  
- **Fraudulent Behavior** → Guests gaming the policy for refunds/chargebacks.  
- **Data Quality Issue** → Mislabeling in the booking system.  

---

## ✅ Recommendations
1. **Audit deposit processing** → verify if full deposits are actually charged.  
2. **Compare booking channels** → check if OTAs drive abnormal cancellation patterns.  
3. **Temporarily suspend** “Full Deposit Made” option until fixed.  
4. **Investigate fraud patterns** → analyze customer segments, IP addresses, and booking sources.  
5. **Improve system logging** → ensure deposit status is tracked correctly.  

---

## 📈 Visualization
*(Example chart – Cancellation Rate by Deposit Type)*  
<img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/da8fdb58-98c7-40b9-ba78-2ccc3941f9f5" />

---

## 📌 Conclusion
The **“Full Deposit Made”** option is **high-risk and unreliable** under the current setup.  
It should be treated as a **priority issue** to protect both **revenue** and **inventory integrity**.


