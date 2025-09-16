# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Laravel 12 application with React frontend using Inertia.js, TypeScript, and Tailwind CSS. The project appears to be a starter kit with authentication, settings, and theme management features.

## Development Commands

### Backend (Laravel/PHP)
- `php artisan serve` - Start local development server
- `php artisan test` - Run PHPUnit tests
- `php artisan migrate` - Run database migrations
- `php artisan tinker` - Start Laravel REPL
- `php artisan queue:listen --tries=1` - Start queue worker
- `php artisan pail --timeout=0` - View application logs
- `php artisan inertia:start-ssr` - Start SSR server

### Frontend (Node.js/React)
- `npm run dev` - Start Vite development server
- `npm run build` - Build for production
- `npm run build:ssr` - Build with SSR support
- `npm run lint` - Run ESLint with auto-fix
- `npm run types` - TypeScript type checking
- `npm run format` - Format code with Prettier
- `npm run format:check` - Check code formatting

### Unified Development
- `composer dev` - Start all development services concurrently (Laravel server, queue worker, logs, and Vite)
- `composer dev:ssr` - Start development with SSR support
- `composer test` - Clear config cache and run tests

## Architecture

### Backend Structure
- **Laravel 12** with modern middleware configuration in `bootstrap/app.php`
- **Inertia.js** for seamless SPA experience with server-side routing
- **Authentication** system with auth routes and controllers in `app/Http/Controllers/Auth/`
- **Settings** functionality with dedicated routes and controllers
- **Custom Middleware**: `HandleAppearance` for theme management, `HandleInertiaRequests` for Inertia setup

### Frontend Structure
- **React 19** with TypeScript in `resources/js/`
- **Inertia.js** pages in `resources/js/pages/`
- **Wayfinder** for type-safe route generation with auto-generated actions in `resources/js/actions/`
- **Tailwind CSS v4** with custom components in `resources/js/components/`
- **Radix UI** components for accessible UI primitives
- **Theme system** with appearance hooks in `resources/js/hooks/`

### Key Files
- `vite.config.ts` - Vite configuration with React, Tailwind, and Wayfinder plugins
- `resources/js/app.tsx` - Main React application entry point
- `routes/web.php` - Main web routes (includes auth and settings routes)
- `phpunit.xml` - PHPUnit configuration with SQLite in-memory database for tests

### Testing
- **PHPUnit** for backend tests with separate Unit and Feature test suites
- Tests use in-memory SQLite database for speed
- Test environment configured in `phpunit.xml`

### Development Tools
- **ESLint** with React and TypeScript support
- **Prettier** with Tailwind CSS plugin and import organization
- **TypeScript** with strict configuration
- **Laravel Pint** for PHP code formatting