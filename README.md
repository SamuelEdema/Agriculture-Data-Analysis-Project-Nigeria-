# Agriculture-Data-Analysis-Project-Nigeria

## Project Overview

This project presents an end-to-end data analytics workflow designed to clean, transform, and visualize an agricultural dataset containing information on farmers across multiple states in Nigeria. The ultimate goal is to provide deep stakeholder insights into total revenue, gender distribution, regional farm productivity, loan sizes, and fertilizer adoption.

The workflow is split into two major phases:

1. **Data Cleaning & Transformation:** Handled programmatically using **Python (Pandas)** inside a Jupyter Notebook.
2. **Data Visualization & Business Intelligence:** Handled dynamically via **Power BI Desktop**, producing an executive-facing PDF report / dashboard.


## Key Metrics & Dashboard Insights

From the final analysis of **500 Total Records**, the project uncovered the following high-level KPIs:

* **Total Revenue Generated:** ₦1.96 Billion
* **Total Tracked Farmers:** 491 (after removing anomalies)
* **Gender Distribution:** 54.44% Male (245) vs 45.56% Female (205)
* **Fertilizer Adoption:** 217 Fertilizer Users vs 170 Non-Users
* **Top Revenue-Generating State:** **Kano State** leads with over ₦337 Million in revenue.
* **Top Performing Crop:** **Maize** yielded the highest market revenue at ₦0.46 Billion, followed closely by **Rice** (₦0.45B).


## Phase 1: Data Cleaning & Transformation (Python)

### Data Challenges Addressed

The raw `Agriculture.csv` dataset contained significant structural inconsistency and noise:

* **Inconsistent Categorical Values:** The `Gender` column mixed entries like `'female'`, `'Female'`, `'male'`, `'Male'`, `'M'`, and `'F'`.
* **Inconsistent State Names:** State records contained variations like `'KANO'`, `'lagos'`, and `'Lagos'`.
* **String Placeholders for Missing Data:** The `FarmSize_Ha` and `Age` columns used string texts like `'unknown'` or `'N/A'` alongside numbers, forcing Pandas to interpret them as text objects.
* **Whitespace & Formatting Issues:** Trailing spaces in crop categories (e.g., `'maize '`, `' Rice'`).

### Cleaning Implementation Code

The cleaning script standardized column names, corrected categorical text, handled null values appropriately, and enforced proper numerical data types before exporting `Agriculture_cleaned.csv`:

## Phase 2: Visualizations & Analytics (Power BI)

Once the clean `.csv` file was generated, it was loaded into Power BI to construct explicit dashboard layouts. The visualizations break down into four key components:

### 1. Financial Performance & Revenue Concentration

* **Total Revenue by State (Bar Chart):** Compares financial output across regions. **Kano** (₦337M), **Enugu** (₦206M), and **Lagos** (₦202M) represent the top three economic regions.
* **Total Revenue by Crop (Bar Chart):** Ranks the financial contribution of each crop. **Maize** (₦0.46bn) and **Rice** (₦0.45bn) outperform traditional cash crops like **Yam** (₦0.35bn) and **Sorghum** (₦0.32bn).

### 2. Demographics & Resource Ingestion

* **Farmers by Gender (Pie Chart):** Outlines resource access and participation by gender. Shows a closely balanced distribution of male-to-female farmers.
* **Total Farmers by Fertilizer Use (Column Chart):** Measures input usage. It shows that a majority of tracked farmers (217) utilize fertilizers to support crop yields.

### 3. Regional Agricultural Metrics

* **Yield-Tons by State (Column Chart):** Details structural agricultural output. **Kano** is the clear leader with **1,833 Tons** produced, followed by **Lagos** (1,577 Tons) and **Enugu** (1,270 Tons).
* **Loan Amount (A.L. Amount) by State:** Compares financial support distribution, highlighting states like **Oyo** (₦2.66M) and **Kano** (₦2.58M) receiving maximum financial leverage.


## Project Structure

```bash
├── Agriculture.csv               # Raw, messy dataset from fields
├── Agriculture (1) (1).ipynb     # Jupyter Notebook with Pandas cleaning script
├── Agriculture_cleaned.csv       # Standardized, type-enforced clean dataset
├── Agriculture PDF.pdf           # Power BI Dashboard Export document
└── README.md                     # Technical project summary report


## Technologies Used

* **Python 3.x**
* **Pandas** for programmatic data scrubbing and normalization


* **Power BI Desktop**
* Data modeling and custom canvas building
* Dashboard visualizations for reporting
