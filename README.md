# BizManager — Small Business Suite

A comprehensive business management dashboard to streamline product inventory, track customer relationships, and monitor sales performance — all in one centralized location.

## Features

- **Dashboard** — Live business metrics (total products, customers, sales, revenue), recent sales activity, and low-stock alerts
- **Products** — Full catalog management with image uploads, stock tracking, search, and CRUD operations
- **Customers** — Contact management with company info, search, and CRUD operations
- **Sales** — Transaction recording with auto-calculated totals, stock deduction on completed sales, status filtering, and revenue tracking
- **Authentication** — Email/password login, registration, and password reset flows
- **Role-Based Access** — Admin-only writes for products, customers, and sales; owner-scoped data visibility

## Tech Stack

- **Frontend:** React + Vite + Tailwind CSS + shadcn/ui
- **Backend:** Base44 (MongoDB-backed entities, auth, file storage)
- **Icons:** Lucide React
- **Charts:** Recharts

## Data Models

| Entity | Key Fields |
|--------|-----------|
| Product | name, description, price, quantity, category, image_url, sku |
| Customer | name, email, phone, address, company |
| Sale | product, customer, quantity, unit_price, total_amount, sale_date, status |

---

## Base44 Project

Use this repository to run and edit the app locally, then publish changes back through Base44.

## Prerequisites

1. Clone the repository using the project's Git URL.
2. Navigate to the project directory.
3. Install dependencies: `npm install`.
4. Install the Base44 CLI: `npm install -g base44@latest`.
5. Install [Deno](https://docs.deno.com/runtime/getting_started/installation/) — the local Base44 backend runs on it.

## Run Locally

```bash
base44 login   # one-time per machine
base44 link    # one-time per clone
base44 dev     # local backend + frontend together
```

## Publish Your Changes

```bash
base44 dashboard open
```

## Docs & Support

GitHub integration: https://docs.base44.com/developers/app-code/local-development/github

Support: https://app.base44.com/support
