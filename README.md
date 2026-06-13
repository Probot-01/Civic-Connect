# 🏙️ CivicConnect — SIH 2025

> A full-stack civic issue reporting and management platform built for **Smart India Hackathon 2025**.  
> Connecting citizens, municipal administrators, and field supervisors on a single unified platform.

---

## 📌 Overview

**CivicConnect** is a three-portal web application that streamlines civic issue reporting and resolution for Municipal Corporations. Citizens can report local problems (roads, sanitation, water, electricity) directly from their mobile browsers, while administrators and field supervisors track, assign, and resolve those issues in real time.

---

## 🧩 Project Structure

```
SIH2025_CivicConnect/
│
├── citizen/          # Citizen-facing PWA (mobile-first)
├── Admin_new/        # Municipal Admin dashboard
└── Overlooker/       # Field Supervisor / Overlooker portal
```

---

## 🌐 Portals

### 📱 Citizen Portal (`/citizen`)
A mobile-first progressive web app for citizens to:
- **Onboard** with guided introduction screens
- **Report issues** with photo capture (webcam/camera), category selection, and location pinning on an interactive map
- **Track** submitted reports and their resolution status
- **Receive notifications** on assignment, resolution, or reopening of issues
- **Explore** a city-wide issue heatmap and community feed
- **Manage** their profile

**Tech:** React 18 · TypeScript · Vite · TailwindCSS · Leaflet · MapLibre GL · Supabase · Framer Motion

---

### 🖥️ Admin Dashboard (`/Admin_new`)
A full-featured dashboard for **Municipal Corporation workers** to:
- **Issue Management** — Triage incoming reports across three tabs: *New Reports → Assigned → Resolved*
  - Filter by category (Roads, Sanitation, Water, Electricity) and ward
  - Auto-route issues to the right department with one click
  - Reassign or delete reports; escalated issues return with a badge
- **User Management** — View registered citizens (search by name/ID/phone), block users, and add Overlooker accounts
- **Analytics & Reports** — Ward-wise distribution charts, pie charts, department performance graphs
- **Special Boards** — Clustered reports and escalated issue boards

**Tech:** React 18 · TypeScript · Vite · TailwindCSS · Shadcn/UI · Radix UI · Recharts · Leaflet · React Query · Zod · React Hook Form

---

### 👁️ Overlooker Portal (`/Overlooker`)
A supervisor-facing dashboard for field personnel to:
- **View assigned issues** for their ward/zone
- **Track resolution progress** and upload confirmation images
- **Browse analytics** on their assigned area
- **Manage community** escalations
- Protected by JWT-based login (`civic_auth_token`)

**Tech:** React 18 · TypeScript · Vite · TailwindCSS · Shadcn/UI · Radix UI · Recharts · Framer Motion · React Query

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 18, TypeScript, Vite |
| Styling | TailwindCSS 3, Shadcn/UI, Radix UI |
| Maps | Leaflet, React-Leaflet, MapLibre GL |
| State / Data | TanStack React Query, React Hook Form |
| Animation | Framer Motion |
| Backend / DB | Supabase (citizen portal) |
| Validation | Zod |
| Charts | Recharts |

---

## 🚀 Getting Started

Each portal is an independent Vite + React app. Navigate into any portal directory and run:

```bash
# Install dependencies
npm install

# Start the development server
npm run dev
```

### Ports (default Vite)
| Portal | Default URL |
|---|---|
| Citizen | http://localhost:5173 |
| Admin | http://localhost:5174 |
| Overlooker | http://localhost:5175 |

> **Note:** Supabase environment variables are required for the Citizen portal. Create a `.env` file in `/citizen` with your Supabase project URL and anon key.

```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

---

## 📂 Key Features

- 📍 **Real-time issue mapping** with Leaflet and MapLibre GL
- 📷 **In-browser photo capture** for issue evidence
- 🔁 **Auto-routing engine** to assign issues to relevant departments
- 📊 **Ward-wise analytics** with interactive charts and graphs
- 🔔 **Notification system** for status updates (assigned, resolved, deleted, reopened)
- 🏷️ **Escalation flow** — Reopened issues surface with an "Escalated" tag
- 🔐 **Protected routes** with token-based auth for Admin and Overlooker portals
- 📱 **Mobile-first** citizen portal with bottom navigation

---

## 🤝 Team

Built for **Smart India Hackathon 2025** 🇮🇳

---

## 📄 License

This project was developed for a national hackathon. All rights reserved.
