<!-- Top Navigation Bar -->
<header class="bg-slate-800 border-b border-slate-700 px-6 py-4 flex items-center justify-between shrink-0">
    <div class="flex items-center space-x-3">
        <div class="bg-amber-500 text-slate-900 p-2 rounded-lg font-bold flex items-center justify-center shadow-lg shadow-amber-500/20">
            <i class="fa-solid fa-feather text-xl"></i>
        </div>
        <div>
            <h1 class="text-lg font-bold tracking-tight text-white flex items-center gap-2">
                CluckTrack <span class="text-xs px-2 py-0.5 rounded-full bg-amber-500/10 text-amber-400 border border-amber-500/20 font-medium">README.md Studio</span>
            </h1>
            <p class="text-xs text-slate-400">Interactive GitHub Documentation Editor & Previewer</p>
        </div>
    </div>
    
    <div class="flex items-center space-x-3">
        <button id="tab-write" onclick="switchTab('write')" class="px-4 py-2 text-sm font-medium rounded-lg bg-slate-700 text-white transition flex items-center gap-2">
            <i class="fa-solid fa-code"></i> Edit Code
        </button>
        <button id="tab-preview" onclick="switchTab('preview')" class="px-4 py-2 text-sm font-medium rounded-lg text-slate-400 hover:text-white transition flex items-center gap-2">
            <i class="fa-solid fa-eye"></i> Live Preview
        </button>
        <div class="h-5 w-px bg-slate-700 mx-1"></div>
        <button onclick="copyReadme()" class="bg-emerald-600 hover:bg-emerald-500 text-white px-4 py-2 rounded-lg text-sm font-semibold transition flex items-center gap-2 shadow-lg shadow-emerald-600/20">
            <i class="fa-solid fa-copy"></i> Copy Markdown
        </button>
    </div>
</header>

<!-- Main Workspace Container -->
<main class="flex-1 overflow-hidden flex flex-col md:flex-row relative">
    
    <!-- Editor View -->
    <div id="editor-container" class="flex-1 flex flex-col h-full p-4 md:p-6 bg-slate-900 overflow-hidden">
        <div class="flex items-center justify-between mb-3 shrink-0">
            <span class="text-xs font-semibold uppercase tracking-wider text-slate-400 flex items-center gap-2">
                <i class="fa-brands fa-markdown text-amber-400"></i> README.md Source Code
            </span>
            <span id="char-count" class="text-xs text-slate-500">0 characters</span>
        </div>
        <div class="flex-1 rounded-xl border border-slate-700 bg-slate-950 overflow-hidden shadow-inner flex flex-col">
            <textarea id="markdown-input" oninput="updatePreview()" class="w-full h-full p-5 bg-transparent text-slate-200 font-mono text-sm resize-none focus:outline-none leading-relaxed selection:bg-amber-500/30"></textarea>
        </div>
    </div>

    <!-- Preview View -->
    <div id="preview-container" class="hidden flex-1 flex flex-col h-full p-4 md:p-6 bg-slate-900 overflow-hidden">
        <div class="flex items-center justify-between mb-3 shrink-0">
            <span class="text-xs font-semibold uppercase tracking-wider text-slate-400 flex items-center gap-2">
                <i class="fa-solid fa-globe text-emerald-400"></i> GitHub Rendered Preview
            </span>
            <span class="text-xs text-slate-500">Theme: GitHub Dark</span>
        </div>
        <div class="flex-1 rounded-xl border border-slate-700 bg-[#0d1117] text-[#c9d1d9] p-6 overflow-y-auto shadow-inner prose prose-invert max-w-none">
            <div id="markdown-preview"></div>
        </div>
    </div>

</main>

<!-- Notification Toast -->
<div id="toast" class="fixed bottom-6 right-6 bg-emerald-600 text-white px-4 py-3 rounded-xl shadow-2xl flex items-center space-x-3 transform translate-y-20 opacity-0 transition-all duration-300 z-50">
    <i class="fa-solid fa-circle-check text-lg"></i>
    <span class="text-sm font-medium">README markdown copied to clipboard successfully!</span>
</div>

<!-- Application Script Logic -->
<script>
    const initialReadme = `# CluckTrack 🐔📊


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

```text
clucktrack/
├── assets/             # Images, custom CSS, and client-side scripts
├── config/             # Database connection and environment configurations
├── includes/           # Reusable components (Navbar, Sidebar, Footer, RBAC checks)
├── modules/            # Core feature modules (Inventory, Production, Analytics, Audit Logs)
├── python_engine/      # Python scripts for predictive forecasting and data processing
├── database/           # SQL schema definitions and migration scripts
├── index.php           # Application entry point / Login redirect
└── dashboard.php       # Main analytics control center
```

⚙️ Getting Started

Prerequisites

XAMPP (or a local LAMP/WAMP server stack with PHP 8.x and MySQL)

Python 3.x (for analytics and forecasting modules)

Composer (optional, for dependency management)

Installation & Setup

Clone the repository:
```bash
git clone https://github.com/alyssamaetdeguzman/clucktrack.git
```

Move to your local server directory:

Place the cloned folder into your `htdocs` directory (if using XAMPP).

Configure the Database:

Open phpMyAdmin and create a new database named `clucktrack_db`.

Import the schema file located in `database/schema.sql`.

Update Database Credentials:

Open `config/db.php` and update your database host, username, and password if necessary:
```php
$host = 'localhost';$db   = 'clucktrack_db';
$user = 'root';$pass = '';
```

Run the Application:

Start Apache and MySQL from your XAMPP control panel.

Open your browser and navigate to: `http://localhost/clucktrack`

👥 Author

Alyssa Mae T. De Guzman – Lead Full-Stack Developer & Team Leader

Polytechnic University of the Philippines`;

  // Initialize textarea value on load
  const inputField = document.getElementById('markdown-input');
  inputField.value = initialReadme;
  updatePreview();

  function switchTab(tab) {
      const editorContainer = document.getElementById('editor-container');
      const previewContainer = document.getElementById('preview-container');
      const tabWrite = document.getElementById('tab-write');
      const tabPreview = document.getElementById('tab-preview');

      if (tab === 'write') {
          editorContainer.classList.remove('hidden');
          previewContainer.classList.add('hidden');
          tabWrite.className = "px-4 py-2 text-sm font-medium rounded-lg bg-slate-700 text-white transition flex items-center gap-2";
          tabPreview.className = "px-4 py-2 text-sm font-medium rounded-lg text-slate-400 hover:text-white transition flex items-center gap-2";
      } else {
          editorContainer.classList.add('hidden');
          previewContainer.classList.remove('hidden');
          tabPreview.className = "px-4 py-2 text-sm font-medium rounded-lg bg-slate-700 text-white transition flex items-center gap-2";
          tabWrite.className = "px-4 py-2 text-sm font-medium rounded-lg text-slate-400 hover:text-white transition flex items-center gap-2";
          updatePreview();
      }
  }

  function updatePreview() {
      const content = inputField.value;
      document.getElementById('char-count').innerText = `${content.length} characters`;
      document.getElementById('markdown-preview').innerHTML = marked.parse(content);
  }

  function copyReadme() {
      navigator.clipboard.writeText(inputField.value).then(() => {
          const toast = document.getElementById('toast');
          toast.classList.remove('translate-y-20', 'opacity-0');
          setTimeout(() => {
              toast.classList.add('translate-y-20', 'opacity-0');
          }, 3000);
      });
  }
