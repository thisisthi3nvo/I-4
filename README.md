# I-4

# Foot Health Monitoring System

## Overview
A real-time IoT system that monitors foot health through smart shoe sensors, predicting injury risks using machine learning and providing preventive recommendations via MQTT communication.

## 🛠 Key Features
- **Multi-sensor Data Collection**: Tracks temperature, pressure, steps, and pace
- **Real-Time Alerts**: Color-coded health status (Green/Yellow/Red)
- **Predictive Analytics**: ML-powered injury risk forecasting

### System Architecture

### Data Flow
1. **Data Generation**  
   `Sensors → CSV File → MQTT Publish (foot/sensors)`

2. **Processing Pipeline**  
   `MQTT Subscriber → Data Validation → Health Assessment → Risk Prediction`

3. **Output Actions**
A[Health Status] --> B{Decision}
B -->|Green| C[Store Only]
B -->|Yellow| D[Send Warning]
B -->|Red| E[Emergency Alert]

### Pseudocode Implementation
