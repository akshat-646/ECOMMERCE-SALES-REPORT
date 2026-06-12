
# 📊 Sales Report — Power BI Dashboard

A Power BI sales analytics dashboard built on 2018 order data from across India. The report enables exploration of revenue, profit, quantity sold, and customer behaviour across states, product categories, and payment modes.

---

## 📁 Project Structure

```
├── SALES_REPORT.pbix       # Power BI report file
├── Orders.csv              # Order-level data (500 records)
├── Details.csv             # Line-item details (1,500 records)
└── README.md               # This file
```

---

## 🗂️ Data Sources

### `Orders.csv`
Contains one row per order — 500 orders spanning the full calendar year 2018.

| Column | Description |
|---|---|
| Order ID | Unique order identifier (e.g. `B-26055`) |
| Order Date | Date of order in `DD-MM-YYYY` format |
| CustomerName | Name of the customer |
| State | Indian state where the order was placed |
| City | City of the customer |

### `Details.csv`
Contains line-item level data — 1,500 records (multiple items per order).

| Column | Description |
|---|---|
| Order ID | Foreign key linking to `Orders.csv` |
| Amount | Sale amount (₹4 – ₹5,729) |
| Profit | Profit earned (can be negative, range: −₹1,981 to ₹1,864) |
| Quantity | Units sold |
| Category | Product category: Electronics, Furniture, or Clothing |
| Sub-Category | One of 17 sub-categories (e.g. Phones, Chairs, Saree) |
| PaymentMode | COD, EMI, Credit Card, UPI, or Debit Card |

**Relationship:** `Orders.Order ID` → `Details.Order ID` (one-to-many)

---

## 📈 What the Report Covers

- **Revenue & Profit Overview** — total sales and profitability at a glance
- **Monthly Trends** — order and revenue patterns across 2018
- **Geographic Analysis** — performance across 19 Indian states
- **Category Breakdown** — Electronics, Furniture, and Clothing performance
- **Sub-Category Deep Dive** — granular product-level insights
- **Payment Mode Analysis** — split between COD, UPI, EMI, Card payments
- **Customer Insights** — top customers by revenue contribution

---

## 🚀 Getting Started

1. Clone or download this repository.
2. Open `SALES_REPORT.pbix` in **Power BI Desktop** (version 2.x or later recommended).
3. If prompted to refresh data, ensure `Orders.csv` and `Details.csv` are in the same directory as the `.pbix` file, then click **Refresh**.
4. Explore the report using slicers for date, state, and category filters.

---

## 🌏 Geographic Coverage

19 states across India are represented, including Uttar Pradesh, Delhi, Maharashtra, Madhya Pradesh, Gujarat, Rajasthan, Tamil Nadu, West Bengal, Kerala, Karnataka, and more.

---
## Reprot
<img width="1328" height="746" alt="image" src="https://github.com/user-attachments/assets/d59194f8-9ed0-44a9-91aa-697f1ea84919" />

## ⚠️ Notes

- All monetary values are in **Indian Rupees (₹)**.
- Data covers **January 1, 2018 – December 31, 2018** only.
- Some orders show **negative profit**, indicating discounted or loss-making transactions.
- The `.pbix` file requires **Power BI Desktop** to open; it cannot be viewed in a standard browser without publishing to Power BI Service.
