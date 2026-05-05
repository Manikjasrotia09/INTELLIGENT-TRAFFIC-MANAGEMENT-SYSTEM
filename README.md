# IntelliTraffic: AI-Powered Smart Traffic Management System

## About
IntelliTraffic is an intelligent traffic monitoring system that uses image processing, machine learning, and real-time APIs to manage urban traffic effectively. It includes:
- **Automatic License Plate Recognition** for vehicle identification
- **Smart Traffic Light Control** using live traffic density
- **Real-time Traffic Monitoring** with Google Maps integration
- **ML-based Traffic Prediction** for congestion forecasting
- **E-Challan System** for traffic violations
- **Emergency Route Clearance** (Green Corridor for ambulances)

## Quick Start Guide

### Prerequisites
- **Node.js** (v14+) and npm
- **Python** (v3.7+) and pip
- **Google Maps API Key** (optional, but needed for map features)
- Git

### Installation & Setup

#### 1. Clone the Repository
```bash
git clone https://github.com/your-repo/Intelligence-traffic-monitoring-system.git
cd Intelligence-traffic-monitoring-system
```

#### 2. Frontend Setup (React)
```bash
# Install dependencies
npm install --legacy-peer-deps

# Create .env file in project root (optional, for Google Maps)
# Add this line if you have a Google Maps API key:
# REACT_APP_GOOGLE_MAPS_KEY=your_api_key_here
```

#### 3. Backend Setup (Flask)
```bash
# Navigate to backend folder
cd backend

# Install Python dependencies
pip install -r requirements.txt
```

### Running the Application

#### Start Backend (Flask API)
```bash
# From the backend directory
python app.py
```
Backend will run on: **http://localhost:5000**

#### Start Frontend (React Dev Server)
```bash
# From the project root directory (open new terminal)
npm start
```
Frontend will run on: **http://localhost:3000**

#### Access the Application
Open your browser and navigate to: **http://localhost:3000**

### Project Structure
```
├── src/                          # React frontend source
│   ├── components/
│   │   ├── LiveTraffic/         # Real-time traffic monitoring
│   │   ├── TrafficCommandCenter/# Signal control interface
│   │   ├── TrafficPrediction/   # ML predictions
│   │   ├── Fine/                # E-Challan system
│   │   ├── registerationForm/   # Vehicle registration
│   │   └── Sidebar/             # Navigation menu
│   ├── App.js
│   └── index.js
├── backend/
│   ├── app.py                   # Flask API server
│   ├── requirements.txt         # Python dependencies
│   └── traffic_data.csv         # Training data
├── public/                      # Static files
└── package.json                 # npm dependencies
```


