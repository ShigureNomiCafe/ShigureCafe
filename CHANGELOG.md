# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v1.2.0] - 2026-01-31

### Added
- **Telegram Bot Integration**: Added `ShigureCafeBot` to handle user verification and automate group invite links.
- **Enhanced Rate Limiting**: Backend now uses Bucket4j for more robust and flexible rate limiting.
- **Improved Security**: Refactored API key authentication mechanism and enhanced internal service security.

### Changed
- **Service Orchestration**: Updated root `docker-compose.yml` to include and manage the Telegram bot service.
- **Configuration**: Standardized environment variable names across services (e.g., `CAFE_API_KEY`).
- **Plugin Update**: Updated Minecraft plugin to v1.0.2 for better API key handling.

### Fixed
- Fixed various consistency issues in service-to-service communication.

---

## [v1.1.1] - 2026-01-24

### Added
- Integrated Cloudflare Turnstile CAPTCHA for both Frontend and Backend.
- Added version badges and detailed technical stack to documentation.

### Fixed
- Fixed package naming typos in Backend.
- Resolved UI flickering in Frontend when binding Minecraft accounts.
