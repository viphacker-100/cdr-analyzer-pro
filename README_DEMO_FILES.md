# CDR Analyzer Demo Files

This directory contains demo CDR (Call Detail Record) files for testing the CDR Analyzer Pro application. These files simulate real-world CDR data from different telecom operators.

## 📁 Demo Files Available

### 1. **demo_cdr_vi.csv** - Vodafone Idea (VI) Format
- **Target Number**: 9876543210
- **Records**: 20 calls
- **Features**: 
  - Incoming/Outgoing calls
  - Different call durations (90-300 seconds)
  - Various B Party numbers
  - Location data (Delhi Central)
  - IMEI/IMSI data

### 2. **demo_cdr_jio.csv** - Jio Format
- **Target Number**: 9876543211
- **Records**: 21 calls
- **Features**:
  - Incoming/Outgoing calls
  - Call termination times
  - Different call durations (115-195 seconds)
  - Location data (Delhi coordinates)
  - IMEI/IMSI data

> **Note:** Airtel CDR format exports (`Target No`, `Dur(s)`, `First CGI Lat/Long`, VoWiFi columns) are also supported by [index.html](index.html), though no standalone Airtel sample file is bundled in this directory.

### 3. **demo_cdr_bsnl.csv** - BSNL Format
- **Target Number**: 9876543213
- **Records**: 32 calls
- **Features**:
  - Incoming/Outgoing calls
  - Different call durations (120-300 seconds)
  - Location data (Delhi Central)
  - IMEI/IMSI data

### 4. **demo_cdr_sms.csv** - SMS Data
- **Target Number**: 9876543214
- **Records**: 36 SMS records
- **Features**:
  - SMS service type
  - Various SMS headers (AD-VERIFY, OTP, INFO, ALERT)
  - Zero duration (SMS)
  - Location data

## 🧪 Testing Features

### **Basic CDR Analysis**
1. Upload any demo file
2. Test the **CDR** tab to view raw data
3. Test **B Party** analysis
4. Test **Max Duration** analysis
5. Test **IMEI/IMSI** analysis

### **Advanced Features**
1. **Call Type Filtering**: Test Incoming/Outgoing filters
2. **Date Range Filtering**: Use date range 12/06/2024 to 15/06/2024
3. **Mobile Number Filtering**: Use target numbers from demo files
4. **Charts**: Test duration and time distribution charts
5. **SMS Analysis**: Use demo_cdr_sms.csv for SMS analysis

### **Multi-Operator Testing**
1. Upload multiple demo files from different operators
2. Test **Common B Party** analysis
3. Test **Common IMEI** analysis
4. Test **Network Graph** visualization

### **Export Features**
1. Test **Export Active File Tab**
2. Test **Export All File Tabs**
3. Test **Export Active Analysis Tab**

## 📊 Data Patterns in Demo Files

### **Call Patterns**
- **Time Distribution**: Calls spread across different hours
- **Duration Patterns**: Mix of short (90s) and long (300s) calls
- **Direction Mix**: Balanced incoming/outgoing calls

### **Location Data**
- **Delhi Central**: 28.7041/77.1025
- **Delhi Coordinates**: 28.6139/77.2090
- **Gurgaon**: 28.4595/77.0266

### **IMEI/IMSI Patterns**
- **VI**: 123456789012345 / 987654321098765
- **Jio**: 234567890123456 / 987654321198765
- **Airtel**: 345678901234567 / 987654321298765
- **BSNL**: 456789012345678 / 987654321398765

### **SMS Headers**
- **AD-VERIFY**: Advertisement verification
- **OTP-XXXX**: One-time passwords
- **INFO-XXXX**: Information messages
- **ALERT-XXXX**: Alert notifications

## 🚀 How to Use

1. **Open the CDR Analyzer Pro** application
2. **Upload demo files** using drag & drop or file browser
3. **Test different tabs** and analysis features
4. **Try filtering** by call type, date range, or mobile number
5. **Generate charts** for duration and time analysis
6. **Export results** in Excel format

## 📈 Expected Results

### **B Party Analysis**
- Should show top called numbers
- Count of calls to each B Party
- First and last call timestamps

### **Duration Analysis**
- Should show total duration by B Party
- Average call duration calculations
- Duration distribution charts

### **IMEI Analysis**
- Should show GSMA Reporting Body Identifier (RBI) fallback metadata offline, or full device model details from user-imported TAC datasets / inline edits (`IndexedDB` `ImeiTacStore`)
- Count of calls per IMEI
- Target numbers associated with each IMEI

### **SMS Analysis**
- Should normalize TRAI DLT headers (`<prefix>-<SenderID>[-<T|S|P|G>]`), match curated banking/govt/telecom entities and local header patterns offline, or apply user-imported DLT sheets / inline overrides (`IndexedDB` `SmsHeaderStore`)
- Show entity names and purposes
- Count of each raw `B Party` and grouped `Unique_SMS` header

### **Location Analysis**
- Should show call locations on map
- Distance calculations between locations
- Location clustering

## 🔧 Troubleshooting

### **File Upload Issues**
- Ensure files are in CSV format
- Check file encoding (UTF-8)
- Verify column headers match expected format

### **Analysis Issues**
- Ensure all required columns are present
- Check date format (DD/MM/YYYY)
- Verify time format (HH:MM:SS)

### **Chart Issues**
- Ensure Chart.js library is loaded
- Check browser console for errors
- Verify data format for charts

## 📝 Notes

- These are **demo files** with simulated data
- **IMEI/IMSI** numbers are fictional
- **Location coordinates** are approximate
- **Phone numbers** are dummy numbers
- **Dates** are set in June 2024 for testing

## 🎯 Testing Checklist

- [ ] Upload single file
- [ ] Upload multiple files
- [ ] Test all analysis tabs
- [ ] Test filtering features
- [ ] Test chart generation
- [ ] Test export functionality
- [ ] Test SMS analysis
- [ ] Test location mapping
- [ ] Test network graph
- [ ] Test keyboard shortcuts

Use these demo files to thoroughly test all features of the CDR Analyzer Pro application! 