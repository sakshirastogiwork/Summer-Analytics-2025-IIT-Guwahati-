# 🚗 Dynamic Pricing for Urban Parking Lots  
**Summer Analytics 2025 — Capstone Project**  
📍 Hosted by Consulting & Analytics Club × Pathway  
👩‍💻 Built using Python, NumPy, Pandas & Pathway

---

## 🧠 Problem Statement

Urban parking lots are a limited, high-demand resource. Flat-rate pricing leads to:
- Overcrowding in high-traffic zones
- Underutilization in others

To solve this, we designed a **Dynamic Pricing System** that updates parking prices in real-time, responding to:
- Occupancy rates
- Traffic congestion
- Queue lengths
- Special events
- Vehicle type
- Competitor pricing (Model 3)

> Aimed to ensure optimal usage, smart rerouting, and price fairness across 14 parking lots over 73 days and 18 time slots/day.

---

## 🎯 Objective

📈 Create an intelligent, explainable pricing engine that:
- Starts with a base price of `$10`
- Dynamically adjusts prices in real time
- Maintains smooth and interpretable pricing behavior
- Simulates competitive responses to nearby lot pricing
- Runs on streaming data using Pathway

---

## 🧪 Dataset Overview

Sampled across **14 urban parking spaces** over **73 days**, every **30 minutes from 8 AM to 4:30 PM**.

### Features:
- 🗺️ Location: Latitude & Longitude
- 🏢 Capacity, Occupancy, Queue Length
- 🚗 Vehicle Type: Car, Bike, Truck
- 🚦 Traffic Level, Special Day Indicator
- 💰 Competitor Prices (Model 3)

---

## 🧮 Models Developed

### **Model 1: Baseline Linear Pricing**
> Simple, interpretable pricing rule:
Priceₜ₊₁ = Priceₜ + α · (Occupancy / Capacity)


### **Model 2: Demand-Based Pricing**
> Introduced weighted demand function:
Demand = α · (Occupancy / Capacity)
+ β · QueueLength
- γ · Traffic
+ δ · IsSpecialDay
+ ε · VehicleWeight


Priceₜ = BasePrice · (1 + λ · NormalizedDemand)



- Ensured price bounds: min 0.5x base, max 2x base.

### **Model 3: Competitive Pricing Logic**
> Added location intelligence + competitor price influence:
- Compared prices of nearby lots (via lat-long)
- Recommended rerouting or price boosts based on competition

---

## ⏱️ Real-Time Simulation

Built with **Pathway**, simulating:
- Streamed time-ordered records
- Real-time price updates
- Live Bokeh visualizations

### 📊 Visualizations
- Dynamic pricing curves per lot
- Occupancy vs. price over time
- Reroute recommendations

---

## 📁 Files in This Repo

| File | Description |
|------|-------------|
| `Summer_Analytics_Final_Assignment.ipynb` | Full end-to-end Colab code |
| `problem statement.pdf` | Official project brief |
| `report.pdf` _(optional)_ | Summary write-up & visual explanations |

---

## 📌 Submission Guidelines Followed
✅ Clean code with comments  
✅ Explained demand model & logic  
✅ Integrated real-time stream simulation  
✅ All visualizations included using **Bokeh**  
✅ Report included justifying assumptions

---

## 🛠️ Tools Used
- Python, NumPy, Pandas
- Pathway (real-time engine)
- Bokeh (for dynamic plotting)
- Google Colab

---

## 🚀 Final Thoughts

This project showcases how economic modeling + real-time ML can optimize city infrastructure, one parking space at a time.  
No AI hype — just good, clean logic built from scratch.

---

## 🔗 References
- [Pathway Real-Time Guide](https://pathway.com/developers/user-guide/introduction/first_realtime_app_with_pathway/)
- [Summer Analytics 2025 Course Page](https://www.caciitg.com/sa/course25/)

---

> Designed with 🧠 by a Summer Analytics 2025 participant.
