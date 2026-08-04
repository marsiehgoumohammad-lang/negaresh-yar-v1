# Negaresh Yar V1 - Database Specification

## Database Technology

Database:

PostgreSQL


ORM:

Prisma


---

# Database Philosophy

The database must remain minimal.

Only required V1 features should have database models.

Do not create future systems inside V1.

---

# Prisma Models

The main models are:

- AdminUser
- Article
- ArticleReview
- AiInterpretation
- Invoice
- InvoiceItem
- SocialLink
- Setting


---

# AdminUser Model

Purpose:

Stores administrator accounts only.


Fields:

- id
- name
- email
- passwordHash
- createdAt
- updatedAt


Important:

There is no public user account system.


---

# Article Model

Purpose:

Stores website articles.


Fields:

- id
- title
- slug
- excerpt
- content
- featuredImage
- metaTitle
- metaDescription
- status
- publishedAt
- createdAt
- updatedAt


Status:

- DRAFT
- REVIEW
- APPROVED
- PUBLISHED


---

# ArticleReview Model

Purpose:

Stores AI article evaluations.


Fields:

- id
- articleId
- seoScore
- contentScore
- qualityScore
- finalScore
- reviewData
- createdAt


Relationship:

One article can have multiple reviews.


---

# AiInterpretation Model

Purpose:

Stores AI document interpretation history.


Fields:

- id
- filePath
- fileType
- aiResult
- status
- createdAt
- updatedAt


Status:

- PENDING
- PROCESSING
- COMPLETED
- FAILED


---

# Invoice Model

Purpose:

Simple invoice generation.


Fields:

- id
- invoiceNumber
- customerName
- customerPhone
- totalAmount
- createdAt
- updatedAt


Note:

This is not a CRM system.


---

# InvoiceItem Model

Purpose:

Invoice rows.


Fields:

- id
- invoiceId
- description
- quantity
- amount


---

# SocialLink Model

Purpose:

Manage messenger links.


Platforms:

- WhatsApp
- Telegram
- Eitaa
- Rubika
- Bale


Fields:

- id
- platform
- url
- active


---

# Setting Model

Purpose:

General website settings.


Examples:

- siteName
- logo
- phone
- seoTitle
- seoDescription


---

# Forbidden V1 Models

Do not create:

- Customers
- Cases
- Conversations
- Tickets
- Payments
- CRM tables
