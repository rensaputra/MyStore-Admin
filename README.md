# MyStore - Admin

An admin dashboard for a fashion-oriented eStore built with Next.js. This application allows the store owner to easily manage their inventory (including fashion sizes like S/M/L), product categories, user administration, buyers, and tracking of sales transactions.

> **Note**: This repository contains the admin dashboard. There is a separate client-facing repository called "MyStore - Client" that handles the customer storefront.

## Tech Stack

- **Framework**: [Next.js 16](https://nextjs.org/) (App Router)
- **Library**: [React 19](https://react.dev/)
- **Database**: PostgreSQL
- **ORM**: [Prisma 7](https://www.prisma.io/)
- **Styling**: [Tailwind CSS 4](https://tailwindcss.com/)
- **Charts**: [Recharts](https://recharts.org/)
- **Language**: TypeScript

## Features

- **Product Management**: Add, update, and manage products, tracking inventory levels, prices, and specifics like small/medium/large sizes.
- **Product Types**: Categorize your items (e.g. Shirts, Pants, Accessories).
- **Sales Transactions**: View comprehensive sales and track individual transactions.
- **Buyer & User Management**: Keep track of registered buyers and manage admin access.
- **Charts & Analytics**: Easily visualize business metrics with interactive charts.

## Prerequisites

- Node.js 18+
- npm
- PostgreSQL database

## Getting Started

1. **Clone the repository and install dependencies**
```bash
npm install
```

2. **Environment Variables**
Create a `.env` file in the root directory and add the following variables:
```env
# Connection string for your PostgreSQL database
DATABASE_URL="postgresql://user:password@localhost:5432/mystore"

# JWT Secret for authentication
JWT_SECRET="your-super-secret-jwt-key"
```

3. **Database Setup**
Generate the Prisma client and push your schema to the database:
```bash
# Generate the Prisma client
npm run gen:prisma

# Run migrations to update your DB schema
npm run migrate:dev
```
*(Optional) You can seed the database using `npm run db:seed`*

4. **Start the Development Server**
```bash
npm run dev
```
The admin app will start on **http://localhost:3001** (as configured in package.json).

## Available Scripts

| Script                 | Description                             |
| ---------------------- | ---------------------------------------- |
| `npm run dev`          | Start the dev server on port 3001       |
| `npm run build`        | Build for production                    |
| `npm run start`        | Start the production server on port 3001|
| `npm run lint`         | Run ESLint                              |
| `npm run gen:prisma`   | Generate the Prisma client              |
| `npm run migrate:dev`  | Run DB migrations in development        |
| `npm run migrate:prod` | Deploy DB migrations in production      |
| `npm run db:push`      | Push schema changes without a migration |
| `npm run db:seed`      | Seed the database                       |

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
