# Urban Parking Dynamic Pricing - Summer Analytics 2025 Capstone Project

## Project Overview

This project implements a dynamic pricing system for urban parking spaces using time-series and geo-spatial data. We developed three pricing models:
1. **Model 1**: Baseline static pricing based on occupancy ratio.
2. **Model 2**: Demand-based dynamic pricing.
3. **Model 3**: Demand + Geo-spatial neighbor-aware pricing.

The goal is to optimize parking prices in real time based on demand patterns and nearby lot availability.

---

## Tech Stack

- Python 3.11
- Pandas, NumPy, Matplotlib
- Pathway (for real-time stream processing)
- Geopy (for spatial distance)
- Jupyter Notebook
- Git, GitHub

---

## 🧠 Architecture Diagram

```mermaid
flowchart TD
    A[parking_stream.csv] -->|Static Stream| B(Pathway Ingestion)
    B --> C{Model 1<br>Baseline}
    B --> D{Model 2<br>Demand-Based}
    B --> E{Model 3<br>Geo + Demand}
    C --> F[model1_output.csv]
    D --> G[model2_output.csv]
    E --> H[model3_output.csv]
    F & G & H --> I[Comparison Script]
    I --> J[model_comparison_plot.png]
