# Poster Frontend

Next.js 14 App Router frontend for the Poster AI physical product platform.

## Stack
- Next.js 14, TypeScript, Tailwind CSS, shadcn/ui, Framer Motion
- Inter font, Apple-like minimal aesthetic
- API calls go to FastAPI backend at http://localhost:8000

## Run
npm run dev

## Design principles
- Inter font everywhere
- White space is intentional — never crowd elements
- shadcn/ui components as the base, customised with Tailwind
- Framer Motion for transitions

## Learning Instructions

I am a junior developer learning Python, FastAPI, and AI engineering through this project. 
My current stack experience is Node.js, React, Postgres, and Express.

When you write any code for this project, always:
- Explain what the code does in plain English before showing it
- Point out syntax that is specific to TypeScript or Next.js App Router that might be unfamiliar
- If a pattern is different from how it would be done in plain React or Node.js, call that out explicitly
- Explain why a decision was made, not just what the decision is
- If there are multiple ways to do something, briefly mention the alternatives and why we chose this one
- Keep explanations concise — one short paragraph per concept, not an essay

## Project Structure Philosophy

Always organise code the way a senior engineer would structure a production Next.js App Router project.
Follow these conventions:

- `app/` — routes and pages only, no business logic
- `components/ui/` — shadcn base components, never modified directly
- `components/common/` — shared components used across multiple pages (Navbar, Footer, etc.)
- `components/features/` — feature-specific components (cards/, books/, checkout/, etc.)
- `lib/` — utility functions, helpers, constants
- `lib/api/` — all fetch calls to the FastAPI backend, one file per resource
- `hooks/` — custom React hooks only
- `types/` — TypeScript interfaces and types, one file per domain
- `config/` — app-wide configuration and constants

Rules:
- Never put fetch calls directly in a component — always go through lib/api/
- Never put business logic in a page — pages are layout and composition only
- If a component exceeds 150 lines, it needs to be broken into smaller components
- Every new file gets a one-line comment at the top explaining what it does
- When creating a new file, tell me which folder it belongs in and why