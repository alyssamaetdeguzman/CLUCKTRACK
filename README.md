# CluckTrack 🐔📊
Web-based Real-time Inventory & Production Analytics System (Agricultural ERP)

Transitioning local poultry farming operations from manual records and fragmented spreadsheets into a centralized, data-driven digital pipeline.

🌟 Overview
CluckTrack is a comprehensive, web-based Agricultural ERP designed to streamline poultry farm management. Built as an academic capstone project, it replaces error-prone paper ledgers and disconnected spreadsheets with a real-time dashboard. The system tracks dynamic inventory, monitors daily production metrics, and leverages predictive analytics to generate actionable profitability reports for farm operators.

🚀 Key Features
📦 Dynamic CRUD Inventory Module: Real-time tracking of feed, livestock, mortality rates, and supplies with automated low-stock notifications.

📈 Production & Profitability Analytics: Interactive charts powered by Chart.js to visualize Key Performance Indicators (KPIs) like feed conversion ratios (FCR) and egg/meat yields.

🔮 Strategic Forecasting Engine: Predictive data processing to assist managers in planning stock replenishment and assessing cycle profitability.

🔒 Role-Based Access Control (RBAC): Secure permission layers for farm administrators, supervisors, and standard staff.

📝 Comprehensive Audit Trail: System activity logs ensuring complete transparency, accountability, and data governance across operations.

🛠️ Tech Stack
Backend & Logic: PHP, Python (Analytics & Forecasting Engine)

Frontend: HTML5, Tailwind CSS, JavaScript, Chart.js

Database: MySQL

Server Environment / Tools: Apache, Linux/XAMPP, Git & GitHub, Railway (Deployment)

📂 Project Structure
Plaintext
clucktrack/
├── assets/             # Images, custom CSS, and client-side scripts
├── config/             # Database connection and environment configurations
├── includes/           # Reusable components (Navbar, Sidebar, Footer, RBAC checks)
├── modules/            # Core feature modules (Inventory, Production, Analytics, Audit Logs)
├── python_engine/      # Python scripts for predictive forecasting and data processing
├── database/           # SQL schema definitions and migration scripts
├── index.php           # Application entry point / Login redirect
└── dashboard.php       # Main analytics control center
⚙️ Getting Started
Prerequisites
XAMPP (or a local LAMP/WAMP server stack with PHP 8.x and MySQL)

Python 3.x (for analytics and forecasting modules)

Composer (optional, for dependency management)

Installation & Setup
Clone the repository:

Bash
git clone https://github.com/alyssamaetdeguzman/clucktrack.git
Move to your local server directory:

Place the cloned folder into your htdocs directory (if using XAMPP).

Configure the Database:

Open phpMyAdmin and create a new database named clucktrack_db.

Import the schema file located in database/schema.sql.

Update Database Credentials:

Open config/db.php and update your database host, username, and password if necessary:

PHP
$host = 'localhost';
$db   = 'clucktrack_db';
$user = 'root';
$pass = '';
Run the Application:

Start Apache and MySQL from your XAMPP control panel.

Open your browser and navigate to: http://localhost/clucktrack

👥 Author
Alyssa Mae T. De Guzman – Lead Full-Stack Developer & Team Leader

Polytechnic University of the Philippines
