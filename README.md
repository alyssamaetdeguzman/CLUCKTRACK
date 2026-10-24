<div align="center">

  <!-- Red-Themed Header Banner -->
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=20,3,3,10,15&height=185&section=header&text=CluckTrack&fontSize=50&fontColor=fff&animation=fadeIn&fontAlignY=35&desc=Agricultural%20ERP%20&%20Real-time%20Production%20Analytics%20System&descSize=15&descAlignY=62" width="100%" />

  <p align="center">
    <i>Transitioning local poultry farming operations from manual records and fragmented spreadsheets into a centralized, data-driven digital pipeline.</i>
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Status-In%20Active%20Development-red?style=for-the-badge&logo=git&logoColor=white" alt="Status" />
    <img src="https://img.shields.io/badge/Capstone-Academic-darkred?style=for-the-badge&logo=graduation-dot-com&logoColor=white" alt="Capstone" />
    <img src="https://img.shields.io/badge/ERP-Agricultural-crimson?style=for-the-badge&logo=databricks&logoColor=white" alt="ERP" />
    <img src="https://img.shields.io/badge/License-MIT-firebrick?style=for-the-badge&logo=opensourceinitiative&logoColor=white" alt="License" />
  </p>

</div>

<div style="border: 2px solid #dc2626; border-radius: 12px; padding: 25px; margin-top: 20px; background-color: #fef2f2; color: #1f2937;">

  <h2 align="center" style="color: #991b1b; border-bottom: 2px solid #fca5a5; padding-bottom: 10px;">🔴 CLUCKTRACK: SYSTEM DOCUMENTATION & SETUP GUIDE 🔴</h2>

  <p align="center">
    <b>Web-based Real-time Inventory & Production Analytics System</b><br>
    <i>All-in-one repository master guide, project structure, and automated setup instructions.</i>
  </p>

  <hr style="border: 0; height: 1px; background: #fca5a5; margin: 20px 0;">

  <h3>📌 About CluckTrack</h3>
  <p><strong>CluckTrack</strong> is an enterprise-grade Agricultural ERP web application engineered to modernize poultry farm management. Developed as an academic capstone project, it eliminates error-prone paper ledgers and disconnected Google Sheets, replacing them with a unified real-time dashboard that tracks dynamic inventory, monitors daily production yields, and processes predictive analytics for optimized farm profitability.</p>

  <h3 style="margin-top: 25px;">🚀 Key Features</h3>
  <table width="100%" style="border-collapse: collapse;">
    <tr>
      <td width="50%" valign="top" style="padding: 10px; background: #fff; border: 1px solid #f87171; border-radius: 8px;">
        <h4 style="color: #991b1b; margin-top: 0;">📦 Dynamic CRUD Inventory Module</h4>
        <p style="font-size: 14px;">Real-time tracking of feed stock, livestock batches, mortality rates, and operational supplies equipped with automated low-stock threshold alerts.</p>
      </td>
      <td width="50%" valign="top" style="padding: 10px; background: #fff; border: 1px solid #f87171; border-radius: 8px;">
        <h4 style="color: #991b1b; margin-top: 0;">📈 Production & KPI Analytics</h4>
        <p style="font-size: 14px;">Interactive data visualizations powered by <b>Chart.js</b> tracking key agricultural metrics like Feed Conversion Ratios (FCR) and egg/meat production yields.</p>
      </td>
    </tr>
    <tr>
      <td width="50%" valign="top" style="padding: 10px; background: #fff; border: 1px solid #f87171; border-radius: 8px; margin-top: 10px;">
        <h4 style="color: #991b1b; margin-top: 0;">🔮 Strategic Forecasting Engine</h4>
        <p style="font-size: 14px;">Python-powered predictive analytics processing historical farm cycles to generate actionable profitability reports and assist in forward resource planning.</p>
      </td>
      <td width="50%" valign="top" style="padding: 10px; background: #fff; border: 1px solid #f87171; border-radius: 8px; margin-top: 10px;">
        <h4 style="color: #991b1b; margin-top: 0;">🔒 RBAC & Audit Trails</h4>
        <p style="font-size: 14px;">Secure Role-Based Access Control separating permissions for administrators and staff, backed by a detailed system activity logging framework.</p>
      </td>
    </tr>
  </table>

  <h3 style="margin-top: 25px;">🛠️ Technology Stack</h3>
  <div align="center">
    <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" />
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
    <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
    <img src="https://img.shields.io/badge/Apache-D22128?style=for-the-badge&logo=apache&logoColor=white" />
    <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" />
    <img src="https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chart.js&logoColor=white" />
    <img src="https://img.shields.io/badge/Railway-131415?style=for-the-badge&logo=railway&logoColor=white" />
  </div>

  <h3 style="margin-top: 25px;">📂 Project Architecture</h3>
  <pre style="background: #1f2937; color: #f87171; padding: 15px; border-radius: 8px; text-align: left; font-family: monospace;"><code>clucktrack/
├── assets/
│   ├── css/            # Custom Tailwind and layout stylesheets
│   ├── js/             # Frontend interaction scripts & Chart.js wrappers
│   └── img/            # System avatars, logos, and UI illustration graphics
├── config/
│   └── db.php          # Database connection handler & environment mapping
├── includes/
│   ├── navbar.php      # Navigation header component with user dropdown
│   ├── sidebar.php     # Dynamic sidebar navigation controlled by RBAC roles
│   ├── footer.php      # Global footer component
│   └── auth_check.php  # Role-based access control validation middleware
├── modules/
│   ├── inventory/      # Stock management CRUD interfaces & low-stock alerts
│   ├── production/     # Daily egg/meat yield logging & mortality tracking
│   ├── analytics/      # Chart.js visualization dashboards & KPI summaries
│   └── audit/          # System activity audit logs for administrative monitoring
├── python_engine/
│   ├── forecaster.py   # Python prediction models for cycle profitability forecasting
│   └── requirements.txt# Python pipeline dependencies (pandas, numpy, etc.)
├── database/
│   └── schema.sql      # Database initialization schema, tables, and seed roles
├── index.php           # Application entry point & login authentication redirect
└── dashboard.php       # Main administrative analytics control center</code></pre>

  <h3 style="margin-top: 25px;">⚙️ Automated Installation & Setup Guide</h3>
  <div style="background: #ffffff; padding: 15px; border-radius: 8px; border: 1px solid #fca5a5; text-align: left;">
    <h4>📋 Prerequisites</h4>
    <ul>
      <li><b>XAMPP</b> (or any local LAMP/WAMP server stack supporting <b>PHP 8.x</b> and <b>MySQL</b>)</li>
      <li><b>Python 3.x</b> (Required for running the predictive forecasting analytics engine)</li>
      <li><b>Git</b> (For version control and repository cloning)</li>
    </ul>

    <h4>Step 1: Clone the Repository</h4>
    <pre style="background: #f3f4f6; padding: 8px; border-radius: 4px;"><code>git clone https://github.com/alyssamaetdeguzman/clucktrack.git</code></pre>

    <h4>Step 2: Move to Local Server Root Directory</h4>
    <p>Move the cloned folder into your local server web root directory (e.g., <code>C:\xampp\htdocs\clucktrack</code> for XAMPP).</p>

    <h4>Step 3: Initialize and Configure the Database</h4>
    <ol>
      <li>Start <b>Apache</b> and <b>MySQL</b> modules from your XAMPP Control Panel.</li>
      <li>Open your browser and navigate to phpMyAdmin: <code>http://localhost/phpmyadmin</code></li>
      <li>Create a new database named <b><code>clucktrack_db</code></b>.</li>
      <li>Select the database, click the <b>Import</b> tab, upload <code>database/schema.sql</code>, and click <b>Go</b>.</li>
    </ol>

    <h4>Step 4: Configure Database Connection</h4>
    <p>Open <code>config/db.php</code> and verify your database settings:</p>
    <pre style="background: #f3f4f6; padding: 8px; border-radius: 4px;"><code>&lt;?php
$host = 'localhost';
$db   = 'clucktrack_db';
$user = 'root';
$pass = ''; // Default XAMPP password is blank

try {
    $pdo = new PDO("mysql:host=$host;dbname=$db;charset=utf8mb4", $user, $pass, [
        PDO::ATTR_ERRMODE => PDO::ERRMODE_EXCEPTION,
        PDO::ATTR_DEFAULT_FETCH_MODE => PDO::FETCH_ASSOC
    ]);
} catch (\PDOException $e) {
    throw new \PDOException($e->getMessage(), (int)$e->getCode());
}
?&gt;</code></pre>

    <h4>Step 5: Install Python Dependencies</h4>
    <pre style="background: #f3f4f6; padding: 8px; border-radius: 4px;"><code>cd path/to/clucktrack/python_engine
pip install -r requirements.txt</code></pre>

    <h4>Step 6: Launch the Application</h4>
    <p>Open your browser and navigate to: <b><code>http://localhost/clucktrack/index.php</code></b></p>
  </div>

  <h3 style="margin-top: 30px;">👥 Author & Contact Information</h3>
  <div align="center">
    <b style="font-size: 16px; color: #991b1b;">Alyssa Mae T. De Guzman</b><br>
    <i>Lead Full-Stack Developer & Team Leader</i><br>
    Polytechnic University of the Philippines<br><br>

    <a href="https://linkedin.com/in/alyssa-mae-de-guzman">
      <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
    </a>
    <a href="https://github.com/alyssamaetdeguzman">
      <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
    </a>
    <a href="mailto:alyssamaetdeguzman@gmail.com">
      <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
    </a>
  </div>

</div>
