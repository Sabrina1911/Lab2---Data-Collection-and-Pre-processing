# Lab 2 — Data Collection and Pre-Processing  
**Course:**    PROG8245 — Machine Learning Programming  
**Author:**    Sabrina Ronnie George Karippatt
**Student ID** 8991911
**Date:**      29-09-2025 

---

## 📌 Project Synopsis
This lab implements a **12-step Data Engineering roadmap** on a realistic e-commerce dataset.  
The workflow demonstrates how raw CSV data is ingested, cleaned, transformed, and enriched to prepare for downstream machine learning tasks. Functions and modular design were used to keep the code reusable, readable, and reproducible. Final cleaned data is serialized in  
both JSON and CSV formats.

---

## ⚙️ Quick Start
Clone the repo and set up the environment:

```bash
# 1. Create a virtual environment
python -m venv .venv
# On Windows
.venv\Scripts\activate
# 2. Install dependencies
pip install -r requirements.txt
# 3. Launch Jupyter Notebook
jupyter notebook
```

Run `Lab2.ipynb` top-to-bottom.

---

## 📂 Data Sources

1. **Primary Dataset (Transactions)**

   * [1000 Sales Records — ExcelBIAnalytics](https://excelbianalytics.com/wp/downloads-18-sample-csv-files-data-sets-for-testing-sales/)
   * First 500 rows were used.

2. **Secondary Metadata**

   * Derived fields included in the lab:

     * `shipping_city` mapped from `Country` (using capitals).
     * `coupon_code` and `discount_pct` generated synthetically.

---

## ✅ Key Features

* Loaded raw CSV into pandas and displayed first rows.
* Justified choice of **list of dictionaries** for data representation.
* Implemented functions to populate data structures.
* Applied cleaning rules (strip whitespace, fix unknown cities, date parsing).
* Transformations: parsed coupon codes into numeric discounts.
* Feature engineering: added `customer_id`, `days_since_purchase`.
* Mini-aggregation: revenue per `shipping_city`.
* Serialization: saved outputs to **CSV + JSON**.