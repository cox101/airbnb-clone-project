# 🏠 Airbnb Clone Project

[![CI/CD](https://github.com/cox101/airbnb-clone-project/actions/workflows/ci.yml/badge.svg)](https://github.com/cox101/airbnb-clone-project/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📌 Overview

The **Airbnb Clone Project** is a real-world inspired backend system that replicates key functionalities of Airbnb. Built using Django and Django REST Framework, the project focuses on secure APIs, robust database design, seamless user interactions, payment integrations, and modern CI/CD workflows.

---

## 🎯 Project Goals

- Build secure RESTful and GraphQL APIs.
- Manage user authentication and roles.
- Enable property listing and booking.
- Integrate secure payment handling.
- Allow guests to leave reviews and ratings.
- Implement CI/CD pipelines for deployment.
- Optimize database queries for performance.

---

## 👥 Team Roles

| Role                       | Responsibilities                                                                                  |
|---------------------------|---------------------------------------------------------------------------------------------------|
| **Backend Developer**      | Implements API endpoints, business logic, and third-party integrations (auth, payments).          |
| **Database Administrator** | Designs schema, maintains data integrity, optimizes queries.                                     |
| **DevOps Engineer**        | Manages Docker, CI/CD pipelines with GitHub Actions, and deployment workflows.                   |
| **QA Engineer**            | Writes tests, performs API validation, and ensures functionality with automated test suites.     |

---

## 🛠️ Technology Stack

| Technology                      | Purpose                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------|
| **Django + DRF**                | Backend framework for building RESTful APIs.                                             |
| **GraphQL**                     | Enables dynamic queries between client and server.                                       |
| **MySQL**                       | Stores user, property, booking, and payment data.                                        |
| **Redis**                       | Supports caching and background task queuing.                                            |
| **Celery**                      | Executes asynchronous tasks like sending emails and processing payments.                |
| **Docker**                      | Containers for consistent dev/test/prod environments.                                    |
| **GitHub Actions**              | CI/CD automation tool for testing and deploying the app.                                 |

---

## 🗄️ Database Design

### Users

Stores authentication credentials and user roles.

- `id`
- `username`
- `email`
- `password`
- `role` (guest or host)

### Properties

Details about listings.

- `id`, `title`, `description`, `location`, `price_per_night`, `host_id`

### Bookings

Records reservation data.

- `id`, `user_id`, `property_id`, `check_in`, `check_out`, `status`

### Payments

Tracks financial transactions.

- `id`, `booking_id`, `amount`, `status`, `payment_date`

### Reviews

Captures user feedback and ratings.

- `id`, `user_id`, `property_id`, `rating`, `comment`

---

## 🧩 Feature Breakdown

### 👤 User Management

Handles user registration, login, profile updates, and role-based access control. Ensures only authenticated users interact with protected endpoints.

### 🏠 Property Management

Hosts can create, update, and manage listings. Guests can view and filter available properties.

### 📅 Booking System

Guests can book available properties with defined check-in and check-out dates. Prevents overlapping reservations.

### 💳 Payment Processing

Securely integrates third-party payment gateways (e.g., Stripe) for handling transactions linked to bookings.

### 🌟 Review System

Guests can rate and write reviews for properties, enhancing trust and decision-making for future bookings.

### ⚡ Data Optimization

Utilizes indexes, caching (Redis), and query optimization to maintain speed and performance as data scales.

### 🔐 API Security

Implements JWT-based authentication, input sanitization, HTTPS, and role-based access control to protect users and data.

### 🔁 CI/CD Integration

GitHub Actions automates testing, building, and deploying the project using Docker and Docker Compose workflows.

---

## 🔐 API Security

Security is integral to the platform:

- **Authentication**: Verifies user identity using JWT tokens.
- **Authorization**: Role-based access ensures only permitted actions are allowed.
- **Rate Limiting**: Prevents abuse and DDoS using throttling.
- **Input Validation**: Protects against SQL injection and XSS attacks.
- **HTTPS & Secure Headers**: Ensures encrypted data transmission and mitigates common exploits.
- **Secure Payment Flow**: Integrates trusted payment gateways with tokenized transactions.

---

## 🔁 CI/CD Pipeline

### Why CI/CD?

- 🔁 **Continuous Integration**: Ensures that new code merges don’t break existing features.
- 🚀 **Continuous Deployment**: Automates release of tested features to staging/production.
- ✅ **Faster Development**: Enables rapid iteration and delivery of updates.
- 🧪 **Improved Quality**: Automatically runs linting, tests, and builds before deployments.

### Tools

- **GitHub Actions** – Automates test and deploy workflows.
- **Docker + Docker Compose** – Manages application containers for each service.
- **Pytest** – Runs backend test suites.
- **PostgreSQL (in Docker)** – Provides consistent database for testing environments.

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- Docker & Docker Compose
- MySQL or PostgreSQL
- Redis

### Setup

```bash
git clone https://github.com/cox101/airbnb-clone-project.git
cd airbnb-clone-project

