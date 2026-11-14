# Praashad Real Estate ERP — Frontend

The frontend application for Praashad Real Estate ERP. It is built with React and Vite and communicates with the Laravel backend through HTTP API requests.

## Technology Stack

- React 19
- Vite 7
- Tailwind CSS 4
- React Router 7
- Axios and Axios Retry
- Framer Motion
- Heroicons, Lucide React, and React Icons
- React Toastify
- Lodash and use-debounce

## Main Application Areas

The source tree includes the following pages and areas:

- **Dashboard**
- **Administration:** employee management
- **Developer / System Setup:** users, roles, ownership, and payment types
- **Real Estate:** projects, floors, blocks, units, customers, leads, procurement, sales, and installments
- **Rental:** rental management area

Shared UI components include the application header, sidebar, layout, and lead-related components.

## Requirements

- Node.js
- npm
- The Laravel backend running locally or at a configured API URL

## Installation

From the repository root, move into the frontend directory:

```bash
cd Praashad_real-state_erp_frontend
npm install
```

Create a `.env` file:

```bash
cp .env.example .env
```

Set the backend API base URL in `.env`:

```env
VITE_API_URL=http://127.0.0.1:8000/api
```

`VITE_API_URL` should point to the Laravel API base URL, including the `/api` prefix.

## Run Locally

```bash
npm run dev
```

Vite will show the local development address in the terminal.

## Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the development server |
| `npm run build` | Build the application for production |
| `npm run preview` | Preview the production build |
| `npm run lint` | Run ESLint |

## Backend Integration

The frontend uses Axios to communicate with the Laravel API. The API base URL is configured through the `VITE_API_URL` environment variable.

Example:

```env
VITE_API_URL=http://127.0.0.1:8000/api
```

Start the backend separately before using features that require API data. See the [backend README](../Praashad_real-state_erp_backend/README.md) for backend installation and database setup.

## Production Build

Create an optimized production build:

```bash
npm run build
```

The generated files are placed in the `dist/` directory. Deploy the contents of that directory to a static hosting service configured for a Vite single-page application.

## Environment Variables

| Variable | Purpose | Example |
|---|---|---|
| `VITE_API_URL` | Base URL of the Laravel API | `http://127.0.0.1:8000/api` |

Do not put private server credentials or secret API keys in frontend environment variables. Vite variables prefixed with `VITE_` are exposed to the client-side bundle.

## Project Structure

```text
Praashad_real-state_erp_frontend/
├── public/
├── src/
│   ├── components/
│   ├── data/
│   ├── pages/
│   │   ├── administration/
│   │   ├── developer/
│   │   └── real-estate/
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── .env.example
├── package.json
└── vite.config.js
```

## Screenshots

Add frontend screenshots here when available. For example:

```md
![ERP Dashboard](../docs/images/dashboard.png)
```
