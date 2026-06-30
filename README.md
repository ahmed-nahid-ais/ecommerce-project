# Ecommerce Project

A full-stack ecommerce application for browsing products, managing a cart, checkout, and order tracking. Built with **Node.js**, **TypeScript**, and **Next.js** (App Router).

## Features

- Product catalog with categories and search
- Shopping cart
- Checkout flow
- Order management and status tracking
- Customer and admin roles *(planned)*

## Tech Stack

| Layer      | Technology              |
| ---------- | ----------------------- |
| Runtime    | Node.js                 |
| Language   | TypeScript              |
| Framework  | Next.js (App Router)    |
| UI         | React                   |
| Styling    | TBD (e.g. Tailwind CSS) |
| Database   | TBD                     |
| Auth       | TBD                     |

## Prerequisites

- [Node.js](https://nodejs.org/) 18.17 or later
- npm (comes with Node.js)

## Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd "Ecommerce Project"
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env.local` file in the project root:

```env
# Add variables as the project grows, e.g.:
# DATABASE_URL=
# NEXTAUTH_SECRET=
```

> Do not commit `.env` or `.env.local` files.

### 4. Run the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Available Scripts

| Command         | Description              |
| --------------- | ------------------------ |
| `npm run dev`   | Start development server |
| `npm run build` | Create production build  |
| `npm run start` | Run production server    |
| `npm run lint`  | Run ESLint               |

## Project Structure

```
Ecommerce Project/
├── src/
│   ├── app/              # Next.js App Router (pages, layouts, API routes)
│   ├── components/       # Reusable UI components
│   ├── lib/              # Utilities, helpers, shared logic
│   └── types/            # Shared TypeScript types and interfaces
├── public/               # Static assets
├── cursor.md             # AI assistant project guidelines
├── package.json
└── tsconfig.json
```

## Development Guidelines

- Use TypeScript strictly — prefer explicit types over `any`
- Prefer React Server Components; use `"use client"` only when needed
- Place API routes under `src/app/api/`
- Keep changes small and focused
- Never commit secrets or credentials

See [cursor.md](./cursor.md) for full project conventions and AI assistant context.

## License

ISC
