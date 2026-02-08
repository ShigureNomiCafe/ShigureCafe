# ShigureCafe ![Version](https://img.shields.io/badge/version-1.3.0-blue)

A robust, secure, and modern social and management system specifically designed for Minecraft communities. It features real-time chat synchronization, automated whitelist management, and a premium user-audit workflow.

## 🚀 Project Overview

ShigureCafe is a full-stack solution consisting of five main components:
- **[Backend](./ShigureCafeBackend)**: Spring Boot 4 + Java 25 service handling auth, security, and game integration.
- **[Frontend](./ShigureCafeFronted)**: Vue 3 + Tailwind CSS 4 dashboard for users and administrators.
- **[Telegram Bot](./ShigureCafeBot)**: Python-based bot for user verification and community management.
- **[Minecraft Plugin](./ShigureCafePlugin)**: MCDReforged plugin for real-time game-to-web synchronization.
- **Gateway**: Nginx-based reverse proxy with automated HTTPS/SSL support.

---

## ✨ Key Features

- **🛡️ Advanced Security**: Stateless JWT authentication, MFA (Email & TOTP), Cloudflare Turnstile CAPTCHA, and Bucket4j rate limiting.
- **🤖 Telegram Integration**: Automated user verification and one-time invite link generation for private groups.
- **🎮 Minecraft Integration**: 
  - **Account Binding**: Link Minecraft accounts via Microsoft OAuth2.
  - **Real-time Chat**: Bidirectional sync between game chat and web interface.
  - **Auto Whitelist**: Dynamic whitelist management based on user audit status.
- **📋 Management Workflow**: 
  - **User Audit**: Multi-stage registration with administrator approval.
  - **Notice Board**: Markdown & KaTeX supported announcement system with reactions.
- **☁️ Cloud Ready**: S3-compatible storage integration for avatars and resources.
- **🌐 Global Reach**: Full i18n support (English & Chinese).

---

## 🛠️ Technical Stack

| Layer | Technologies |
| :--- | :--- |
| **Backend** | Java 25, Spring Boot 4.0, Spring Security, MariaDB, Redis, Bucket4j |
| **Frontend** | Vue 3.5, Vite 7, TypeScript, Tailwind CSS 4, Pinia |
| **Telegram Bot** | Python 3.14, python-telegram-bot |
| **Plugin** | Python, MCDReforged, WebSockets |
| **Infrastructure** | Docker, Nginx (Gateway), S3 Storage |

---

## 📦 Getting Started

### Prerequisites
- [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/)
- SSL Certificates (placed in `./certs/`) if using HTTPS

### Quick Start with Docker

1. **Clone the repository**:
   ```bash
   git clone --recursive https://github.com/your-repo/ShigureCafe.git
   cd ShigureCafe
   ```

2. **Configure environment variables**:
   ```bash
   cp .env.example .env
   # Edit .env with your domain, credentials, and S3 settings
   ```

3. **Prepare SSL Certificates**:
   Place your `fullchain.pem` and `privkey.pem` into the `./certs/` directory.

4. **Launch the system**:
   ```bash
   docker compose up -d
   ```

The gateway will be available at your configured `DOMAIN_NAME` (defaulting to `http://localhost`).

---

## 📂 Project Structure

```text
ShigureCafe/
├── ShigureCafeBackend/    # Java Spring Boot backend
├── ShigureCafeFronted/     # Vue.js frontend application
├── ShigureCafeBot/         # Telegram verification bot
├── ShigureCafePlugin/      # MCDR Minecraft plugin
├── certs/                  # SSL certificates (git-ignored)
├── nginx.conf.template     # Nginx template with ENV support
├── docker-compose.yml      # Main orchestration file
└── .env.example            # Template for all configurations
```
