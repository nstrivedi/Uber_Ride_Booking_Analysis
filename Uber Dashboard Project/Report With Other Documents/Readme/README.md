# 🚖 Uber Ride-Hailing Operations Dashboard | Power BI

> An interactive Power BI dashboard analyzing 150,000 Uber ride bookings across vehicle types, revenue, payment methods, cancellations, and pickup/drop demand — built to support fleet allocation, cancellation-reduction, and payment-channel decisions.

---

## 📌 Project Overview

This project is a complete Business Intelligence solution developed in **Power BI** to analyze Uber ride-booking data. The dashboard helps operations, finance, and city-ops stakeholders monitor booking performance, diagnose the booking funnel, understand payment and geographic demand patterns, and compare vehicle categories using interactive filters and KPIs.

The report is organized into **6 dedicated pages** and lets users dynamically explore data by **vehicle type, quarter/month, and drop location**, with auto-generated narrative insights on the landing page for fast executive consumption.

---

## 🎯 Business Objectives

- Monitor overall booking volume and revenue performance
- Diagnose the booking funnel — completed vs. incomplete vs. cancelled — and quantify lost demand
- Compare performance across vehicle categories
- Identify high-demand pickup and drop locations to guide driver allocation
- Understand payment-channel preference to prioritize reliability investment
- Monitor driver and customer satisfaction via ratings
- Provide auto-generated, decision-ready insights rather than raw charts alone

---

# 📊 Dashboard Pages

| Page | What it shows |
|---|---|
| **Overview** | 9 dynamic, auto-generated insight tiles — top vehicle, booking success rate, lost bookings, cancellation ratio, top pickup, top payment method, peak revenue month, rating gap, digital-vs-cash split |
| **Services** | Vehicle-type explorer with image-based slicer and quarter filter — Total Bookings, Completed Rides, Total Distance, Average Distance |
| **Bookings** | Booking volume & value trends by month/quarter, booking share by vehicle type, funnel of booking value by vehicle |
| **Revenue** | Funnel health — Completed / Incomplete / Cancelled rate gauges, revenue by vehicle type, bookings by quarter |
| **Top Pickup & Drops** | Ranked pickup/drop location tables, average driver & customer rating gauges, rating-gap gauge |
| **Payments** | Payment-method mix (count of bookings by method), booking share by vehicle type |

---

### Executive KPIs

- Total Bookings
- Completed Bookings / Booking Success Rate
- Lost Bookings (Cancelled + No Driver Found)
- Cancellation Rate & Incomplete Rate
- Total Revenue
- Average Trip Distance

### Interactive Filters

Users can filter the report by:

- Vehicle Type (image-based slicer)
- Quarter / Month
- Drop Location

### Visualizations

The dashboard includes:

- 📈 Completed Bookings trend (monthly/quarterly)
- 📊 Booking Value by Month & Quarter
- 🚗 Total Bookings by Vehicle Type (donut)
- 🥧 Revenue by Vehicle Type (funnel/bar)
- 💳 Payment Method Used by Customers (bar chart)
- 📍 Top Pickup & Drop Location tables
- ⭐ Driver & Customer Rating gauges
- 🎯 Booking Success / Cancellation / Incomplete rate gauges
- KPI Cards & dynamic narrative insight tiles

---

# 📈 Key Metrics (from the current dataset)

- **Total Bookings:** 1,50,000
- **Completed Bookings:** 92,551 (61.7% success rate)
- **Lost Bookings:** 56,817 (37.9%) — cancelled or no driver found
- **Cancellation Rate:** 25.0% (driver-initiated cancellations run 2.6× customer-initiated)
- **Incomplete Rate:** 13.0%
- **Total Revenue:** ₹51.85M
- **Average Driver Rating / Customer Rating:** 4.18 / 4.39 (0.21 gap)

---

# 🚘 Vehicle Categories Analyzed

- Auto
- Bike
- Go Mini
- Go Sedan
- Premier Sedan
- Uber XL

---

# 💳 Payment Analysis

The dashboard analyzes customer payment preference across:

- UPI
- Cash
- Uber Wallet
- Credit Card
- Debit Card

**Findings:** UPI is the most preferred method (41,834 uses, ~45% of completed transactions), followed by Cash (~25%). Digital payment methods (UPI, Wallet, Credit, Debit) together account for **75.1%** of completed transactions vs. **24.9%** cash.

---

# 📅 Trend Analysis

The report includes trend analysis for:

- Monthly/quarterly completed bookings and booking value
- Vehicle-type usage and revenue share
- Booking success/cancellation/incomplete rates over time

**Finding:** Completed bookings dip every February and recover by March across every vehicle type — a consistent seasonal pattern. March is the peak revenue month at ₹4.57M.

---

# 💡 Business Insights

- **Auto is the top-performing vehicle category** — 37,419 bookings (24.9% of demand) and ₹12.88M revenue, more than any other category
- **UPI is the most preferred payment method**, with a clear shift toward digital payments (75.1%) over cash
- **Khandsa is the top pickup location** (949 rides), though demand is broadly dispersed across 176+ locations rather than concentrated in one hotspot
- **37.9% of all demand is lost** to cancellations or no-driver-found — the single biggest lever for revenue recovery
- **Driver cancellations occur 2.6× more often than customer cancellations**, pointing to a supply-side (driver availability) issue rather than a demand-side one
- **Customers consistently rate trips ~0.21 points higher than drivers** (4.39 vs. 4.18), a pattern stable across all vehicle types

---

# 🛠️ Tech Stack

- Microsoft Power BI (Desktop & Service)
- Power Query
- DAX (calculated measures, dynamic narrative-insight text)
- Data Modeling (star-schema style with dedicated measures table)
- Interactive Visualizations

---

# 📂 Dataset

The dashboard is built using an Uber ride-booking log containing:

- Booking ID
- Date
- Vehicle Type
- Booking Status (Completed / Cancelled by Driver / Cancelled by Customer / No Driver Found / Incomplete)
- Pickup Location / Drop Location
- Booking Value
- Ride Distance
- Payment Method
- Driver Rating / Customer Rating
- Cancellation & Incomplete-ride reason fields

## Data Model

| Table | Role |
|---|---|
| `Uber` | Central fact table — one row per booking |
| `Calendar` | Date dimension for Month/Quarter time intelligence |
| `Date_Axis` | Secondary continuous date axis |
| `Image` | Vehicle icon lookup for image-based slicers |
| `Necessary_Measures` | Houses all DAX measures, including the Overview page's dynamic insight text |

---

# 📷 Dashboard Preview

![alt text](<Screenshot 2026-09-09 113816.png>)


![alt text](<Screenshot 2026-09-09 113851.png>)


![alt text](<Screenshot 2026-09-09 113922.png>)


![alt text](<Screenshot 2026-09-09 114015.png>)


![alt text](<Screenshot 2026-09-09 114052.png>)


![alt text](<Screenshot 2026-09-09 114140.png>)


![alt text](<Screenshot 2026-09-09 114211.png>)


![alt text](<Screenshot 2026-09-09 114329.png>)


---

# 📁 Project Structure

```
Uber-Dashboard/
│
├── Uber_Dashboard.pbix
├── README.md
├── uber.xlsx
└── assets/
    └── screenshots/
        ├── Overview.png
        ├── Services.png
        ├── Bookings.png
        ├── Revenue.png
        ├── TopPickupDrops.png
        └── Payments.png
```

---

# 🚀 How to Use

1. Clone or download this repository.
2. Open the `.pbix` file using **Power BI Desktop**.
3. Refresh the dataset from `uber.xlsx` if required.
4. Explore the dashboard using the vehicle-type slicer, quarter/month filters, and drop-location slicer.

---

# ✅ Data Quality & QA Notes

This dashboard went through a structured measure-consistency review across all 6 pages (cross-checking every KPI, chart, and narrative insight against the same figure on other pages). Of the issues identified:

- ✔️ Fixed: broken narrative-text concatenation on the Overview page
- ✔️ Fixed: a mis-scoped "Lost Bookings" measure that was returning a single-vehicle total instead of the fleet-wide figure
- ✔️ Fixed: a "Total Bookings" mismatch between the KPI card and the vehicle-type breakdown chart
- ✔️ Fixed: funnel gauges (Completed/Incomplete/Cancelled) now sum to exactly 100%
- ✔️ Fixed: the Digital-vs-Cash payment split now reconciles exactly with the underlying payment-method chart

---

# 📊 Skills Demonstrated

- Business Intelligence
- Data Cleaning
- Data Modeling
- Power Query
- DAX Calculations (including dynamic, text-generating measures)
- KPI Design
- Dashboard Design
- Data Visualization
- Business Analytics
- Cross-page Measure Consistency & QA
- Interactive Reporting

---

# ⭐ Business Value

This dashboard enables the business to:

- Identify where fleet investment and driver incentives will have the most impact (Auto)
- Quantify and prioritize cancellation reduction as the top lever for revenue recovery
- Understand payment-channel adoption to guide reliability and integration investment
- Monitor driver and customer satisfaction trends side by side
- Support data-driven fleet allocation and operational decision-making

---

# 📬 Connect With Me

**Nishant Trivedi**

- LinkedIn: https://www.linkedin.com/in/nstrivedi
- GitHub: https://www.github.com/nstrivedi

> Replace the details above with your own before publishing.

---

## ⭐ If you found this project useful, don't forget to Star this repository!
