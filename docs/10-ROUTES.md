# Negaresh Yar V1
## Application Routes Specification

---

# Public Routes

---

## Homepage

URL:

/

Purpose:

Main landing page.

---

## Services

URL:

/services

Purpose:

Display available services.

---

## AI Interpretation

URL:

/ai-interpreter

Purpose:

Upload and analyze judicial documents.

---

## Request Page

URL:

/request

Purpose:

Display contact methods.

---

## Articles

URL:

/articles

Purpose:

Display published articles.

---

## Article Detail

URL:

/articles/{slug}

Purpose:

Display single article.

---

## Contact

URL:

/contact

Purpose:

Contact information.

---

# Admin Routes

Prefix:

/admin

---

## Dashboard

/admin/dashboard

---

## Articles

/admin/articles

Features:

- Create
- Edit
- Delete
- Publish

---

## AI Writer

/admin/ai-writer

Features:

- Generate
- Evaluate
- Improve

---

## AI Interpretation

/admin/interpretations

---

## Invoices

/admin/invoices

---

## SEO

/admin/seo

---

## Social Links

/admin/social-links

---

## Settings

/admin/settings

---

# API Routes

---

## Gemini Interpretation

POST:

/api/interpreter/analyze

---

## AI Article Generation

POST:

/api/ai-writer/generate

---

## Article Evaluation

POST:

/api/ai-writer/evaluate

---

# Routes That Must Not Exist

The following routes are forbidden in V1:

/register

/login (public)

/customers

/cases

/chat

/tickets

/payment

/subscription

---

# Route Rules

All routes must be:

- Clean
- SEO friendly
- Meaningful
- Future compatible