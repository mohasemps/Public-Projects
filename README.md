Gulu NGO Donation Tracker




## 📌 Overview

The **Gulu NGO Donation Tracker** is a full-stack enterprise-ready donation management platform designed to support NGOs in managing donors, projects, and contributions with transparency, accountability, and efficiency.

It combines a **Flask backend**, **SQLite relational database**, and a **modern dashboard UI** to deliver real-time tracking and reporting.

---

## 🧭 System Architecture

```
┌───────────────────────┐
│     Web Dashboard     │
│  (HTML/CSS/JS UI)     │
└─────────┬─────────────┘
          │ REST APIs
┌─────────▼─────────────┐
│     Flask Backend     │
│  Authentication + API │
└─────────┬─────────────┘
          │ ORM (SQLAlchemy)
┌─────────▼─────────────┐
│     SQLite DB         │
│  Users, Donors,       │
│  Projects, Donations  │
└───────────────────────┘
```
 Core Features

 Authentication & Authorization
- JWT-based authentication
- Role-based access control (RBAC)
- Secure cookie/session handling

👤 Donor Management
- Register, update, and list donors
- Support for individuals, corporate, and foundations
- Active status management

📋 Project Management
- Create and monitor projects
- Set goals and timelines
- Automatic funding updates

💰 Donation Tracking
- Record donations with full metadata
- Multi-currency support
- Anonymous donations
- Auto-generated receipt numbers

📊 Reporting & Analytics
- Overall system statistics
- Project-level reports
- Donor contribution summaries

 Web Dashboard
- Responsive modern interface
- Tab-based navigation
- Dynamic API-driven updates

---

 🧱 Data Model

Tables

User: Authentication and roles
Donor: Donor identity info
Project: NGO initiatives
Donation: Financial/in-kind contributions

### Relationships

- Donor → Donations (1:N)
- Project → Donations (1:N)

---

## ⚙️ Installation

```bash
python app.py
```

Dependencies auto-install via script.

---

🌐 Access

- Local: http://localhost:8000
- Colab: auto-generated proxy URL

---

🔑 Default Credentials

| Role | Username | Password |
|------|----------|----------|
| Admin | Admin | Nebraska@2014 |
| Finance | Finance | Nebraska@2014 |
| Viewer | Viewer | Nebraska@2014 |

---

 🔌 API Reference

 Authentication
- GET /api/me

 Donors
- GET /api/donors
- POST /api/donors

 Projects
- GET /api/projects
- POST /api/projects

 Donations
- GET /api/donations
- POST /api/donations
- GET /api/donations/recent

Reports
- GET /api/reports/overall
- GET /api/reports/project/{id}

 Users (Admin)
- GET /api/users
- POST /api/users
- PUT /api/users/{id}/role

---

🔒 Security Design

- Password hashing (PBKDF2 + salt)
- JWT token expiration (7 days)
- Role-based access control
- Input validation

---

📦 Deployment

### Local Deployment
```bash
python app.py
```

 Google Colab Deployment
- Run notebook
- Click generated link

 Azure Deployment (Recommended)
- Use Azure App Service
- Replace SQLite with PostgreSQL
- Use environment variables for secrets

---

⚠️ Production Hardening

- Replace SECRET_KEY
- Enable HTTPS (secure cookies)
- Use PostgreSQL/MySQL
- Add logging and monitoring
- Setup backups
- Add rate limiting

---

⚡ Advanced Enhancements (Future)

- Mobile Money Integration (MTN, Airtel)
- AI Analytics Dashboard
- Export to Excel/PDF
- Multi-branch NGO support
- Audit trails

---

📍 Use Cases

- NGO fundraising and tracking
- Transparency dashboards
- Donor reporting systems
- Community aid projects

---

Status

Production Ready – Final Stable Release (2026)

---

 📜 License

MIT License

---

 🙌 Acknowledgment

Built to support transparent and efficient humanitarian work in Uganda and beyond.
