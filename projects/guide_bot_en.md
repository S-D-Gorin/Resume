# Telegram Guide Bot

## Sprotect Bots / Guide Platform

**guide.sprotectbots.ru**

Developed a Telegram bot and CMS platform for creating photo and audio guides with in-Telegram online payments.

The platform enables digital tours with routes, locations, photos, and audio files. Users can pay for access to gated content directly inside Telegram, while content managers manage materials, transactions, and revenue through a web interface.

---

## My Role

**Full-cycle project owner:**

* application architecture
* backend development
* DevOps and deployment
* payment system integrations
* production infrastructure setup
* security and production support
* product development

---

## Technology Stack

* Python
* Django
* Django REST Framework
* PyTelegramBotAPI
* PostgreSQL
* Gunicorn
* NGINX
* Docker
* Docker Compose

---

## Delivered Features

### Telegram Bot Platform

* audio guide experience inside Telegram
* interactive user flow
* route scenario logic
* user journey without installing a separate application

### Online Payments

Integrated payment systems:

* YooMoney / YooKassa
* Robokassa

### CMS / Admin Panel

Implemented a content management system based on Django Admin:

* route creation
* location management
* photo and audio uploads
* object descriptions
* gated content management
* transaction and revenue tracking

---

## Architecture

### Telegram Bot Layer

The PyTelegramBotAPI bot receives incoming messages and acts as a gateway layer for the user journey.

### Application Layer

The Django application:

* handles business logic
* stores user data
* works with media files
* generates user-facing responses
* manages payments and content access

### Data Layer

PostgreSQL stores users, orders, content, and scenario state.

### Reverse Proxy Layer

NGINX handles routing and external traffic.

---

## Impact

* Launched a production-ready platform for digital tours inside Telegram
* Gave content managers a self-service CMS without developer dependency
* Automated payment and access activation inside the user journey
* Prepared the architecture for extending routes, content, and payment providers
* Simplified deployment and maintenance with Docker / Docker Compose

---
