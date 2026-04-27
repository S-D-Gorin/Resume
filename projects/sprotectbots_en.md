# Bot Sprotect

## Sprotect Bots

Anti-spam platform for Telegram groups.

Developed a Telegram bot for automated moderation, unwanted content removal, and protection of groups from spam, advertising, flooding, and suspicious activity.

The project is built as a containerized microservice platform with separated Telegram transport, backend logic, data, reverse proxy, and scheduled task layers.

---

## My Role

**Full-cycle project owner:**

* system architecture
* backend development
* Telegram Bot API integration
* DevOps and deployment
* containerization
* anti-spam logic design
* admin panel development
* production support
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
* Cron

---

## Delivered Features

### Automated Telegram Group Moderation

* spam and advertising message removal
* anti-flood logic
* suspicious user checks
* response to message triggers and patterns
* group protection without manual administrator intervention

### Admin Panel

* moderation rule configuration
* whitelist and trusted user management
* message template management
* system status control
* access to data, events, and service information

### Background Processes

* scheduled broadcasts
* delayed message deletion
* scheduled service tasks
* service data cleanup
* backend endpoint calls for system maintenance

---

## Architecture

### Bot Gateway Layer

A dedicated PyTelegramBotAPI container:

* receives Telegram events via `infinity_polling()`
* serializes incoming messages
* forwards events to the backend API in JSON format

This approach isolates the Telegram transport layer from business logic.

### Backend Application Layer

The Django application running behind Gunicorn:

* processes incoming messages
* applies anti-spam logic
* moderates chats
* works with admin panel data
* sends replies to users
* deletes messages via the Telegram API

The backend uses the same `BOT_TOKEN`, which allows it to perform control actions directly: `deleteMessage`, `sendMessage`, and moderation actions.

Additional Python / FastAPI services are used for extended message processing.

### Data Layer

PostgreSQL stores:

* group data
* moderation settings
* users
* events
* service data

### Reverse Proxy Layer

NGINX handles incoming traffic, reverse proxying, and request routing.

### Scheduler Layer

A Cron container runs scheduled tasks, broadcasts, data cleanup, and backend endpoint calls.

---

## Impact

* Launched a production-ready anti-spam platform for Telegram groups
* Separated transport, logic, data, and scheduler layers by responsibility
* Prepared the architecture for extending anti-spam rules and external processors
* Moved administration into Django Admin without requiring manual code changes
* Simplified deployment and maintenance with Docker / Docker Compose

---
