# 🏙️ Dynamic Pricing for Urban Parking Lots

**Capstone Project - Summer Analytics 2025**
*Consulting & Analytics Club × Pathway*

---

## 🚀 Overview

This project implements a real-time dynamic pricing engine for **14 urban parking spaces**, optimizing utilization using demand signals and competition-based pricing.

---

## 🎯 Problem Statement

Urban parking is limited. Static pricing causes:

* Overcrowding
* Underutilization

The solution: **Dynamic Pricing** driven by:

* Real-time data (traffic, queue, special days)
* Historical occupancy
* Competitor pricing

---

## 🧰 Tech Stack

| Technology       | Purpose                  |
| ---------------- | ------------------------ |
| **Python**       | Programming logic        |
| **Pandas**       | Data manipulation        |
| **NumPy**        | Numeric computation      |
| **Bokeh**        | Real-time visualizations |
| **Pathway**      | Stream processing engine |
| **Google Colab** | Development platform     |

---

## 📦 Dataset Summary

* **14** parking lots
* **73** days of records
* **18** time samples per day (8:00 AM to 4:30 PM)

**Key Features:**

* Coordinates: `Latitude`, `Longitude`
* Metrics: `Occupancy`, `QueueLength`, `Capacity`
* Context: `TrafficConditionNearby`, `IsSpecialDay`, `VehicleType`

---

## 📂 Project Structure

```text
Dynamic_Pricing_Parking/
├── dataset.csv                        # Input dataset
├── Dynamic_Pricing_Urban_Parking.ipynb # Main implementation notebook
└── README.md                          # Project summary (this file)
```

---

## 🔄 Architecture Flow

1. **Data Preprocessing:**

   * Clean features
   * Encode traffic and vehicle type
2. **Model 1: Baseline Linear Pricing**

   * Linear price increase with occupancy:
     `Price_t+1 = Price_t + α * (Occupancy / Capacity)`
3. **Model 2: Demand-Based Pricing**

   * Uses: Occupancy rate, Queue length, Traffic, Special Day, Vehicle Type
   * Demand normalized to \[0, 1]
   * Price bounded: **\$5 ≤ Price ≤ \$20**
4. **Model 3: Competitive Pricing**

   * Calculates geographic proximity via Haversine distance
   * Adjusts price based on nearby lots' prices
5. **Pathway Streaming (Simulated):**

   * Streams `dataset.csv` row-by-row
6. **Bokeh Visualization:**

   * Real-time line plots for pricing trends

---

## ✅ Key Features

* All models from scratch using only `NumPy` and `Pandas`
* Real-time simulated updates with Pathway
* Live plotting using Bokeh
* Pricing logic constraints respected (0.5x – 2x base)

---

## 🛠️ How to Run

```bash
# Step 1: Clone the repo
git clone https://github.com/codewithshek/Summer-Analytics-2025.git

# Step 2: Install dependencies
pip install pathway pandas numpy bokeh
```

1. Open `Dynamic_Pricing_Urban_Parking.ipynb` in **Google Colab**
2. Run all cells sequentially to simulate all models

---

## 📝 License

This project is for academic purposes under **Summer Analytics 2025**.

---

## 👤 Author

**D Abhishek Yadav**
Hyderabad, India
B.Tech CSE @ Vardhaman College of Engineering (VCEH)
