# AaBET — Nursing Quality Improvement Companion App

A personal, self-motivated mobile app I am building on my own time to explore how structured digital auditing could improve nursing quality documentation in hospital settings. Not assigned, not commissioned, and not yet deployed or endorsed by any institution.

> **Status:** 🚧 Active personal project — mobile app in early build.
> Not yet deployed or endorsed by any institution.

---

## Why this exists

I work in a hospital setting and observed a recurring problem:

- Nursing quality audits are still done on paper checklists.
- Scoring is manual, error-prone, and time-consuming.
- Cross-unit comparison and trend analysis are practically impossible.
- Ethiopian-calendar monthly reporting is done by hand.

I couldn't find an existing tool that matched how audits actually work on the
floor — so I'm building one. This is my own project, built on my own time.

---

## Purpose

AaBET replaces manual, paper-based nursing quality audits with a structured
digital workflow:

- Daily / evening shift scheduling (max two units per shift)
- Per-unit assessment entry across sections:
  **VS, MED, HODA, NCP, ICU, TRIAGE, PACU, OPD, PHYS**
- Automatic **Ethiopian-calendar** monthly and rolling 3-month analytics
- Word / Excel-ready export with anonymized MRN subheadings
- Role-based access — Admin, Quality Inspector, Nurse, Physician, Supervisor
- 24-hour correction window on submitted reports, then locked
- FirstLook full-screen reader with share, copy, and print actions

---

## Tech Stack

| Layer     | Technology                                  |
|-----------|---------------------------------------------|
| Mobile    | .NET 10 MAUI                                |
| UI        | Syncfusion MAUI controls (Community License)|
| Backend   | Supabase (PostgreSQL 15+) — private         |
| Auth      | Supabase Auth + custom `auth_user_map`      |
| Realtime  | Supabase Realtime (planned)                 |

---

## Backend

The companion app connects to a **Supabase (PostgreSQL)** backend for
authentication, data storage, real-time sync, and reporting.

The database schema, RLS policies, and SQL functions are kept in a
**private repository** and are not included here.

- Auth — Supabase Auth with a custom `auth_user_map` link table
- Data — PostgreSQL 15+ with Row Level Security
- Analytics — Ethiopian-calendar monthly and rolling 3-month aggregations
- Realtime — Supabase Realtime (planned for chat / notifications)

---

## Repository Structure

```
aabet-companion/
├── README.md
├── LICENSE
├── .gitignore
├── src/
│   └── AaBET.Companion/
└── docs/
    └── screenshots/
        └── login.png
```

- `src/` — the .NET 10 MAUI companion app
- `docs/` — screenshots and project documentation

---

## Screenshots

### Login

![AaBET login page with Welcome to greeting, DevExpress Report logo, and quality-improvement marquee](docs/screenshots/login.png)

The login screen is designed for clarity and quick sign-in on mobile:

- A soft **"Welcome to"** greeting above the **DEVEXPRESS REPORT** logo,
  centered and wide.
- Username / password fields with an inline show-hide password toggle.
- "Remember me" and "Forgot password?" options.
- A prominent **Sign In** action leading to Supabase authentication.
- A continuous right-to-left marquee reading
  *"AaBET Nursing Quality Improvement: Auditing for Excellence."* —
  placed at the bottom of the page.

---

## Status

| Component                  | State                                   |
|----------------------------|-----------------------------------------|
| PostgreSQL schema (v6.3)   | ✅ Complete, tested on Supabase (private)|
| Supabase RLS + functions   | ✅ Complete (private)                   |
| MAUI app — Login           | ✅ Working                              |
| MAUI app — Data Export     | ✅ Working (FirstLook + share / copy)   |
| MAUI app — Dashboard       | 🚧 In progress                          |
| MAUI app — Assessment      | 🚧 In progress                          |
| MAUI app — Reports         | 🚧 Planned                              |
| Deployment                 | ⏳ Not yet                              |

---

## A note on scope

This project is intentionally **personal and non-commercial right now**.
I'm building it to learn, to solve a real problem I see every day, and — if it
proves useful — to eventually offer it for free to public hospitals in
Ethiopia.

If any institution adopts it later, that decision will be made then. For now,
this repository is my own work in progress.

---

## License

Application code in this repository: **MIT**.

Syncfusion MAUI components are used under the
**Syncfusion Community License**.

---

## Author

*[Abel Tefera Gebremichael]* — nurse / developer.

Found a bug, or want to chat? Open an issue.
