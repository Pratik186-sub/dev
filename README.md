# Smart Patient Monitoring System

A web-based smart monitoring system prototype for detecting abnormal patient activity, unsafe posture, or prolonged immobility in home-care environments. Built with React.js for the hackathon.

## 🏥 Project Overview

This system provides real-time patient monitoring with advanced alert capabilities, fall detection, posture monitoring, and immobility tracking. Perfect for home-care environments and healthcare facilities.

## ✨ Features

- **Real-time Patient Monitoring**: Live simulation of patient vitals and activities
- **Fall Detection System**: Automatic detection of falls with emergency alerts
- **Posture Monitoring**: Tracks patient posture and alerts for unsafe positions
- **Immobility Detection**: Alerts when patient is immobile for prolonged periods (>5 minutes)
- **Vital Signs Tracking**: Heart rate, blood pressure, oxygen level, and temperature
- **Activity Monitoring**: Real-time activity level and movement detection
- **Automatic Alert System**: Multi-level alerts (Info, Warning, Emergency)
- **Push Notifications**: Browser notifications for critical alerts
- **Activity Trend Analytics**: Charts and visualizations of patient data
- **Alert History Dashboard**: Complete alert log with filtering and search
- **Data Export**: Export monitoring data and alerts in JSON/CSV formats

## 🚀 Installation & Setup

### Prerequisites
- Node.js 14+ and npm installed
- Modern web browser with ES6 support

### Method 1: Local Development Setup

1. **Clone or navigate to the project folder**:
   ```bash
   cd "Hack 2.0"
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start the development server**:
   ```bash
   npm start
   ```

4. **Access the application**:
   - Opens automatically at `http://localhost:3000`
   - Allow notifications when prompted

### Method 2: Production Build

1. **Create production build**:
   ```bash
   npm run build
   ```

2. **Serve the build files** using any static server:
   ```bash
   npm install -g serve
   serve -s build
   ```

### Method 3: Using VS Code with Live Server

1. Install "Live Server" extension from VS Code marketplace
2. Right-click `public/index.html` → "Open with Live Server"
3. Application opens at `http://localhost:5500`

## 📖 How to Use the System

### 1. Initial Setup

- Open the application in your browser
- Allow browser notifications when prompted for alert notifications
- System is ready for monitoring

### 2. Starting Monitoring

1. Navigate to **📊 Monitoring** tab
2. Click **▶️ Start Monitoring** button
3. System begins simulating patient activity
4. Real-time sensor data updates every 3 seconds

### 3. Real-time Monitoring Dashboard

**Vital Signs Section:**
- ❤️ **Heart Rate**: Normal range 60-100 bpm
- 💉 **Blood Pressure**: Tracks systolic/diastolic pressure
- 🫁 **Oxygen Level**: Normal ≥94%
- 🌡️ **Temperature**: Normal 36.5-37.5°C

**Activity Section:**
- 📍 **Posture**: Normal, Lying, Sitting, Standing
- 🚶 **Activity**: Resting, Walking, Sitting, Lying Down
- ⚡ **Movement Level**: Low, Moderate, High
- ⏱️ **Immobility Time**: Tracks duration without movement

### 4. Testing Features

**Control Panel Options:**
- **🔔 Test Alert**: Send test notification to verify alerts work
- **🚨 Simulate Fall**: Trigger emergency fall detection alert
- **⚠️ Simulate Unsafe Posture**: Test unsafe posture detection
- **⏹️ Stop Monitoring**: Pause all monitoring activities

### 5. Viewing Analytics

1. Click **📈 Analytics** tab
2. View comprehensive analytics including:
   - **Key Statistics**: Total alerts, average vitals, heart rate ranges
   - **Heart Rate Trend**: Last 30 readings visualization
   - **Alert Distribution**: Pie chart of alert severity levels
   - **Alert Type Distribution**: Bar chart of alert categories
   - **Recent Alerts Timeline**: Chronological view of recent alerts
   - **Data Export**: Download data in JSON or CSV format

### 6. Alert History

1. Click **📋 Alert History** tab
2. Features include:
   - Search alerts by message or type
   - Filter by severity level (All, Emergency, Warning, Info)
   - View alert statistics
   - Complete alert timeline with details

## 🎯 System Components

### 1. Monitoring Dashboard
- Real-time sensor data display
- Status indicators for each vital sign
- Active alert visualization
- Control buttons for monitoring operations

### 2. Alert System
- **Emergency Alerts** (🚨): Critical conditions requiring immediate action
  - Fall detection
  - Critically low oxygen levels
  
- **Warning Alerts** (⚠️): Concerning conditions needing attention
  - Unsafe posture
  - Prolonged immobility
  - Abnormal heart rate
  
- **Info Alerts** (ℹ️): System updates and test alerts

### 3. Analytics Dashboard
- Heart rate trend visualization
- Alert severity distribution
- Alert type breakdown
- Timeline view of recent events
- Key statistics and metrics

### 4. Simulation Engine
- Random but realistic activity patterns
- Configurable alert thresholds:
  - Immobility timeout: 5 minutes
  - Fall detection: 1% random chance during activity
  - Heart rate range: 60-100 bpm (normal)
  - Oxygen level: ≥94% (normal)
- Smooth data transitions

## 🔧 Technical Stack

- **Frontend Framework**: React 18
- **Visualization**: Recharts for charts and graphs
- **Styling**: CSS3 with responsive design
- **Browser APIs**: Notifications API for alerts
- **State Management**: React Hooks (useState, useEffect)

## 📊 Data Flow

```
System Start
    ↓
Initialize State & Request Notifications
    ↓
User Starts Monitoring
    ↓
Simulation Engine Generates Sensor Data (every 3s)
    ↓
Check Alert Conditions
    ↓
Update Displays & Store Data
    ↓
Send Notifications if Alerts
    ↓
Display in Analytics & History
    ↓
Allow Data Export
```

## 🏥 Real-world Implementation Guide

### Hardware Requirements

1. **Movement Sensors**
   - Accelerometers (3-axis)
   - Gyroscopes
   - Inertial Measurement Units (IMU)

2. **Posture Detection**
   - Pressure sensors (bed/chair)
   - Vision-based systems (privacy-focused)
   - Wearable sensors

3. **Vital Signs Monitoring**
   - Pulse oximeter (SpO2 & Heart Rate)
   - Blood pressure monitor
   - Thermometer
   - ECG sensors (optional)

4. **Communication Hardware**
   - Wi-Fi module
   - Bluetooth module
   - Cellular backup (optional)

5. **Processing Unit**
   - Raspberry Pi 4/5
   - Arduino with gateway
   - Edge device for local processing

### Software Architecture

```
Hardware Layer
    ↓
Data Collection & Preprocessing
    ↓
Anomaly Detection Engine
    ↓
Alert Generation
    ↓
Cloud/Local Storage
    ↓
Dashboard & Notifications
```

### Deployment Options

1. **Home-Care Setup**
   - Local edge device for privacy
   - Cloud backup of critical alerts
   - Mobile app notifications

2. **Facility Setup**
   - Centralized monitoring station
   - Multiple patient monitoring
   - Integration with existing systems

3. **Cloud Deployment**
   - Azure IoT Hub
   - Real-time processing
   - Scalable alerting
   - Historical analytics

## 🔐 Privacy & Security Considerations

- Patient data encryption
- HIPAA compliance
- Minimal data collection
- Local processing options
- Secure cloud transmission
- User consent for notifications

## 📱 Browser Compatibility

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 🎨 Customization

### Changing Alert Thresholds

Edit `src/components/MonitoringDashboard.js`:

```javascript
// Modify immobility alert threshold (in seconds)
if (data.immobilityTime > 300) { // 5 minutes = 300 seconds
  // Alert triggered
}

// Modify fall detection probability
if (data.activity === 'Walking' && Math.random() < 0.01) { // 1% chance
  // Fall alert
}
```

### Adding New Metrics

1. Add new data field in `simulateSensorData()`
2. Create new sensor card in `SensorData.js`
3. Add visualization in `AnalyticsDashboard.js`

### Styling Customization

Modify CSS variables in `App.css` and component-specific CSS files.

## 🐛 Troubleshooting

### Notifications Not Working
- Ensure browser notifications are allowed
- Check browser console for permission errors
- Try reloading the page

### Data Not Updating
- Verify monitoring is started
- Check browser console for errors
- Ensure JavaScript is enabled

### Charts Not Displaying
- Wait for data to accumulate (30+ readings)
- Check browser compatibility
- Verify Recharts is installed properly

## 📈 Performance Tips

- Clear alert history periodically for better performance
- Export old data for archival
- Use Firefox or Chrome for best performance
- Ensure sufficient available memory

## 🤝 Contributing

For improvements and feature additions:
1. Create a new feature branch
2. Make your changes
3. Test thoroughly
4. Submit for review

## 📄 License

This project is created for hackathon purposes. Use and modify as needed.

## 🎓 Learning Resources

- React Documentation: https://react.dev
- Recharts: https://recharts.org
- Web Notifications API: https://developer.mozilla.org/en-US/docs/Web/API/Notifications_API

## 📞 Support

For issues or questions:
1. Check the troubleshooting section
2. Review browser console for errors
3. Verify all dependencies are installed
4. Try clearing browser cache

---

**Smart Patient Monitoring System v1.0**
*Real-time Health Monitoring Solution for Home-Care Environments*
