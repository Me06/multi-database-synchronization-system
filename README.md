# multi-database-synchronization-system
A real-time and scheduled multi-database synchronization system with automatic conflict detection, resolution, visualization, and email notifications.
📌 Overview

The Multi-Database Synchronization System is designed to synchronize data across heterogeneous databases while ensuring data consistency, integrity, and availability.
It supports real-time synchronization, conflict detection, admin management, and interactive dashboards, making it suitable for both academic research and practical enterprise scenarios.

✨ Features

Multi-Database Support

SQLite (Primary)

MySQL (Simulated)

PostgreSQL (Simulated)

Synchronization Modes

Real-time synchronization

Scheduled synchronization

Manual synchronization trigger

Conflict Management

Automatic conflict detection

Web-based conflict resolution

Email alerts for detected conflicts

User & Admin Management

Role-based access control

Secure authentication and authorization

Data Visualization

Interactive dashboards

Synchronization metrics and charts

Conflict trend analysis

Advanced Query Tool

Multi-table SQL queries

Nested subqueries

Query optimization support

🛠 System Requirements

Python 3.8+

Flask Web Framework

SQLite3 (included with Python)

Modern web browser (Chrome / Firefox / Edge)

📂 Project Structure
MULTI-DB-PROJECT/
├── app/
│   ├── templates/
│   │   ├── index.html           -- Home page
│   │   ├── dashboard.html       -- Charts & metrics dashboard
│   │   ├── query.html           -- SQL query tool
│   │   ├── conflicts.html       -- Conflict resolution UI
│   │   ├── admin.html           -- Admin panel
│   │   ├── login.html           -- Login page
│   │   └── register.html        -- Registration page
│   ├── static/
│   │   ├── css/
│   │   │   └── style.css        -- Custom styles
│   │   └── js/
│   │       └── main.js          -- Frontend logic
│   ├── __init__.py              -- Flask app factory
│   ├── routes.py                -- Main routes & APIs
│   ├── models.py                -- Database models
│   ├── auth.py                  -- Authentication module
│   ├── admin.py                 -- Admin features
│   ├── syncer.py                -- Synchronization engine
│   ├── detector.py              -- Conflict detector
│   ├── emailer.py               -- Email notification service
│   └── config.py                -- Configuration file
├── run.py                       -- Application entry point
├── start_system.py              -- System initialization
├── init_db.py                   -- Database initialization
├── requirements.txt             -- Python dependencies
├── primary.db                   -- Primary SQLite database
├── mysql_sim.db                 -- MySQL simulation database
├── postgres_sim.db              -- PostgreSQL simulation database
└── README.md                    -- Project documentation

🗄 Database Schema

The system is built around the following core tables:

users — user accounts and roles

books — book information

authors — author details

sections — library sections/categories

borrow_records — borrowing history

data_conflicts — detected synchronization conflicts

The schema follows 1NF → 3NF (BCNF) normalization standards.

🔄 Synchronization Features
1️⃣ Real-Time Synchronization

Data changes are propagated instantly across databases.

2️⃣ Scheduled Synchronization

Automatic sync at configurable intervals.

3️⃣ Manual Synchronization

Triggered directly from the web dashboard.

⚠️ Conflict Detection & Resolution

Automatic detection of data inconsistencies

Conflict logging with timestamps and sources

Email notifications sent to administrators

Web-based interface for resolving conflicts

📊 Data Visualization

Synchronization performance metrics

Conflict frequency analysis

Database status monitoring

🧪 Testing Summary

Real-time Sync — Pass (≤ 1 second)

Conflict Detection — Pass (7 conflicts detected)

Email Notification — Pass

Web Interface — Pass

Mobile Access — Pass (Responsive design)

🔌 API Endpoints
GET  /api/sync-status           -- Get synchronization status
POST /api/run-query             -- Execute SQL query
GET  /api/get-conflicts         -- Retrieve conflicts
POST /api/resolve-conflict      -- Resolve conflict
GET  /api/sync-metrics          -- Sync performance metrics
POST /api/trigger-manual-sync   -- Manual synchronization

🚀 Installation & Usage
1️⃣ Clone the Repository
git clone <repository-url>
cd MULTI-DB-PROJECT

2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Initialize Database
python init_db.py

4️⃣ Start the System
python start_system.py


or

python run.py

## 🎯 Conclusion

This project demonstrates a robust, scalable, and normalized multi-database synchronization system.
It integrates real-time data sync, conflict management, visual dashboards, and secure access control, making it suitable for academic evaluation and real-world applications.

📈 Future Enhancements

Support for MongoDB and Redis

AI-assisted conflict resolution

Distributed architecture for scalability

Native mobile applications (iOS / Android)

Advanced performance monitoring dashboards

📄 License

This project is intended for educational and research purposes.
