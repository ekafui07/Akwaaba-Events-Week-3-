# Akwaaba — Event Management Platform (Frontend)

A full-featured event management platform built for organizers to manage events, tickets, attendees, analytics and notifications all from a single platform.

---

## Description

My role on the team was a **Frontend Developer**. The goal was to take provided UI mockups and translate them into fully working, interactive React pages. 

---

## Why

The team needed a polished frontend that stakeholders and backend developers could interact with during development. Rather than handing over static mockups, a fully working coded version:

- Gives the backend team a **clear picture of the data shapes** each page needs
- Allows **early user testing** before APIs are connected
- Serves as a **living reference** for the final design system across all pages

---

## Pages Implemented

| Page | Route | Description |
|---|---|---|
| Landing | `/` | Public marketing page with hero, features, and call-to-action |
| Login | `/login` | Split-screen login with branding panel and form |
| Dashboard | `/dashboard` | KPI stat cards, event activity table, and status breakdown |
| Analytics | `/analytics` | Revenue chart, KPI sparkbars, traffic sources, attendance rate |
| Browse Events | `/browse` | Public event listing with live search and category filters |
| Reports | `/reports` | Report templates, recent reports log, and scheduled reports |
| Register Tickets | `/register-tickets` | VIP, Standard, and Free ticket type configuration |
| QR Codes | `/tickets` | QR code directory with revoke, delete, and quick generator |
| Notifications | `/notifications` | Event log feed with tab filters and preference settings panel |
| Profile & Settings | `/settings` | 5-tab profile page: Personal Info, Security, Organization, Preferences, Billing |

---

## Screenshots

Below are screenshots demonstrating the live implementation of the Akwaaba platform user interface across key routes:

| Dashboard | Analytics |
|---|---|
| ![Dashboard](./public/screenshots/dashboard.png) | ![Analytics](./public/screenshots/analytics.png) |

| Login | Notifications |
|---|---|
| ![Login](./public/screenshots/login.png) | ![Notifications](./public/screenshots/notifications.png) |

| Browse Events | Register Digital Tickets |
|---|---|
| ![Browse Events](./public/screenshots/browse.png) | ![Register Tickets](./public/screenshots/register_tickets.png) |

| QR Codes Management | Administrative Reports |
|---|---|
| ![QR Codes](./public/screenshots/qr_codes.png) | ![Reports](./public/screenshots/reports.png) |

| Profile & Settings | Public Landing |
|---|---|
| ![Settings](./public/screenshots/settings.png) | ![Landing](./public/screenshots/landing.png) |

---

## Architecture

```
Frontend/
├── public/
│   ├── hero_event_hall.png         # Landing page hero image
│   └── screenshots/                # Application UI screenshots
│       ├── landing.png
│       ├── login.png
│       ├── dashboard.png
│       ├── analytics.png
│       ├── browse.png
│       ├── reports.png
│       ├── register_tickets.png
│       ├── qr_codes.png
│       ├── notifications.png
│       └── settings.png
├── src/
│   ├── Akwaaba/
│   │   ├── Icons.jsx               # Shared SVG icon components
│   │   ├── Layout.jsx              # Sidebar navigation and app shell
│   │   ├── Badges.jsx              # Status badge components
│   │   └── ProtectedRoute.jsx      # Auth guard for private routes
│   ├── akwaabapages/
│   │   ├── Landing.jsx
│   │   ├── Login.jsx
│   │   ├── Dashboard.jsx
│   │   ├── Analytics.jsx
│   │   ├── BrowseEvents.jsx
│   │   ├── Reports.jsx
│   │   ├── RegisterTickets.jsx
│   │   ├── QRCodes.jsx
│   │   ├── Notifications.jsx
│   │   └── Settings.jsx
│   ├── features/
│   │   └── dashboard/
│   │       └── dashboardSlice.js   # Redux slice for dashboard state
│   ├── lib/
│   │   └── auth.jsx                # Supabase authentication context
│   ├── App.jsx                     # Route definitions
│   ├── main.jsx                    # App entry point
│   └── styles.css                  # Global design tokens and shared classes
└── index.html                      # Google Fonts (Plus Jakarta Sans) loaded here
```

---

## API Integration Notes

All pages currently use static mock data. When backend endpoints are ready, the following pages will need to be connected:

| Page | Data Required |
|---|---|
| Dashboard | Events list, submission counts, participant counts |
| Analytics | Revenue totals, ticket sales, conversion rates by period |
| Browse Events | Public events list with filtering support |
| Notifications | Real-time notification feed (WebSocket or SSE recommended) |
| QR Codes | Attendee QR records with revoke/delete endpoints |
| Register Tickets | Ticket type CRUD, sales summary data |
| Reports | Report generation triggers, scheduled report list |
| Settings/Profile | User profile read/update, billing plan data |

---

## Tech Stack

| Tool | Purpose |
|---|---|
| React 18 | UI framework |
| Vite | Build tool and dev server |
| React Router v6 | Client-side routing |
| Redux Toolkit | Global state management |
| Vanilla CSS + Inline Styles | Styling |

---

## Branch

This work lives on the `edwin-ui/finished` branch.
Pull Request: [View on GitHub](https://github.com/Wild-Technological-Services/eventcloud/pull/new/edwin-ui/finished)

---

## Author

**Edwin Kafui** — Frontend Developer, Week 3
Wild Technological Services · Akwaaba Project Team
