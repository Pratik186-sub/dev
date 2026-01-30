# Smart Patient Monitoring System - Quick Start Guide

## What You'll Build

A professional React-based web application for real-time patient monitoring with:
- Real-time vital signs tracking
- Fall detection system
- Posture monitoring
- Immobility alerts
- Beautiful analytics dashboard
- Complete alert history

## Quick Setup

### 1. Install Node.js (if not already installed)
Download from: https://nodejs.org/ (LTS version recommended)

### 2. Navigate to Project Folder
```bash
cd "Hack 2.0"
```

### 3. Install Dependencies
```bash
npm install
```

### 4. Start Development Server
```bash
npm start
```

The app will automatically open at http://localhost:3000

## How to Use

### Monitoring Tab
1. Click "Start Monitoring" to begin
2. System simulates patient activity every 3 seconds
3. View real-time vitals and activity data
4. Use test buttons to simulate different conditions

### Analytics Tab
1. View heart rate trends
2. See alert distribution
3. Analyze alert types
4. Export data as JSON or CSV

### Alert History Tab
1. Search for specific alerts
2. Filter by severity level
3. View complete timeline
4. Track alert statistics

## Key Features Explained

**Real-time Monitoring:**
- Heart Rate, Blood Pressure, Oxygen Level, Temperature
- Activity tracking, Posture detection
- Movement level monitoring

**Intelligent Alerts:**
- Emergency: Fall detected, low oxygen
- Warning: Unsafe posture, prolonged immobility
- Info: System updates, test alerts

**Analytics:**
- 30-day heart rate trends
- Alert severity distribution
- Alert type breakdown
- Complete audit trail

## File Structure

```
Hack 2.0/
├── package.json           # Project dependencies
├── README.md             # Full documentation
├── QUICKSTART.md         # This file
├── public/
│   ├── index.html        # Main HTML file
│   └── manifest.json     # PWA manifest
└── src/
    ├── App.js            # Main app component
    ├── App.css           # Main styling
    ├── index.js          # Entry point
    └── components/
        ├── MonitoringDashboard.js/.css
        ├── SensorData.js/.css
        ├── AlertPanel.js/.css
        ├── ControlPanel.js/.css
        ├── AnalyticsDashboard.js/.css
        └── AlertHistory.js/.css
```

## Customization Examples

### Change Alert Threshold
Edit `src/components/MonitoringDashboard.js` line ~100:
```javascript
// Alert after 10 minutes instead of 5
if (data.immobilityTime > 600) {
```

### Adjust Heart Rate Range
```javascript
// Change normal range to 55-105 bpm
if (data.heartRate < 55 || data.heartRate > 105) {
```

## Common Issues & Solutions

| Issue | Solution |
|-------|----------|
| Port 3000 in use | Run `npm start -- --port 3001` |
| Notifications not working | Check browser notification permissions |
| Dependencies error | Delete `node_modules` and run `npm install` again |
| Charts not showing | Wait for 30+ data readings to accumulate |

## Building for Production

```bash
npm run build
```

This creates an optimized build in the `build/` folder.

## Next Steps

1. ✅ Run `npm install`
2. ✅ Run `npm start`
3. ✅ Explore the monitoring dashboard
4. ✅ Test alert features
5. ✅ Check analytics dashboard
6. ✅ Export some sample data

## Tips

- Allow browser notifications for better alert experience
- Use Chrome or Firefox for best performance
- The system generates realistic but simulated data
- All data stays in your browser (no cloud upload)
- Perfect for hackathon presentations!

## Need Help?

- Check README.md for detailed documentation
- Review console errors (F12 → Console)
- Try clearing browser cache
- Ensure Node.js is properly installed

---

Enjoy building! 🚀
