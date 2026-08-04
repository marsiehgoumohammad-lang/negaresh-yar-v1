# Negaresh Yar V1 - Technical Architecture

## Architecture Decision

Negaresh Yar V1 uses a modern full-stack JavaScript architecture.

The reason for this decision is:

- Fast development.
- Native compatibility with the current development environment.
- Strong SEO support.
- Excellent React ecosystem.
- Simple Gemini API integration.

---

# Technology Stack

## Full Stack Framework

Next.js

Version:

Latest stable version


---

## Frontend

React

+

Tailwind CSS

+

TypeScript


---

## Backend

Next.js Server Actions

+

API Routes


The backend logic is implemented inside the Next.js application.

---

## Database

PostgreSQL


ORM:

Prisma


---

## AI Provider

Google Gemini API


---

# Application Architecture
Browser

↓

Next.js App Router

↓

React Components

↓

Server Actions / API Routes

↓

Services Layer

↓

Prisma ORM

↓

PostgreSQL Database

---

# Project Structure
src/

├── app/
│
├── components/
│
├── services/
│
├── lib/
│
├── prisma/
│
├── types/
│
└── utils/

---

# Main Application Sections

## Public Website

Responsibilities:

- Homepage.
- Services pages.
- AI interpreter page.
- Articles.
- Request page.


---

## Admin Panel

Responsibilities:

- Article management.
- AI article workflow.
- Social link management.
- Invoice generation.
- Website settings.


---

# Service Layer

Business logic must not be placed directly inside UI components.

Services:

## GeminiService

Responsibilities:

- Gemini API communication.
- Prompt handling.
- Error handling.


---

## ArticleService

Responsibilities:

- Article generation.
- Review workflow.
- Score calculation.


---

## SeoService

Responsibilities:

- Metadata generation.
- Sitemap.
- Schema markup.


---

## InvoiceService

Responsibilities:

- Invoice creation.
- PDF generation.


---

# SEO Architecture

Next.js must use:

- Server Side Rendering.
- Static generation where possible.
- Dynamic metadata.
- Structured data.


---

# Mobile First Rule

All interfaces must be designed for mobile first.

Desktop is an adaptation of mobile experience.

---

# Development Rules

Do not:

- Add unnecessary packages.
- Create unnecessary abstractions.
- Change architecture without permission.

Keep the V1 implementation simple and maintainable.
