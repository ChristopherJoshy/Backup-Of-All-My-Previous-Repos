# 🌐 IEEE SB CEK Society Website Design Competition — SIGHT Affinity Group

A responsive and content-driven website built for the **IEEE Student Branch CEK Society Website Design Competition**, targeting the **IEEE SIGHT Affinity Group**.
The site implements all required sections — **Home, About, Execom Members, Activities, Achievements, and Contact** — with a modern tech stack and clean UI.

🔗 **Live Demo:** [sightwebdesigncompbychris.up.railway.app](https://sightwebdesigncompbychris.up.railway.app)

---

## Team Details

* **Name** : neural_Nomads
* **Members** : Christopher Joshy

## 🚀 Tech Stack

* **Frontend:** React 18 + TypeScript, Vite
* **Styling/UI:** Tailwind CSS, Radix UI primitives
* **Routing:** Wouter
* **Data fetching:** TanStack Query
* **Backend/Server:** Express (Vite middleware for dev, static build for prod)

---

## ✨ Features

* **Navigation:** Persistent navbar linking all key sections
* **Home:** Hero banner with logo/name, intro text, CTAs, animated stats
* **About:** Dual section overview (local chapter + IEEE SIGHT global) with imagery
* **Execom Members:** Responsive card layout with placeholders for member details
* **Activities:** Event cards with title, photo, description, status (past/upcoming)
* **Achievements:** Card grid with title, optional photo, description, date/year
* **Contact:** Email, phone, and placeholders for socials/location
* **Responsive Design:** Consistent typography, colors, and subtle animations
* **Customizable:** Content and branding fully editable via JSON and theme files

---

## 📂 Project Structure

```bash
.
├── client/        # React app (pages, components, styles)
│   ├── src/data   # JSON content (members, events, etc.)
│   └── src/components/ui  # Shared UI components
├── server/        # Express entry point & Vite dev integration
├── shared/        # Shared types & schemas
├── Assets/        # Static assets (logos, images, etc.)
```

---

## 🛠 Getting Started

### Prerequisites

* **Node.js** 18+ recommended

### Installation & Development

```bash
npm install
npm run dev
```

The server runs on **[http://localhost:5000](http://localhost:5000)** by default.

### Production Build

```bash
npm run build
npm start
```

This serves the prebuilt client (`dist/public`) via the Express server.

---

## 🎨 Customization

* Update branding (logo, colors) in Tailwind/theme config and `Assets/`
* Edit content in `client/src/data/*.json`
* Extend components under `client/src/components` and pages under `client/src/pages`

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙌 Credits

Built by **[Christopher Joshy](https://github.com/ChristopherJoshy)**
For the **IEEE SB CEK Society Website Design Competition** (SIGHT Affinity Group)
