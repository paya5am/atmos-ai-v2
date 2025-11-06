# Atmos AI: Pollution-Aware Navigation for Bengaluru

## Overview

**Atmos AI** is an innovative navigation app that doesn’t just find the *fastest* route — it finds the *cleanest* one.  
By combining real-time traffic, weather, and air quality data, our app helps users cut their pollution exposure by **over 50%**, often for just a few extra minutes of travel.

**Currently available exclusively for the city of Bengaluru, India.**

---

## Core Innovation: Graph Neural Network (GNN)

At the heart of Atmos AI lies our **Graph Neural Network (GNN)** — the key to understanding how air pollution actually flows through an urban landscape.  
A city like Bengaluru isn’t a simple grid; it’s a dynamic network of roads, vehicles, and weather patterns.

### Why a GNN?

- **Cities are complex networks** – Traditional routing models can’t capture how congestion or weather in one area impacts another.  
- **Pollution spreads dynamically** – A GNN models the physics of air movement across roads and intersections.  
- **Smarter predictions** – It learns how a traffic jam on M.G. Road, combined with a southwest wind, impacts the air quality on nearby streets like Brigade Road or Richmond Circle.

---

## Technical Deep Dive

### Data Pipeline

To power our “virtual sensor” engine, we built a robust and scalable data pipeline using **5 years of daily AQI data** from **12 KSPCB stations** across Bengaluru:

1. **Ingestion**  
   We collected **daily Air Quality Index (AQI)** data for the past 5 years from **12 official KSPCB monitoring stations** located throughout Bengaluru.

2. **Feature Matching**  
   Each daily AQI reading was precisely matched with corresponding data on:
   - **Traffic density**  
   - **Wind speed and direction**  
   - **Humidity**  
   - **Temporal and spatial metadata** (time of day, seasonality)

3. **Training**  
   We trained our **Graph Neural Network (GNN)** on this **massive spatio-temporal dataset**, enabling it to learn how pollution moves dynamically through the city's streets.

---

### Model Performance

Our trained GNN model can now:

- Take **live traffic** and **live weather** data.  
- Predict **street-level AQI** for any GPS coordinate in Bengaluru.  
- Power **pollution-aware route recommendations** in real-time.

This allows users to make healthier travel choices, significantly reducing their exposure to harmful air pollutants during daily commutes.

---

## Key Features

- **Real-time Cleanest Route Suggestions**  
  Navigate Bengaluru with the cleanest possible route — not just the fastest.

- **Dynamic Pollution Prediction**  
  Live AQI updates at street-level accuracy.

- **Switch to Fastest Route in Emergency**  
  In case of an emergency, users can **switch from the cleanest route to the fastest route** to save time.

- **Data-Driven Decision Making**  
  Combines historical, meteorological, and traffic data into a unified model.

---

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Python 3.x  
- TensorFlow or PyTorch (depending on your implementation)  
- Common Python libraries: `pandas`, `numpy`, `geopandas`, `matplotlib`

### TO RUN
  python train_model.py
   ( train the model first according to required level of sensitivity )
   ( or use the existing model in the repo )
  python main.py

### ACKNOWLEDGMENTS

  Karnataka State Pollution Control Board (KSPCB) for providing AQI data from 12 monitoring stations across Bengaluru.
  mapboxapi for the maps.
  TensorFlow / PyTorch for powering the GNN architecture.

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/atmos-ai.git

# Navigate into the folder
cd atmos-ai

# Install dependencies
pip install -r requirements.txt

#
