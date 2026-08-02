# 🏛️ Laravel 12 Enterprise Boilerplate (`laravel-12-enterprise`)

<p align="center">
  <a href="https://github.com/zyekhabdul/laravel-12-enterprise/actions/workflows/ci.yml">
    <img src="https://github.com/zyekhabdul/laravel-12-enterprise/actions/workflows/ci.yml/badge.svg" alt="CI Build Status">
  </a>
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT">
  </a>
  <a href="https://laravel.com/">
    <img src="https://img.shields.io/badge/Laravel-12.x-red.svg?logo=laravel&logoColor=white" alt="Laravel 12">
  </a>
  <a href="https://www.php.net/">
    <img src="https://img.shields.io/badge/PHP-8.4-777BB4.svg?logo=php&logoColor=white" alt="PHP 8.4">
  </a>
  <a href="SECURITY.md">
    <img src="https://img.shields.io/badge/Architecture-DDD--Clean-brightgreen.svg" alt="Domain-Driven Design">
  </a>
</p>

A production-ready, enterprise-grade Laravel 12 boilerplate built around **Domain-Driven Design (DDD)** principles, strict typing, Data Transfer Objects (DTOs), and automated testing (Pest/PHPUnit).

---

## 🏗️ Domain-Driven Design (DDD) Architecture

```mermaid
graph TD
    A["HTTP Request / API Client"] --> B["API Gateway / Controllers"]
    B --> C["Form Requests & DTO Validation"]
    C --> D["Domain Application Actions & Service Handlers"]
    
    D --> E["Domain Entities & Aggregates"]
    D --> F["Domain Repositories (Contracts / Interfaces)"]
    
    F --> G["Infrastructure Layer (Eloquent / Redis / External APIs)"]
    E --> H["Domain Events & Queue Event Handlers"]
```

---

## 🚀 Key Features

- 🏛️ **Domain-Driven Design Structure**: Clear separation between Domain, Application, and Infrastructure layers.
- 📦 **Strict Typing & DTOs**: Spatie Data-style typed DTOs to eliminate array passing.
- 🔒 **Security First**: Prepared SQL, strict Content-Security-Policy middleware, and RBAC authorization.
- 🧪 **Automated Testing**: Pre-configured Pest / PHPUnit test suite for domain actions & API endpoints.
- 🐳 **Docker & Sail Ready**: Instant development environment setup using Docker Compose.

---

## 💻 Quick Start

```bash
# Clone repository
git clone https://github.com/zyekhabdul/laravel-12-enterprise.git
cd laravel-12-enterprise

# Install PHP dependencies
composer install

# Environment configuration
cp .env.example .env
php artisan key:generate

# Run database migrations & seeders
php artisan migrate --seed

# Start development server
php artisan serve
```

---

## 📜 License

MIT License © 2026 Zyekh Abdul Qadir Jailani.
