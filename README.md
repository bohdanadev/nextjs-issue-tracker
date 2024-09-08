# NEXTJS-ISSUE-TRACKER

## Overview

NEXTJS-ISSUE-TRACKER is a fullstack issue tracking application built using modern web technologies such as Next.js, TypeScript, Prisma, TailwindCSS, and Radix UI. It provides functionality for user authentication (via Google), creating and managing issues, assigning users to issues, filtering issues by status and sorting, and editing or deleting issues.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies](#technologies)
- [Installation](#installation)
- [Commands](#commands)

## Features

- **User Authentication**: Google login via NextAuth.
- **Issue Management**: Create, view, edit, and delete issues.
- **Assign Users**: Assign users to specific issues.
- **Filter & Sort**: Filter issues by status (open, closed, in progress.) and sort them.
- **Authorization**: Only authenticated users can manage issues.

## Technologies

### Next.js

Next.js is a React-based framework that enables server-side rendering and static site generation. It simplifies routing, handling API routes, and provides built-in performance optimizations.

### TypeScript

TypeScript is a superset of JavaScript that brings static typing to the language, improving code quality and development experience.

### Prisma

Prisma is an open-source ORM (Object Relational Mapping) that helps with database management by providing an easy-to-use query language. It works well with Next.js and allows for the integration of relational databases like MySQL and PostgreSQL.

### PlanetScale

PlanetScale is a scalable serverless MySQL-compatible database platform. It works with Prisma to manage the app's database schema, migrations, and querying.

### TailwindCSS

TailwindCSS is a utility-first CSS framework that provides low-level CSS classes to build custom designs quickly and efficiently.

### Radix UI

Radix UI provides accessible, unstyled, and highly customizable UI components for React apps. It's used in this project for building the interface.

### NextAuth

NextAuth.js is a complete open-source authentication solution for Next.js applications.

### Axios

Axios is a promise-based HTTP client used for making API requests from the client to the server.

### TanStack Query

TanStack Query (React Query) simplifies data fetching, caching, synchronization, and more in React applications. It's used for handling server state, particularly with fetching, caching, and updating users data.

### Zod

Zod is a TypeScript-first schema declaration and validation library. It's used for validating incoming data such as issue title, description, etc.

## Installation

1. Clone this repository to your local machine.

2. In the project folder, rename **.env.example** to **.env**.

3. Set **all** the environment variables.

You will need to set the following environment variables:

`NEXTAUTH_URL`: The URL where your app is hosted (e.g., http://localhost:3000).

`GOOGLE_CLIENT_ID`: The client ID from your Google OAuth app.

`GOOGLE_CLIENT_SECRET`: The client secret from your Google OAuth app.

`DATABASE_URL`: The connection URL for your database (PlanetScale in this example).

4. Run `npm install` to install the dependencies.

5. Set up PlanetScale database:

Create a new database in PlanetScale and obtain the connection URL.
Add this URL to your `.env` file as `DATABASE_URL`.

Migrate the Database: Run `npx prisma migrate dev` to generate database tables.

6. Run `npm run dev` to start the web server.

This will run the app in development mode.

7. Open the app in your browser:

Open http://localhost:3000 to view it in the browser.

## Commands

### Development

- **Start the development server:**

```bash
npm run dev
```

### Production

- **Build the project for production:**

```bash
npm run build
```

- **Run the production server:**
  `npm run start`

### Prisma

- **Run Prisma migrations:**

```bash
npx prisma migrate dev --name <migration-name>
```

Use this command to apply migrations to the database during development. Replace <migration-name> with a descriptive name for the migration.

- **Reset the database:**

```bash
npx prisma migrate reset
```

This resets the database and applies all migrations from scratch. It is useful when developing locally.
