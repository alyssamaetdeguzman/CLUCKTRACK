<div align="center">

  <!-- Header Banner -->
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20,30,40&height=185&section=header&text=CluckTrack&fontSize=50&fontColor=fff&animation=fadeIn&fontAlignY=35&desc=Agricultural%20ERP%20&%20Real-time%20Production%20Analytics%20System&descSize=15&descAlignY=62" width="100%" />

  <p align="center">
    <i>Transitioning local poultry farming operations from manual records and fragmented spreadsheets into a centralized, data-driven digital pipeline.</i>
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Status-In%20Active%20Development-orange?style=for-the-badge&logo=git&logoColor=white" alt="Status" />
    <img src="https://img.shields.io/badge/Capstone-Academic-blue?style=for-the-badge&logo=graduation-dot-com&logoColor=white" alt="Capstone" />
    <img src="https://img.shields.io/badge/ERP-Agricultural-success?style=for-the-badge&logo=databricks&logoColor=white" alt="ERP" />
    <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge&logo=opensourceinitiative&logoColor=white" alt="License" />
  </p>

</div>

---

## 📌 About CluckTrack

**CluckTrack** is an enterprise-grade Agricultural ERP web application engineered to modernize poultry farm management. Developed as an academic capstone project, it eliminates error-prone paper ledgers and disconnected Google Sheets, replacing them with a unified real-time dashboard that tracks dynamic inventory, monitors daily production yields, and processes predictive analytics for optimized farm profitability.

---

## 🚀 Key Features

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>📦 Dynamic CRUD Inventory Module</h3>
      <p>Real-time tracking of feed stock, livestock batches, mortality rates, and operational supplies equipped with automated low-stock threshold alerts.</p>
    </td>
    <td width="50%" valign="top">
      <h3>📈 Production & KPI Analytics</h3>
      <p>Interactive data visualizations powered by <b>Chart.js</b> tracking key agricultural metrics like Feed Conversion Ratios (FCR) and egg/meat production yields.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🔮 Strategic Forecasting Engine</h3>
      <p>Python-powered predictive analytics processing historical farm cycles to generate actionable profitability reports and assist in forward resource planning.</p>
    </td>
    <td width="50%" valign="top">
      <h3>🔒 RBAC & Comprehensive Audit Trails</h3>
      <p>Secure Role-Based Access Control separating permissions for administrators and staff, backed by a detailed system activity logging framework.</p>
    </td>
  </tr>
</table>

---

## 🛠️ Technology Stack

<div align="center">

### Backend & Analytics
<img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
<img src="https://img.shields.io/badge/Apache-D22128?style=for-the-badge&logo=apache&logoColor=white" />

### Frontend & UI
<img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chart.js&logoColor=white" />
<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />

### Tools & Deployment
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
<img src="https://img.shields.io/badge/Railway-131415?style=for-the-badge&logo=railway&logoColor=white" />
<img src="https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white" />

</div>

---

## 📂 Project Architecture

<details>
<summary><b>📂 Click to expand complete directory tree structure</b></summary>

```text
clucktrack/
├── assets/
│   ├── css/            # Custom Tailwind and layout stylesheets
│   ├── js/             # Frontend interaction scripts and Chart.js wrappers
│   └── img/            # System avatars, logos, and UI illustration graphics
├── config/
│   └── db.php          # Database connection handler and environment mapping
├── includes/
│   ├── navbar.php      # Navigation header component with user profile dropdown
│   ├── sidebar.php     # Dynamic sidebar navigation controlled by RBAC roles
│   ├── footer.php      # Global footer component
│   └── auth_check.php  # Role-based access control validation middleware
├── modules/
│   ├── inventory/      # Stock management CRUD interfaces & low-stock alerts
│   ├── production/     # Daily egg/meat yield logging and mortality tracking
│   ├── analytics/      # Chart.js visualization dashboards and KPI summaries
│   └── audit/          # System activity audit logs for administrative monitoring
├── python_engine/
│   ├── forecaster.py   # Python prediction models for cycle profitability forecasting
│   └── requirements.txt# Python pipeline dependencies (pandas, numpy, etc.)
├── database/
│   └── schema.sql      # Database initialization schema, tables, and seed roles
├── index.php           # Application entry point & login authentication redirect
└── dashboard.php       # Main administrative analytics control center
