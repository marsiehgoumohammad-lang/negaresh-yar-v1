# Negaresh Yar V1
## Technical Architecture Document

---

# Architecture Goal

The architecture must support a professional commercial product while keeping V1 simple and maintainable.

The system must be easy to expand in future versions.

---

# Application Architecture

Architecture Pattern:

MVC + Service Layer

---

# Backend Structure

Framework:

Laravel 13

Main responsibilities:

- Business logic
- Database communication
- API communication
- Security
- Content management

---

# Frontend Structure

Technology:

- Blade Templates
- Tailwind CSS 4
- Vite

Design approach:

Server-rendered application with optimized performance.

---

# Main Application Layers

## Controllers

Responsibilities:

- Receive requests
- Validate input
- Call services
- Return responses

Controllers must remain clean.

---

## Services

Business logic must be placed in service classes.

Examples:

- GeminiService
- ArticleWriterService
- SeoService
- InvoiceService

---

## Models

Models represent database entities.

Models must not contain complex business logic.

---

## Database Layer

Technology:

MySQL

Requirements:

- Clean relationships
- Proper indexing
- Future scalability

---

# AI Integration Architecture

AI provider:

Google Gemini API

---

AI communication must be isolated.

Example structure:

app/

Services/

Gemini/

GeminiService.php

---

Benefits:

- Easy replacement
- Better maintenance
- Cleaner code

---

# Article System Architecture

Workflow:

Input Topic

↓

AI Research

↓

Article Generation

↓

Quality Evaluation

↓

SEO Evaluation

↓

Approval

↓

Publication

---

# File Storage Architecture

Uploaded files must be stored securely.

Rules:

- No public direct access
- File validation required
- Storage separation

---

# Configuration Management

Sensitive information:

- API keys
- Database credentials
- External services

must exist only inside environment variables.

---

# Performance Requirements

The application should prioritize:

- Fast page loading
- Optimized assets
- Minimal JavaScript
- Server-side rendering

---

# Future Compatibility

The architecture should allow:

- Mobile application
- Advanced user accounts
- Payment systems
- Larger AI workflows

without rewriting the core system.