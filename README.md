# Refrigerator & Freezer Temperature Management System 🌡️

A professional web application for managing temperature monitoring of 10 refrigerators and 4 freezers (14 units total). Features twice-daily (AM/PM) temperature recording and monthly monitoring capabilities.

## 🎯 Project Overview

This system is a web-based solution designed for systematic temperature recording and monitoring of refrigerated/frozen storage facilities for food safety and HACCP compliance.

### Main Purpose
- Accurate recording and tracking of refrigerator/freezer temperatures
- Immediate detection and alerting of abnormal temperatures
- Visualization of monthly temperature trends
- Management and accountability tracking by personnel

## ✨ Key Features

### 1. 📊 Dashboard
- **Real-time Status**: Total device count, today's records, abnormal temperature occurrences
- **Abnormal Temperature Alerts**: Immediate display of out-of-range temperatures
- **Recent Records**: Table showing last 20 temperature records
- **Quick Record**: One-click access to temperature recording screen

### 2. 📝 Temperature Recording
- **Batch Input**: Simultaneous input for all 14 devices on one screen
- **Period Classification**: AM/PM time period selection
- **Personnel Recording**: Automatic saving of person in charge name
- **Notes Feature**: Record special notes or observations
- **Real-time Validation**: Display of normal temperature ranges and automatic validation

### 3. ⚙️ Device Management
- **Device Information**: Manage 10 refrigerators and 4 freezers
- **Temperature Range Settings**: Customize normal temperature range per device
  - Refrigerator default: 32°F ~ 50°F
  - Freezer default: -13°F ~ 5°F
- **Device Naming**: Edit individual device names
- **Individual Settings**: Independent temperature criteria per device

### 4. 📈 Monthly Report
- **Temperature Change Chart**: Interactive graph using Chart.js
  - Select all devices or individual devices
  - Daily average temperature trends
  - Normal range boundary display (when individual device selected)
- **Statistical Summary**:
  - Average temperature
  - Highest/lowest temperatures
  - Abnormal temperature count and rate
- **Abnormal Temperature Analysis**: Device-by-device abnormal occurrence count and rate
- **Personnel Analysis**: Recording status and participation by personnel

## 🚀 Getting Started

### Access Method
Open the `index.html` file in any web browser to start using immediately.

### Supported Environments
- ✅ **PC**: Windows, Mac, Linux (Chrome, Firefox, Edge, Safari)
- ✅ **Mobile**: Android, iOS (all major browsers)
- ✅ **Tablet**: iPad, Android tablets

### Initial Setup
1. On first run, 14 devices are automatically created
   - Refrigerator 1-10
   - Freezer 1-4
2. If needed, modify device names and temperature ranges in the "Devices" menu

## 📱 How to Use

### Recording Temperature
1. Select **"Record"** tab from bottom navigation
2. Select date and period (AM/PM) (auto-filled with current)
3. Enter person in charge name
4. Input temperature for each of the 14 devices
5. Add notes if necessary
6. Click **"Save"** button

💡 **Tip**: Normal range is displayed next to each temperature input field for reference!

### Viewing Reports
1. Select **"Report"** tab from bottom navigation
2. Select month (year/month) to view
3. Select device (all or individual)
4. Click **"Search"** button
5. Review charts and statistics

### Changing Device Settings
1. Select **"Devices"** tab from bottom navigation
2. Click **"Edit Settings"** button for the device to modify
3. Edit device name, minimum/maximum temperature
4. Click **"Save"** button

## 🎨 Screen Layout

### Bottom Navigation (4 Tabs)
- 🏠 **Dashboard**: Today's status and recent records
- ✏️ **Record**: Batch temperature input for 14 devices
- 📦 **Devices**: Device information and settings management
- 📊 **Report**: Monthly charts and statistical analysis

## 💾 Data Storage

### LocalStorage Usage
- All data is stored in browser's LocalStorage
- Works without server or internet connection
- Data persists within the same browser

### Data Structure
```javascript
// Device Information
{
  id: "fridge-1",
  name: "Refrigerator 1",
  type: "fridge",
  minTemp: 32,
  maxTemp: 50
}

// Temperature Record
{
  id: "unique-id",
  date: "2026-03-15",
  period: "AM",
  deviceId: "fridge-1",
  temperature: 41.4,
  person: "John Smith",
  memo: "Normal",
  timestamp: 1710489600000
}
```

### Data Backup Recommended
⚠️ LocalStorage data may be deleted when browser data is cleared. Regularly backup important data through export features.

## 🛠️ Technology Stack

### Frontend
- **HTML5**: Semantic markup
- **CSS3**: Modern styling and responsive design
- **Vanilla JavaScript**: Pure JS without frameworks

### Libraries (CDN)
- **Chart.js 4.4.0**: Temperature change chart visualization
- **Font Awesome 6.4.0**: Icon set

### Data Storage
- **LocalStorage API**: Browser local storage

## 📋 Feature Details

### Completed Features ✅

#### 1. Dashboard
- [x] Display total device count
- [x] Display today's record count
- [x] Display abnormal temperature count
- [x] Abnormal temperature alert banner
- [x] Recent 20 records table
- [x] Temperature recording button

#### 2. Temperature Recording
- [x] Date selection (default: today)
- [x] Period selection (AM/PM, auto-set)
- [x] Person in charge input
- [x] Notes input
- [x] Batch temperature input for 14 devices
- [x] Normal temperature range display
- [x] Input data validation
- [x] Save and reset functionality

#### 3. Device Management
- [x] Display 14 device list
- [x] Device type distinction (refrigerator/freezer)
- [x] Normal temperature range display
- [x] Device settings modal
- [x] Device name editing
- [x] Temperature range editing
- [x] Settings save functionality

#### 4. Report
- [x] Month selection filter
- [x] Device selection filter (all/individual)
- [x] Temperature change line chart
- [x] Statistics cards (average/highest/lowest/abnormal)
- [x] Device-by-device abnormal temperature occurrence status
- [x] Personnel-by-personnel recording status
- [x] Normal range line display when individual device selected

#### 5. UI/UX
- [x] Responsive design (mobile/tablet/PC)
- [x] Bottom tab navigation
- [x] Modern and professional design
- [x] Intuitive user interface
- [x] Touch-friendly UI (mobile)

### Future Enhancement Possibilities 💡

#### Data Management
- [ ] Excel/CSV export feature
- [ ] Data import feature
- [ ] Data backup/restore feature
- [ ] Record edit/delete feature

#### Alert Features
- [ ] Push notification on abnormal temperature
- [ ] Recording time reminder
- [ ] Regular inspection alerts

#### Advanced Features
- [ ] Device-by-device history detailed view
- [ ] PDF report generation
- [ ] Multi-user support (permission management)
- [ ] Cloud synchronization
- [ ] Photo attachment feature

#### Analysis Features
- [ ] Predictive analysis (temperature pattern analysis)
- [ ] Abnormal temperature trend analysis
- [ ] Device performance monitoring
- [ ] Temperature distribution by time period

## 🎯 Use Cases

### Food Industry
- Food storage temperature management
- HACCP record management
- Hygiene inspection preparation

### Hospitals/Pharmacies
- Medicine storage temperature management
- Vaccine storage temperature tracking
- Compliance with legal requirements

### Research Labs
- Experimental sample storage
- Precision temperature control
- Data recording and reporting

### Logistics/Distribution
- Cold/frozen warehouse management
- Cold chain management
- Quality assurance

## 📞 Support & Inquiries

### Troubleshooting
- **Data disappeared**: Data is deleted when browser cache/cookies are cleared. Regular backup is recommended.
- **Chart not showing**: Check internet connection (Chart.js CDN load required).
- **Slow on mobile**: Too many records may cause slowness. Clean up old data.

### Browser Compatibility
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 📄 License

This project is free to use, modify, and distribute.

## 🔄 Update History

### v1.0.0 (2026-03-15)
- ✨ Initial version release
- 🎯 14 device management feature
- 📝 Twice-daily temperature recording feature
- 📊 Monthly report and charts
- 📱 Mobile/PC responsive support
- 💾 LocalStorage-based data storage
- 🌡️ Fahrenheit temperature unit
- 🌐 English interface

## 📐 Temperature Conversion Reference

For your reference, the default temperature ranges convert as follows:

**Refrigerators:**
- Celsius: 0°C to 10°C
- **Fahrenheit: 32°F to 50°F** (current setting)

**Freezers:**
- Celsius: -25°C to -15°C
- **Fahrenheit: -13°F to 5°F** (current setting)

All temperature inputs and displays use Fahrenheit (°F) throughout the application.

---

**Start systematic and efficient temperature management with the Refrigerator & Freezer Temperature Management System!** 🌡️✨
