# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Structure

Monorepo-style layout with a Next.js 16 frontend application in `frontend/`.

## Tech Stack

- **Framework**: Next.js 16.1.6 (App Router, Turbopack)
- **React**: 19.2.3
- **Language**: TypeScript (strict mode)
- **Styling**: Tailwind CSS v4 (using `@import "tailwindcss"` and `@theme inline`)
- **Package Manager**: npm

## Commands

All commands run from `frontend/`:

```bash
npm run dev      # Start dev server (Turbopack)
npm run build    # Production build
npm run start    # Run production server
npm run lint     # ESLint with Next.js core web vitals + TypeScript rules
```

## Architecture

- **App Router**: `frontend/app/` — uses Next.js 13+ file-based routing
- **Path alias**: `@/*` maps to `frontend/*` (configured in tsconfig.json)
- **Fonts**: Google Fonts (Geist Sans & Geist Mono) loaded via `next/font/google` in root layout
- **Theming**: CSS custom properties in `globals.css` with dark mode via `prefers-color-scheme`
- **Static assets**: `frontend/public/`
