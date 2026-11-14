# Praashad Real Estate ERP — Backend

The backend API for Praashad Real Estate ERP. It is built with Laravel 10 and PHP and uses MySQL for data storage.

## Technology Stack

- PHP 8.1+
- Laravel 10
- MySQL
- Laravel Sanctum
- Cloudinary Laravel integration
- Composer

## Main Backend Areas

The API contains controllers and models for:

- User and role management
- Ownership records
- Leads and customers
- Employees, payroll, and payroll summaries
- Projects, floors, blocks, and units
- Procurement, sales, and installments
- Expense categories and expenses
- Payment types and incentives
- Transactions and additional charges
- Rental projects, blocks, floors, units, leads, ownerships, tenants, and installments
- Project hierarchy queries

## Requirements

- PHP 8.1 or later
- Composer
- MySQL
- PHP extensions required by Laravel 10 and the installed Composer packages

## Installation

From the repository root:

```bash
cd Praashad_real-state_erp_backend
composer install
```

Create the environment file:

```bash
cp .env.example .env
```

Generate the application key:

```bash
php artisan key:generate
```

## Database Configuration

Create a MySQL database. The supplied `.env.example` uses `Prashad_ERP_db` as the database name.

Update the database values in `.env` to match your local MySQL configuration:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=Prashad_ERP_db
DB_USERNAME=root
DB_PASSWORD=
```

Run migrations:

```bash
php artisan migrate
```

## Start the API Server

```bash
php artisan serve
```

By default, the Laravel development server runs at:

```text
http://127.0.0.1:8000
```

The API base URL is:

```text
http://127.0.0.1:8000/api
```

## API Routes

The API routes are defined in `routes/api.php`. The resource groups include:

| Resource group | Base endpoint |
|---|---|
| Users | `/api/users` |
| Roles | `/api/roles` |
| Ownerships | `/api/ownerships` |
| Expense categories | `/api/expense-categories` |
| Expenses | `/api/expenses` |
| Leads | `/api/leads` |
| Customers | `/api/customers` |
| Employees | `/api/employees` |
| Payroll | `/api/payrolls` |
| Payroll summaries | `/api/payroll-summaries` |
| Projects | `/api/projects` |
| Floors | `/api/floors` |
| Blocks | `/api/blocks` |
| Units | `/api/units` |
| Procurements | `/api/procurements` |
| Incentives | `/api/incentives` |
| Sales | `/api/sales` |
| Installments | `/api/installments` |
| Transactions | `/api/transactions` |
| Additional charges | `/api/additional-charges` |
| Rental projects | `/api/rental-projects` |
| Rental blocks | `/api/rental-blocks` |
| Rental floors | `/api/rental-floors` |
| Rental units | `/api/rental-units` |
| Rental leads | `/api/rental-leads` |
| Rental ownerships | `/api/rental-ownerships` |
| Tenants | `/api/tenants` |
| Rental installments | `/api/rental-installments` |

Most resource groups define list, search, create, show, update, and delete routes. Check `routes/api.php` for the exact route methods and controller actions.

### Project Hierarchy

| Method | Endpoint | Controller action |
|---|---|---|
| `GET` | `/api/hierarchy/project/{id}` | `projectFloors` |
| `GET` | `/api/hierarchy/floor/{id}` | `floorUnits` |
| `GET` | `/api/hierarchy/block/{id}` | `blockUnits` |
| `GET` | `/api/hierarchy/project-hierarchy/{id}` | `projectHierarchy` |

## Frontend Connection

The React frontend uses the API base URL configured by its `VITE_API_URL` environment variable.

For local development:

```env
VITE_API_URL=http://127.0.0.1:8000/api
```

See the [frontend README](../Praashad_real-state_erp_frontend/README.md) for frontend setup.

## Optional / Service Configuration

The project includes the Cloudinary Laravel package and a Cloudinary configuration file. Set the credentials required by the application's Cloudinary configuration if the related functionality is enabled.

Do not publish your `.env` file or expose database passwords, application keys, or third-party credentials.

## Useful Artisan Commands

| Command | Purpose |
|---|---|
| `php artisan serve` | Start the local Laravel server |
| `php artisan migrate` | Run database migrations |
| `php artisan migrate:status` | Check migration status |
| `php artisan route:list --path=api` | List API routes |
| `php artisan config:clear` | Clear cached configuration |
| `php artisan cache:clear` | Clear application cache |

## Project Structure

```text
Praashad_real-state_erp_backend/
├── app/
│   ├── Http/Controllers/Api/
│   ├── Models/
│   └── Console/
├── bootstrap/
├── config/
├── database/
│   ├── migrations/
│   ├── factories/
│   └── seeders/
├── public/
├── routes/
│   └── api.php
├── .env.example
├── artisan
└── composer.json
```

## License

No project-specific license is documented here. Refer to the repository root for project licensing information.
