# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v1.3.0] - 2026-02-08

### Added
- **Backend**: New token validation endpoint to support enhanced session management.
- **Frontend**: Session validation logic and automatic logout mechanism for improved security.

### Changed
- **Bot Integration**: 
  - Restructured `ShigureCafeBot` into a modular package with a clear `main.py` entry point.
  - Simplified proxy configuration in the bot's application builder.
- **Repository Cleanup**: Removed deprecated `mihomo` directory from the root repository as part of the transition to `ShellCrash`.
- **Submodules**: Updated all submodule pointers to their latest stable versions.

---

## [v1.2.1] - 2026-02-02

### Changed
- **Proxy Service**: Switched from `mihomo` to `ShellCrash` for improved core management and added `MIHOMO_CONTROL_PORT` configuration.
- **Bot Integration**: Updated `ShigureCafeBot` submodule to fix intermittent stops by implementing asynchronous HTTP requests.
- **Service Health**: Enhanced healthcheck for the proxy service to verify dashboard accessibility.

---

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
