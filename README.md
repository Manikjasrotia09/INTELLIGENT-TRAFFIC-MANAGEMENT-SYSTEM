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

### Features & Pages

| Page | Description |
|------|-------------|
| **Live Traffic** 🚦 | Real-time map view with traffic lights and vehicle counts |
| **Command Center** 📊 | Congestion monitoring & signal control panel |
| **Accident Map** 📍 | Heatmap visualization of high-risk areas |
| **Green Corridor** 🚑 | Emergency route clearance for ambulances |
| **Statistics** 📈 | Traffic data visualization & trends |
| **Predictions** 🤖 | ML-based traffic density forecasting |
| **Fine Management** 🚔 | E-Challan system for violations |
| **Registration** 📋 | Vehicle license registration |

### Backend API Endpoints

```
GET  /api/health             - Health check
POST /api/predict            - Get traffic predictions
```

**Example Prediction Request:**
```bash
curl -X POST http://localhost:5000/api/predict \
  -H "Content-Type: application/json" \
  -d '{
    "weather": "Sunny",
    "road_condition": "Dry",
    "hour": 14,
    "day_of_week": 2
  }'
```

### Google Maps Setup (Optional)
To enable map features:

1. Get an API key from [Google Cloud Console](https://console.cloud.google.com/apis/library/maps-backend.googleapis.com)
2. Enable these APIs:
   - Maps JavaScript API
   - Directions API
3. Create a `.env` file in the project root:
   ```
   REACT_APP_GOOGLE_MAPS_KEY=your_actual_api_key_here
   ```
4. Restart the dev server: `npm start`

### Advanced Features

#### License Plate Detection
```bash
cd vehicle_number_by_its_plate
python3 licenseplateDetection.py sample_image.jpg
```

#### Vehicle Counting with OpenCV
```bash
cd countingCars
python count.py
```

#### Traffic Prediction Model
The backend includes a trained Random Forest model for traffic prediction:
```bash
cd trafficPrediction
python mlprediction.py
```

### Technologies Used
- **Frontend:** React 18, Ant Design 5, React Router 6, Google Maps API
- **Backend:** Flask, scikit-learn, pandas, numpy
- **Database:** CSV-based traffic data
- **APIs:** Google Maps, Google Directions

### System Requirements
- **Disk Space:** ~500 MB
- **RAM:** 2 GB minimum (4 GB recommended)
- **Browser:** Modern browser (Chrome, Firefox, Safari, Edge)

### Troubleshooting

**Port Already in Use:**
```bash
# If port 3000 is busy, use alternate port
$env:PORT=3001; npm start  # Windows PowerShell
PORT=3001 npm start         # macOS/Linux
```

**Dependencies Installation Error:**
```bash
# Use legacy peer deps flag
npm install --legacy-peer-deps
```

**Google Maps Not Loading:**
- Create `.env` file with valid `REACT_APP_GOOGLE_MAPS_KEY`
- Verify API key has Maps JavaScript API enabled
- Restart development server

### Contributing
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Support
For issues or questions, please create an issue on GitHub or contact the development team.

---

**Happy Traffic Managing! 🚗🚗🚗**
