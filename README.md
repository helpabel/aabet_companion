# aabet_companion
Nursing Quality Improvement - companion App (MAUI + Suprabase)
# AaBET — Nursing Quality Improvement Companion App

A private companion mobile app for the **AaBET Nursing Quality Assessment System** —
a hospital-wide auditing tool used to score nursing and physician documentation
quality against approved questionnaire standards.

## Purpose

AaBET replaces manual, paper-based nursing quality audits with a structured
digital workflow:

- Daily/evening shift scheduling
- Per-unit assessment entry (VS, MED, HODA, NCP, ICU, TRIAGE, PACU, OPD, PHYS)
- Automatic Ethiopian-calendar monthly & rolling 3-month analytics
- Word/Excel-ready export with MRN subheadings
- Role-based access (Admin, Quality Inspector, Nurse, Physician, Supervisor)

## Tech Stack

| Layer | Technology |
|---|---|
| Backend  | Supabase (PostgreSQL 15+) |
| Auth     | Supabase Auth + custom `auth_user_map` |
| Mobile   | .NET 10 MAUI |
| UI       | Syncfusion MAUI controls (Community License) |
| Realtime | Supabase Realtime |

## Repository Layout

- `/database` — full PostgreSQL / Supabase schema (idempotent, single-file migration)
- `/src/AaBET.Companion` — .NET 10 MAUI app
- `/docs` — screenshots, architecture notes

## Status

🚧 **Active development** — schema finalized (v6.3), mobile app in early build.

## License

Application code: MIT.  
Database schema: MIT.  
Syncfusion components: used under the Syncfusion Community License.
