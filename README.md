<p align="center">
  <a href="https://github.com/viphacker-100/cdr-analyzer-pro">
    <img src="assets/logo.svg" alt="CDR Analyzer Pro Logo" width="560" />
  </a>
</p>

# CDR Analyzer Pro

A powerful web-based Call Detail Record (CDR) analysis tool designed for telecom investigators, law enforcement, and network analysts. This application provides comprehensive analysis of call data from multiple telecom operators with advanced visualization and reporting capabilities.

**Made with ❤️ by [viphacker.100](https://github.com/viphacker-100) (Aryan Ahirwar)**

**Repository**: [https://github.com/viphacker-100/cdr-analyzer-pro](https://github.com/viphacker-100/cdr-analyzer-pro)

*Inspired by [xnoncywer](https://github.com/xnoncywer)*

[![GitHub Repo](https://img.shields.io/badge/GitHub-viphacker--100%2Fcdr--analyzer--pro-181717?style=for-the-badge&logo=github)](https://github.com/viphacker-100/cdr-analyzer-pro)
![CDR Analyzer Pro](https://img.shields.io/badge/CDR-Analyzer%20Pro-blue?style=for-the-badge&logo=chart-line)
![Version](https://img.shields.io/badge/Version-2.1-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

## 🚀 Features

### **📱 Multi-Operator Support**
- **Vodafone Idea (VI)** - Complete CDR format support
- **Jio** - Advanced call termination analysis
- **Airtel** - VoWiFi and enhanced location tracking
- **BSNL** - Government operator format support

### **📊 Advanced Analytics**
- **Call Pattern Analysis** - Incoming/Outgoing call distribution
- **Duration Analysis** - Call duration patterns and statistics
- **IMEI/IMSI Tracking** - Device and SIM card analysis
- **Location Mapping** - Interactive maps with call locations
- **SMS Analysis** - Message header categorization and analysis
- **Network Graph** - Visual call relationship mapping

### **🎨 Modern UI/UX**
- **Responsive Design** - Works on desktop, tablet, and mobile
- **Dark Mode Support** - Automatic theme detection + manual light/dark toggle (persisted)
- **Design System** - Navy/amber "Data-Dense Dashboard" theme with Fira Sans + Fira Code typography, WCAG-checked contrast, reduced-motion support
- **Drag & Drop Upload** - Easy file handling
- **Real-time Notifications** - User feedback system
- **Interactive Charts** - Theme-aware data visualizations
- **Keyboard Shortcuts** - Fast navigation

### **📈 Data Visualization**
- **Call Duration Charts** - Pie charts for duration distribution
- **Time Analysis Charts** - Bar charts for call time patterns
- **Interactive Maps** - Google Maps integration
- **Network Graphs** - D3.js powered relationship visualization
- **Export Capabilities** - Excel export with formatting

### **🔍 Advanced Filtering**
- **Call Type Filtering** - Incoming/Outgoing call separation
- **Date Range Filtering** - Time-based data filtering
- **Mobile Number Filtering** - Specific number analysis
- **Real-time Search** - Instant data filtering
- **Column-based Filtering** - Advanced data exploration

## 🛠️ Installation

### **Prerequisites**
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for external libraries and maps)
- No server setup required - runs entirely in browser

### **Quick Start**
1. **Clone or Download** the repository:
   ```bash
   git clone https://github.com/viphacker-100/cdr-analyzer-pro.git
   ```
   Or download directly from [github.com/viphacker-100/cdr-analyzer-pro](https://github.com/viphacker-100/cdr-analyzer-pro).
2. **Open** `index.html` in your web browser
3. **Start analyzing** CDR data immediately

### **File Structure**
```
cdr-analyzer-pro/
├── index.html                        # Main application file (single-file offline-capable UI)
├── 404.html                          # Custom 404 fallback page with breadcrumb navigation
├── sitemap.xml                       # Search engine sitemap
├── robots.txt                        # Crawler directives & sitemap reference
├── llms.txt                          # Machine-readable project summary for AI tools
├── assets/                           # Brand logos & social share assets (SVG & PNG)
│   ├── logo.svg                      # Horizontal brand banner SVG
│   ├── logo-mark.svg                 # Standalone square vector emblem
│   ├── logo.png                      # High-DPI banner PNG preview
│   ├── logo-mark.png                 # High-DPI square icon PNG
│   └── social-preview.png            # Open Graph / Twitter social card (1200x630)
├── demo_cdr_vi.csv                   # VI operator demo data (20 records)
├── demo_cdr_jio.csv                  # Jio operator demo data (21 records)
├── demo_cdr_bsnl.csv                 # BSNL operator demo data (32 records)
├── demo_cdr_sms.csv                  # SMS analysis demo data (36 records)
├── design-system/cdr-analyzer-pro/   # Design tokens and UI specifications
├── README.md                         # This file
└── README_DEMO_FILES.md              # Demo files documentation
```

## 📖 Usage Guide

### **1. File Upload**
- **Drag & Drop**: Simply drag CSV files onto the upload area
- **File Browser**: Click "Choose Files" to select files
- **Supported Formats**: CSV, Excel (.xlsx, .xls), ZIP archives
- **Multiple Files**: Upload multiple files simultaneously

### **2. Data Analysis**
- **CDR Tab**: View raw call data in table format
- **B Party Analysis**: Analyze called numbers and patterns
- **Max Duration**: Find longest calls and duration patterns
- **IMEI Analysis**: Track device usage and patterns
- **IMSI Analysis**: Analyze SIM card usage
- **Location Analysis**: Map call locations with distance calculations
- **SMS Analysis**: Categorize and analyze SMS messages

### **3. Advanced Features**
- **Call Type Filtering**: Filter by Incoming/Outgoing calls
- **Date Range Filtering**: Analyze specific time periods
- **Mobile Number Filtering**: Focus on specific numbers
- **Chart Generation**: Create visual representations of data
- **Export Results**: Download analysis in Excel format

### **4. Visualization**
- **Interactive Maps**: View call locations on Google Maps
- **Network Graphs**: Visualize call relationships
- **Duration Charts**: Pie charts showing call duration distribution
- **Time Charts**: Bar charts showing call time patterns

## 🔧 Technical Details

### **Supported CDR Formats**

#### **Vodafone Idea (VI)**
```csv
Target /A PARTY NUMBER,CALL_TYPE,Type of Connection,B PARTY NUMBER,LRN- B Party Number,Translation of LRN,Call date,Call Initiation Time,Call Duration,First BTS Location,First Cell Global Id,Last BTS Location,Last Cell Global Id,SMS Centre Number,Service Type,IMEI,IMSI,Call Forwarding Number,Roaming Network/Circle,MSC ID,In TG,Out TG
```

#### **Jio**
```csv
Calling Party Telephone Number,Called Party Telephone Number,Call Forwarding,LRN Called No,Call Date,Call Time,Call Termination Time,Call Duration,First Cell ID,Last Cell ID,Call Type,SMS Center Number,IMEI,IMSI,Roaming Circle Name
```

#### **Airtel**
```csv
Target No,Call Type,TOC,B Party No,LRN No,LRN TSP-LSA,Date,Time,Dur(s),First CGI,First CGI Lat/Long,Last CGI,Last CGI Lat/Long,SMSC No,Service Type,IMEI,IMSI,Call Fow No,Roam Nw,SW & MSC ID,IN TG,OUT TG,Vowifi First UE IP,Port1,Vowifi Last UE IP,Port2
```

#### **BSNL**
```csv
Target/A-Party Number,Call_Type,Type_Of_Conn,B_Party Number,LRN_B_Party_No,LRN_DESCRIPTION,Call_Date,Call_Initiation_Time(CIT),Call_Duration,First_Cell_Desc,First_Cell_id,Last_Cell_Desc,Last_Cell_ID,SMSC_No,Service_Type,IMEI,IMSI,Call_FOW_No,Circle_NW,MSC_ID,IN_TG,OUT_TG
```

### **External Dependencies**
- **Chart.js** - For data visualization charts
- **D3.js** - For network graph visualization
- **Vis.js** - For interactive network graphs
- **Google Maps API** - For location mapping
- **XLSX.js** - For Excel file processing
- **Zip.js** - For ZIP archive handling
- **Font Awesome** - For modern icons

### **Browser Storage**
- **IndexedDB** - Client-side data storage
- **Local Storage** - User preferences and settings
- **Session Storage** - Temporary session data

## 🎯 Use Cases

### **Law Enforcement**
- **Call Pattern Analysis** - Track communication patterns
- **Location Tracking** - Map suspect movements
- **Device Tracking** - Monitor device usage patterns
- **Relationship Mapping** - Visualize call networks

### **Telecom Investigation**
- **Fraud Detection** - Identify suspicious call patterns
- **Network Analysis** - Analyze network usage
- **Customer Behavior** - Understand calling patterns
- **Service Quality** - Monitor call quality metrics

### **Corporate Security**
- **Employee Monitoring** - Track company phone usage
- **Security Audits** - Analyze communication patterns
- **Compliance** - Ensure regulatory compliance
- **Cost Analysis** - Optimize telecom expenses

## 🚀 Advanced Features

### **Real-time Analysis**
- **Live Data Processing** - Instant analysis of uploaded files
- **Progressive Loading** - Handle large datasets efficiently
- **Background Processing** - Non-blocking data analysis
- **Memory Optimization** - Efficient data handling

### **Export Capabilities**
- **Excel Export** - Formatted `.xlsx` workbooks (`Active Analysis Tab`, `Active File Tab`, `All File Tabs`, and table export in `Mobile No. Brief`)
- **Clipboard Copy** - Tabular clipboard copy from active analysis views

### **Security & Privacy Controls**
- **100% Local-First Processing** - File parsing, filtering, charts, Excel generation, IMEI TAC decoding (GSMA RBI + `ImeiTacStore`), and SMS header analysis (TRAI DLT + `SmsHeaderStore`) run completely locally in your browser via `IndexedDB` (`CDRDatabase` v3) with zero third-party lookup calls
- **Offline Reference Dataset Importer & Inline Overrides** - Open **Offline DB** (`<dialog id="settings-dialog">`) to import your own TAC or TRAI DLT header registries (`.csv`, `.tsv`, `.json`, `.xls`, `.xlsx`) into persistent `IndexedDB` stores, or click **Edit** directly in `Max IMEI` / `SMS Analysis` rows to save local analyst notes (`source: "manual"`)
- **Optional Self-Hosted Endpoints** - Leave custom URL templates empty for strict offline resolution (`Offline DB`), or configure your own internal `http://`/`https://` endpoint URLs (`{tac}`, `{header}`) for intranet database lookups (`Custom API`) whose hits cache into `IndexedDB`
- **User-Configured Google Maps & Offline Mode** - No Google Maps API key is bundled in source; enter your own key in **Offline Reference DB & API Settings** for live map views, or inspect call location coordinates locally offline
- **Subresource Integrity (SRI)** - External version-pinned CDN libraries and stylesheets enforce `sha384` integrity digests with `crossorigin="anonymous"` and `no-referrer` policy

## 🔍 Analysis Capabilities

### **Call Analysis**
- **Call Volume** - Total number of calls
- **Call Duration** - Average and total duration
- **Call Direction** - Incoming vs Outgoing analysis
- **Call Timing** - Time-based call patterns
- **Call Frequency** - Call frequency analysis

### **Location Analysis**
- **Call Locations** - Geographic call distribution
- **Movement Patterns** - User movement tracking
- **Location Clustering** - Geographic clustering analysis
- **Distance Calculations** - Inter-location distances
- **Route Analysis** - Movement route visualization

### **Device Analysis**
- **IMEI Tracking** - Device usage patterns
- **Device Details** - Device manufacturer and model
- **Multi-device Usage** - Multiple device analysis
- **Device Switching** - Device change patterns

### **Network Analysis**
- **Call Networks** - Visual call relationship mapping
- **Contact Analysis** - Most contacted numbers
- **Network Clusters** - Call network clustering
- **Relationship Strength** - Call frequency relationships

## 🎨 UI/UX Features

### **Modern Design**
- **Gradient Backgrounds** - Beautiful visual appeal
- **Smooth Animations** - Professional user experience
- **Responsive Layout** - Works on all screen sizes
- **Intuitive Navigation** - Easy-to-use interface

### **Interactive Elements**
- **Hover Effects** - Visual feedback on interaction
- **Click Animations** - Smooth button animations
- **Loading States** - Progress indicators
- **Error Handling** - User-friendly error messages

### **Accessibility**
- **Keyboard Navigation** - Full keyboard support
- **Screen Reader Support** - Accessibility compliance
- **High Contrast** - Better visibility
- **Font Scaling** - Adjustable text size

## 🔧 Configuration

### **Customization Options**
- **Theme Selection** - Light/Dark mode
- **Language Support** - Multi-language interface
- **Export Formats** - Configurable export options
- **Chart Types** - Customizable visualizations

### **Performance Settings**
- **Data Loading** - Configurable batch sizes
- **Memory Usage** - Optimizable memory settings
- **Processing Speed** - Adjustable processing parameters
- **Cache Settings** - Configurable caching options

## 📊 Demo Data

The project includes four demo CSV files covering three operators plus SMS records (Airtel format headers are also supported when you upload your own Airtel export):

- **demo_cdr_vi.csv** - Vodafone Idea format (20 records)
- **demo_cdr_jio.csv** - Jio format (21 records)
- **demo_cdr_bsnl.csv** - BSNL format (32 records)
- **demo_cdr_sms.csv** - SMS analysis demo data (36 records)

See `README_DEMO_FILES.md` for detailed demo file documentation.

## 🚀 Getting Started

### **Quick Test**
1. Open `index.html` in your browser
2. Upload any demo CSV file
3. Explore different analysis tabs
4. Try filtering and chart features
5. Export results to Excel

### **Full Analysis**
1. Upload multiple CDR files
2. Use all analysis tabs
3. Generate charts and visualizations
4. Create network graphs
5. Export comprehensive reports

## 🤝 Contributing

### **Development Setup**
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

### **Testing**
- Test with all operator formats
- Verify all analysis features
- Check export functionality
- Test on different browsers
- Validate mobile responsiveness

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- **Chart.js** - For beautiful data visualizations
- **D3.js** - For network graph visualization
- **Google Maps API** - For location mapping
- **Font Awesome** - For modern icons
- **XLSX.js** - For Excel file processing

## 📞 Support

For support, questions, or feature requests:

- **Repository**: [https://github.com/viphacker-100/cdr-analyzer-pro](https://github.com/viphacker-100/cdr-analyzer-pro)
- **Issues**: [Create an issue on GitHub](https://github.com/viphacker-100/cdr-analyzer-pro/issues)
- **Documentation**: Check the demo files and documentation
- **Testing**: Use the provided demo files for testing

## 🔄 Version History

### **v2.1** - Current Version
- 🔒 Removed hardcoded Google Maps API key and replaced third-party TAC/SMS API calls with an offline-first architecture: `CDRDatabase` v3 (`ImeiTacStore`, `SmsHeaderStore`), built-in GSMA RBI / TRAI DLT protocol decoders + curated SMS dictionary, CSV/TSV/JSON/XLS/XLSX dataset importers, inline row annotations, and optional self-hosted HTTP/HTTPS endpoint URLs (`<dialog id="settings-dialog">`)
- 🛡️ Version-pinned CDN dependencies with `sha384` Subresource Integrity, `referrerpolicy="no-referrer"`, text-cell Excel serialization (`raw: true`), and DOM/textContent-only rendering (zero `innerHTML` writes)
- 🔧 Fixed mobile/date filtering, Excel workbook exports, DD/MM/YYYY date sorting, ZIP/Excel nested extraction, and responsive `#analysis-view` separation

### **v2.0**
- ✨ Modern UI/UX redesign
- 📊 Interactive charts and visualizations
- 🔔 Real-time notification system
- ⌨️ Keyboard shortcuts
- 🌙 Dark mode support
- 📱 Enhanced mobile responsiveness
- 🎯 Advanced filtering capabilities
- 📈 Improved export functionality

### **v1.0** - Initial Release
- 📱 Basic CDR analysis
- 📊 Simple data visualization
- 📁 File upload support
- 📤 Basic export functionality

---

**CDR Analyzer Pro** - Professional CDR analysis made simple and powerful! 🚀 