# 🏨 Hotel Booking Cancellation Analysis

## Project Overview
An end-to-end data analysis project examining 119,390 hotel bookings across two hotels in Portugal (Resort Hotel in Algarve and City Hotel in Lisbon) to identify cancellation patterns, revenue loss drivers, and guest loyalty insights.

## Dataset
- **Source:** Antonio, N., Almeida, A., & Nunes, L. (2019). Hotel Booking Demand Datasets. *Data in Brief*, Volume 22. https://doi.org/10.1016/j.dib.2018.11.126
- **Available on Kaggle:** https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand
- **Size:** 119,390 bookings | 32 variables | July 2015 – August 2017
- **Hotels:** H1 = Resort Hotel (Algarve) | H2 = City Hotel (Lisbon)

## Tools Used
| Tool | Purpose |
|---|---|
| Python (Pandas, Matplotlib, Seaborn) | Data cleaning, EDA, visualizations |
| Kaggle Notebook | Development environment |
| Power BI Desktop | Interactive dashboard |
| DAX | KPI measures and calculated columns |

## Project Structure
```
hotel-booking-cancellation-analysis/
│
├── eda-hotelbooking.ipynb        # Python EDA notebook (Kaggle)
├── hotel_bookings_cleaned.csv    # Cleaned dataset exported to Power BI
├── Hotel_Booking_Dashboard.pbix  # Power BI dashboard file
└── README.md
```

## Key Findings

### 1. Overall Cancellation Rate
- **37.04%** of all bookings were canceled — 1 in 3 bookings never resulted in a stay
- City Hotel accounts for **74.85%** of all cancellations despite having 2x more bookings than Resort Hotel

### 2. Deposit Type vs Cancellation
| Deposit Type | Total Bookings | Cancellations | Cancellation Rate |
|---|---|---|---|
| No Deposit | 104,641 | 29,694 | 28.4% |
| Non Refund | 14,587 | 14,494 | 99.4% |
| Refundable | 162 | 36 | 22.2% |

> No Deposit bookings drive the highest cancellation volume (29,694). Non Refund's near-100% rate is a system recording artifact — hotel collects full payment before cancellation occurs, resulting in no actual revenue loss.

### 3. Revenue Analysis
| Hotel | Revenue Ratio |
|---|---|
| Resort Hotel | **2.46** |
| City Hotel | **2.15** |

- Peak revenue and peak losses both occur in **July–August** (summer season)
- Resort Hotel earns **$2.46** for every $1 lost vs City Hotel's $2.15

### 4. Guest Loyalty
- Total repeated guests: **3,810** (City Hotel: 2,032 | Resort Hotel: 1,778)
- Repeated guests who completed their stay: **3,258 (85.5% loyalty rate)**
- Resort Hotel retains more loyal guests (**1,667**) than City Hotel (**1,591**) despite fewer total bookings

### 5. Customer Type
- **Transient customers** account for the highest cancellation volume
- **Group bookings** are the most reliable — lowest cancellation rate regardless of deposit type

## Dashboard Pages

### Page 1 — Overview
- KPI Cards: Total Bookings, Cancellations, Cancellation Rate, Avg ADR, Third Party Bookings, Total Checkouts, Repeated Guests, Loyal Guests Stayed
- Cancellation by Hotel Type (Clustered Bar)
- Cancellation by Deposit Type (Bar)
- Repeated Guests per Hotel (Bar)
- Checkout Guests per Hotel (Bar)
- Date slicers: Check-in and Check-out date range filters

### Page 2 — Revenue Analysis
- Total Revenue vs Revenue Lost by Month (Line & Stacked Column Chart)
- Revenue Ratio by Hotel (KPI Cards)
- Seasonal revenue patterns identified

### Page 3 — Customer & Geographic Analysis
- Top 10 Countries by Bookings (Map)
- Customer Type Breakdown (Donut Chart)

## Recommendations
1. **Introduce deposit requirements** for bookings with lead time > 180 days to reduce No Deposit cancellation risk
2. **Target loyalty programs** at City Hotel — Resort Hotel already retains guests better
3. **Focus marketing in July–August** peak season — highest revenue AND highest loss months
4. **Prioritize Transient customer retention** — they represent the highest cancellation volume
5. **Offer early bird discounts** for bookings 90+ days in advance with deposit to incentivize commitment

## How to Run

### Python EDA
1. Open [Kaggle Notebook](https://www.kaggle.com)
2. Add Hotel Booking Demand dataset as input
3. Run `eda-hotelbooking.ipynb` step by step

### Power BI Dashboard
1. Download `hotel_bookings_cleaned.csv`
2. Open `Hotel_Booking_Dashboard.pbix` in Power BI Desktop
3. Use Check-in / Check-out date slicers to filter data

## Citation
```
António, N., Almeida, A., & Nunes, L. (2019). 
Hotel booking demand datasets. 
Data in Brief, 22, 41–49. 
https://doi.org/10.1016/j.dib.2018.11.126
```

---
*Project by Ruchitha Kota | Data Analyst Portfolio*
