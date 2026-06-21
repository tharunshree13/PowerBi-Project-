# 📖 Data Dictionary — Zepto Sales Flat Dataset

**File:** `zepto_sales_flat_dataset.xlsx`
**Sheet:** `Zepto_Sales_Flat`
**Total Records:** 1,000
**Total Columns:** 42

---

## 🧾 Order Information

| Column | Data Type | Description | Example |
|---|---|---|---|
| `Order_ID` | Text | Unique identifier for each order | O00001 |
| `Order_Date` | Date | Date when the order was placed | 2025-01-15 |
| `Order_Time` | Time | Time when the order was placed | 21:30 |
| `Delivery_Date` | Date | Date when the order was delivered | 2025-01-15 |
| `Delivery_Time` | Time | Time when the order was delivered | 21:44 |
| `Order_Status` | Text | Final status of the order | Delivered / Cancelled |

---

## 👤 Customer Information

| Column | Data Type | Description | Example |
|---|---|---|---|
| `Customer_ID` | Text | Unique customer identifier | C0184 |
| `Customer_Name` | Text | Customer display name | Customer_48 |
| `Customer_Phone` | Text | Customer contact number | 9866857926 |
| `City` | Text | City where order was placed | Mumbai, Hyderabad, Bangalore, Delhi |
| `Area` | Text | Area/locality within city | Indiranagar, BTM, HSR, Koramangala, Whitefield |
| `Pincode` | Text | PIN code of delivery location | 560095 |

---

## 🏪 Store Information

| Column | Data Type | Description | Example |
|---|---|---|---|
| `Store_ID` | Text | Unique identifier for the dark store | S002 |
| `Store_Name` | Text | Name of the store | Store_1 |
| `Store_City` | Text | City where the fulfilling store is located | Mumbai |

---

## 🛵 Delivery Partner Information

| Column | Data Type | Description | Example |
|---|---|---|---|
| `Delivery_Partner_ID` | Text | Unique ID of the delivery rider | D027 |
| `Delivery_Partner_Name` | Text | Name/alias of the delivery partner | Rider_41 |
| `Delivery_Time_Minutes` | Number | Time taken to deliver in minutes | 14 |
| `Distance_KM` | Decimal | Distance traveled for delivery in km | 8.47 |

---

## 📦 Product Information

| Column | Data Type | Description | Example |
|---|---|---|---|
| `Product_ID` | Text | Unique product identifier | P0137 |
| `Product_Name` | Text | Name of the product | Chips, Apple, Milk, Banana |
| `Brand` | Text | Brand of the product | Amul, Nestle, ITC, Tata, Local |
| `Category` | Text | Main product category | Dairy, Snacks, Vegetables, Beverages, Fruits |
| `Sub_Category` | Text | Sub-category of the product | General |
| `SKU` | Text | Stock Keeping Unit code | SKU2278 |

---

## 💰 Pricing & Financial Information

| Column | Data Type | Description | Example |
|---|---|---|---|
| `Quantity` | Integer | Number of units ordered | 3 |
| `Unit_Price` | Decimal | Selling price per unit (after discount) | 31 |
| `MRP` | Decimal | Maximum Retail Price per unit | 46 |
| `Discount_%` | Decimal | Discount percentage applied | 15 |
| `Discount_Amount` | Decimal | Total discount value in ₹ | 13.95 |
| `Selling_Price` | Decimal | Total revenue from this order | 79.05 |
| `Cost_Price` | Decimal | Total cost to fulfill this order | 69.75 |
| `Profit` | Decimal | Profit earned from this order (₹) | 9.30 |
| `Refund_Amount` | Decimal | Refund issued in case of cancellation | 0 |

---

## 💳 Payment Information

| Column | Data Type | Description | Example |
|---|---|---|---|
| `Payment_Method` | Text | Mode of payment used | Card, UPI, COD |
| `Payment_Status` | Text | Status of payment | Paid |
| `Coupon_Code` | Text | Coupon/promo code applied | FEST50, FIRST20, SAVE10, NONE |

---

## ⭐ Customer Feedback

| Column | Data Type | Description | Example |
|---|---|---|---|
| `Rating` | Integer | Customer rating (1–5); blank for cancelled orders | 3, 4, 5 |

---

## 📅 Time Dimensions

| Column | Data Type | Description | Example |
|---|---|---|---|
| `Day_of_Week` | Text | Day of the week the order was placed | Monday, Sunday |
| `Month` | Integer | Month number (1 = January) | 1, 2, 3 |
| `Quarter` | Integer | Quarter of the year | 1 |
| `Year` | Integer | Year of the order | 2025 |

---

## 📝 Notes

- All monetary values are in **Indian Rupees (₹)**
- Orders with `Order_Status = Cancelled` have `Rating = blank` and `Refund_Amount > 0`
- The dataset covers **Q1 2025** (January, February, March) only
- `Store_City` may differ from `City` — the nearest dark store fulfills the order
- `Selling_Price` = `Unit_Price × Quantity` (after discount)
- `Profit` = `Selling_Price − Cost_Price`
