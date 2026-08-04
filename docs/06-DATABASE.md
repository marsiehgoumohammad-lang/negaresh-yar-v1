# Negaresh Yar V1
## Database Design Document

---

# Database Philosophy

The V1 database must be minimal.

Only required business data should exist.

Avoid unnecessary tables.

---

# Database Engine

MySQL

---

# Core Tables

---

# users

Purpose:

Admin authentication only.

Important:

Public user registration does not exist.

Fields:

- id
- name
- email
- password
- created_at
- updated_at

---

# articles

Purpose:

Store published content.

Fields:

- id
- title
- slug
- excerpt
- content
- featured_image
- meta_title
- meta_description
- status
- published_at
- created_at
- updated_at

---

# article_scores

Purpose:

Store AI evaluation results.

Fields:

- id
- article_id
- quality_score
- seo_score
- readability_score
- total_score
- evaluation_details
- created_at

---

# ai_interpretations

Purpose:

Store AI document interpretation requests.

Fields:

- id
- file_path
- file_type
- ai_response
- status
- created_at
- updated_at

---

# invoices

Purpose:

Simple invoice generation.

Fields:

- id
- invoice_number
- customer_name
- description
- amount
- logo_path
- created_at

---

# social_links

Purpose:

Manage external communication links.

Fields:

- id
- platform
- url
- active
- created_at
- updated_at

Platforms:

- WhatsApp
- Telegram
- Rubika
- Eitaa
- Bale

---

# settings

Purpose:

Global website settings.

Fields:

- id
- key
- value
- created_at
- updated_at

---

# Excluded Database Tables

Do not create:

- customers
- cases
- conversations
- tickets
- payments
- subscriptions

---

# Database Rules

- Use migrations.
- Use meaningful naming.
- Add indexes where needed.
- Keep schema simple.