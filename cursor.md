# Ecommerce Project — Cursor AI Guide

This file provides context and guidelines for AI assistants working in this project.

## Project Overview

An ecommerce application built with Next.js and TypeScript for managing products, cart, checkout, and orders.

## Tech Stack

- **Runtime:** Node.js
- **Language:** TypeScript
- **Framework:** Next.js (App Router)
- **Frontend:** React (via Next.js)
- **Styling:** TBD (e.g. Tailwind CSS)
- **Database:** TBD
- **Auth:** TBD

## Project Structure

```
Ecommerce Project/
├── cursor.md
├── src/
│   ├── app/              # Next.js App Router (pages, layouts, API routes)
│   ├── components/       # Reusable UI components
│   ├── lib/              # Utilities, helpers, shared logic
│   └── types/            # Shared TypeScript types/interfaces
├── public/               # Static assets
├── package.json
└── tsconfig.json
```

## Coding Conventions

- Use TypeScript strictly — avoid `any`; prefer explicit types and interfaces
- Use functional React components; prefer Server Components unless client interactivity is needed (`"use client"`)
- Colocate API logic in `src/app/api/` route handlers or `src/lib/` services
- Write clear, self-documenting code with meaningful names
- Keep changes focused — avoid unrelated refactors
- Match existing patterns and style in the codebase
- Add comments only for non-obvious business logic
- Handle errors explicitly; avoid silent failures

## Ecommerce Domain Notes

- **Products:** name, description, price, stock, images, categories
- **Cart:** session or user-based; validate stock before checkout
- **Orders:** immutable once placed; track status (pending, paid, shipped, delivered)
- **Payments:** never log or store raw card data; use a payment provider
- **Users:** separate customer and admin roles where applicable

## AI Assistant Instructions

When working in this project:

1. Read surrounding code before making changes
2. Prefer minimal, targeted diffs over large rewrites
3. Reuse existing utilities and components instead of duplicating logic
4. Do not commit secrets (`.env`, API keys, credentials)
5. Only create git commits when explicitly asked
6. Ask before adding new dependencies or changing architecture

## Common Tasks

- **Add a feature:** follow App Router conventions (`page.tsx`, `layout.tsx`, `route.ts`)
- **Fix a bug:** identify root cause; avoid broad speculative changes
- **New API endpoint:** add `route.ts` under `src/app/api/`; validate input; return typed JSON responses
- **UI component:** keep accessible (labels, keyboard nav, contrast); split Server vs Client components appropriately

## Environment Setup

```bash
npm install
npm run dev      # Start dev server (default: http://localhost:3000)
npm run build    # Production build
npm run start    # Run production server
npm run lint     # Run ESLint
```
