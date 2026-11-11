# Praashad Real Estate ERP

A full-stack Real Estate Enterprise Resource Planning (ERP) application. The project contains a React-based frontend and a Laravel REST API backend.

## Technology Stack

### Frontend
- React 19
- Vite 7
- Tailwind CSS 4
- React Router
- Axios
- Framer Motion

### Backend
- PHP 8.1+
- Laravel 10
- MySQL
- Laravel Sanctum
- Cloudinary Laravel integration

## Project Structure

```text
Praashad_real-state_erp/
│
├── Praashad_real-state_erp_frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── .env.example
│
├── Praashad_real-state_erp_backend/
│   ├── app/
│   ├── bootstrap/
│   ├── config/
│   ├── database/
│   ├── public/
│   ├── routes/
│   ├── storage/
│   ├── composer.json
│   └── .env.example
│
├── .gitignore
└── README.md
```

## Requirements

Install the following tools before running the project:

- PHP 8.1 or later
- Composer
- MySQL
- Node.js and npm

## Installation and Setup

### 1. Clone the Repository

```bash
git clone YOUR_REPOSITORY_URL
cd Praashad_real-state_erp
```

Replace `YOUR_REPOSITORY_URL` with the actual GitHub repository URL.

### 2. Backend Setup

Open a terminal in the backend directory:

```bash
cd Praashad_real-state_erp_backend
```

Install PHP dependencies:

```bash
composer install
```

Create the environment file:

```bash
cp .env.example .env
```

Generate the Laravel application key:

```bash
php artisan key:generate
```

Create a MySQL database and update the database settings in the backend `.env` file:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=Prashad_ERP_db
DB_USERNAME=root
DB_PASSWORD=
```

Run database migrations:

```bash
php artisan migrate
```

Configure Cloudinary credentials in `.env` if the application uses Cloudinary uploads:

```env
CLOUDINARY_URL=
CLOUDINARY_UPLOAD_PRESET=
```

Start the Laravel development server:

```bash
php artisan serve
```

The backend API will normally be available at:

`http://127.0.0.1:8000/api`

### 3. Frontend Setup

Open another terminal in the frontend directory:

```bash
cd Praashad_real-state_erp_frontend
```

Install JavaScript dependencies:

```bash
npm install
```

Create a `.env` file in the frontend directory and set the backend API URL:

```env
VITE_API_URL=http://127.0.0.1:8000/api
```

Start the frontend development server:

```bash
npm run dev
```

Vite will display the local development URL in the terminal.

## Available Frontend Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the development server |
| `npm run build` | Build the frontend for production |
| `npm run preview` | Preview the production build |
| `npm run lint` | Run ESLint checks |

## Important Notes

- The frontend and backend must both be running for the application to work locally.
- Configure the database and required third-party services before using related features.
- Do not commit `.env` files, passwords, API keys, or other private credentials.
- User-uploaded files and runtime data are excluded from this repository.
- The repository does not include `node_modules` or `vendor`; install dependencies using npm and Composer.

## License

No license has been specified for this repository yet.
