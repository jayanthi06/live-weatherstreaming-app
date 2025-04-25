# 🌦️ Real-Time Weather Streaming App using Azure Event Hub, Databricks, and Power BI

This project showcases a full-stack Azure-based streaming pipeline that ingests **live weather data**, processes it using **Azure Databricks + Functions**, stores structured data in **Kusto DB (Eventhouse)**, and visualizes insights through **Power BI** with real-time alerts via **Data Activator**.

---

## 📌 Project Goals

- Ingest live weather events using public APIs
- Clean and push data to Azure Event Hub
- Stream and transform in real-time with Event Stream + Eventhouse
- Visualize key weather trends (temperature, wind, pressure)
- Trigger real-time alerts based on anomaly thresholds

---

## 🧱 Architecture Overview

![Architecture](images/weather-architecture.png)

---

## 🔁 Components & Flow

| Step | Description |
|:--|:--|
| 🔄 **Live Weather API** | Real-time data source (temperature, humidity, wind, etc.) |
| ⚙️ **Azure Functions / Databricks** | Transforms & pushes events into Event Hub |
| 🔗 **Azure Event Hub** | Ingests weather events (JSON format) |
| 🌀 **Event Stream** | Pipes data to Eventhouse |
| 🏠 **Eventhouse (Kusto DB)** | Stores structured weather records |
| 🔍 **KQL Querysets** | Runs queries for live dashboards |
| 📊 **Power BI** | Visualizes weather patterns & KPIs |
| 🔔 **Data Activator + Outlook** | Sends alerts when thresholds are breached |

---

## 🔧 Setup Process

### 1. Data Ingestion
- Configured Azure Function to fetch API data every X minutes
- Used Azure Key Vault for credential security

### 2. Event Hub & Event Stream
- Created Event Hub namespace and eventstream
- JSON schema enforced in Event Stream

### 3. Eventhouse & Dashboards
- Connected Event Stream output to Eventhouse (Kusto DB)
- Built KQL queries and pinned to Power BI

### 4. Real-Time Alerts
- Used Data Activator to monitor conditions
- Alerts sent to email via Outlook integration

---

## 📈 Sample Visualizations
- 📉 Temperature trends over time  
- 🌬️ Wind speed vs. pressure comparisons  
- 📍 City-level anomaly detection

---

## 🚀 Results
- Handled **thousands of events per day** without data loss
- Achieved **sub-5s latency** from ingestion to visualization
- Triggered **real-time alerts** for rapid decisions

---

## 🔮 Future Enhancements
- Add ML anomaly detection using Azure ML or Synapse ML
- Integrate IoT weather stations as new data source
- Extend dashboards to mobile and Teams

