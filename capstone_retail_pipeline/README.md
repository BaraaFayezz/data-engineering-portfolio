# 🧹 Data Cleaning and Feature Engineering Project

## 📘 Overview
This project demonstrates how to clean, preprocess, and enrich raw order data using **Python**, **NumPy**, and **Pandas**.  
The main goal is to transform an unclean dataset (`Orders_with_issues.csv`) into a reliable, analysis-ready file while generating summary insights.

---

## 🧠 Objectives
- Clean and standardize inconsistent or missing data.
- Convert data types and handle invalid values.
- Perform feature engineering to derive new insights.
- Generate summarized reports and export the final cleaned dataset.

---

## ⚙️ Technologies Used
- **Python 3.10+**
- **NumPy**
- **Pandas**

---

## 📂 Project Files
| File Name | Description |
|------------|-------------|
| `Orders_with_issues.csv` | Raw input dataset containing issues and missing data |
| `data_cleaning.ipynb` | Jupyter Notebook with the cleaning and transformation steps |
| `data_cleaning.py` | Python script performing the same operations programmatically |
| `cleaned_orders_final.csv` | Final cleaned dataset ready for analysis |

---

## 🧩 Data Cleaning Workflow

1. **Data Type Conversion**
   - Converted `OrderDate` and `ShippedDate` to datetime format.
   - Converted `ShippingCost` to numeric and replaced invalid (negative) entries.

2. **Handling Missing Values**
   - Replaced missing `ShippingCost` with the column median.
   - Forward-filled missing `OrderID` values.
   - Replaced missing `CustomerID` and `ShipCity` with descriptive placeholders.
   - Removed rows missing both `OrderDate` and `ShippedDate`.

3. **Text Standardization**
   - Trimmed spaces and standardized capitalization for all location and company columns.
   - Unified inconsistent company names (e.g., “Kiwilytics”).

4. **Feature Engineering**
   - Created `DeliveryDays` as the difference between order and shipment dates.
   - Classified orders into `DeliveryStatus` → **OnTime**, **Late**, or **Unknown**.
   - Added `IsDomestic` based on the shipping country.
   - Added `AffiliationStatus` → **Affiliated** vs **External** shipping companies.

5. **Reporting & Summary**
   - Generated reports for:
     - Delivery status distribution
     - Orders by country and city
     - Top shipping companies
     - Affiliation breakdown

---

## 🧾 Example Insights
- Majority of orders are **OnTime**, with a small share being **Late**.
- Shipping costs vary across different companies and destinations.
- **Affiliated** companies tend to have more consistent delivery times.

---

## 🧱 Setup & Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/data-engineering-portfolio.git
   
2. **Navigate to the project folder**
   ```bash
   cd data-cleaning-project

3. **Install dependencies**
   ```bash
   pip install pandas numpy

---

## ▶️ How to Run
```bash
jupyter notebook data_cleaning.ipynb
```
When you run the project:
  - It cleans and processes the dataset.
  - Creates new analytical columns.
  - Prints summaries and statistics.
  - Exports the final cleaned CSV file (cleaned_orders_final.csv).

## 📊 Output

- **Generated File**: cleaned_orders_final.csv
     A fully cleaned and structured dataset ready for analytics and reporting.

- **Reports Produced**:
  - Delivery status breakdown (OnTime / Late / Unknown)
  - Orders distribution by country and city
  - Top 3 shipping companies by count
  - Shipping company affiliation analysis




