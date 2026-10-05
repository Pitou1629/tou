# my-accessories-cambodia-tech
E-commerce platform for mobile phone accessories in Cambodia with admin dashboard, customer portal, real-time notifications, and analytics

## Database

The Express backend stores customers, products, orders, visits, feedback, and messages in SQLite at `backend/data/store.sqlite`. On first startup, it imports existing data from `backend/data/db.json` without deleting or modifying that file. If there is no JSON database, it initializes the SQLite database with the sample products.

Set `DATABASE_PATH` to use a different SQLite file location. For example, in PowerShell:

```powershell
$env:DATABASE_PATH = "C:\data\my-accessories.sqlite"
npm run dev
```

Install dependencies with `npm install`, then start the site and API with `npm run dev`.

## Storefront and admin access

The customer-facing storefront displays the complete product catalog without sales counts. Sales analytics and inventory controls are restricted to the admin dashboard. Only authenticated administrators can add products; newly added products appear in the customer catalog.
