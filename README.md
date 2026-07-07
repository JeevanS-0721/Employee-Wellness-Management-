# MoodMentor

> An AI-powered emotional tone analyzer and well-being recommendation platform designed to help organizations understand emotional trends in written communication while maintaining privacy and security.

---

# Project Overview

MoodMentor is an AI-powered emotional tone analyzer that identifies emotional patterns in written communication and provides personalized well-being recommendations.

Modern organizations generate large volumes of text through emails, feedback forms, surveys, and internal communication channels. Extracting meaningful emotional insights from this data manually is time-consuming and difficult. MoodMentor automates this process by analyzing unstructured text, identifying emotional dimensions, and translating the results into actionable wellness recommendations.

The platform is designed for:

- Human Resources teams
- Team Managers
- Organizational Wellness Programs
- Internal Research Teams

By providing longitudinal emotional insights, MoodMentor helps organizations better understand workforce well-being while ensuring secure handling of user information.

---

# Key Features

- AI-powered emotional tone analysis
- Personalized wellness recommendations
- Secure user authentication
- Email-based OTP verification
- Password recovery workflow
- JWT-based session management
- Protected analytics dashboard
- Historical emotional trend tracking
- Privacy-focused architecture
- Secure password storage using bcrypt

---

# System Architecture

MoodMentor follows a modular and decoupled architecture for scalability, maintainability, and security.

## Application Layer

- Streamlit-based web interface
- Optimized light theme for accessibility
- Multi-page application structure

## Database Layer

- Serverless Neon PostgreSQL
- Relational data storage
- Indexed user records
- Historical activity logging

## Security Layer

- Bcrypt password hashing
- JSON Web Token (JWT) authentication
- Secure session management
- OTP verification system

## Communication Layer

- Secure SMTP integration
- SSL / STARTTLS email delivery
- Automated verification email routing

---

# Technology Stack

| Component | Technology |
|-----------|------------|
| Frontend | Streamlit |
| Backend | Python |
| Database | Neon PostgreSQL |
| Authentication | JSON Web Tokens (JWT) |
| Password Security | bcrypt |
| Email Service | SMTP (SSL / STARTTLS) |
| Data Storage | PostgreSQL |

---

# Database Design

## Users Table

Stores registered user profiles.

### Fields

- User ID (Primary Key)
- Username
- Email Address
- Password Hash
- Account Status
- Created Timestamp

---

## OTP Codes Table

Stores temporary verification codes.

### Fields

- OTP Record ID
- Email Address
- Six-Digit Verification Code
- Verification Purpose
- Expiration Time
- Used Status

---

# Core Modules

## 1. User Registration

- Validates all required fields
- Email validation using Regex
- Prevents duplicate usernames
- Prevents duplicate email addresses
- Generates secure six-digit OTP
- Stores verification record
- Sends verification email

---

## 2. Email Verification

- Sends OTP using secure SMTP
- Verifies submitted OTP
- Prevents account activation until verification succeeds
- Expires invalid or outdated codes

---

## 3. User Login

- Authenticates registered users
- Verifies password using bcrypt
- Creates JWT session token
- Grants secure dashboard access

---

## 4. Password Recovery

- Verifies registered email
- Generates recovery OTP
- Allows secure password reset
- Stores updated password as bcrypt hash

---

## 5. Protected Dashboard

Authenticated users can access:

- Team wellness overview
- Emotional polarity insights
- Historical trend analysis
- Organizational wellness metrics
- Data visualization charts

---

# Security Features

- bcrypt password hashing
- JWT authentication
- OTP email verification
- Session protection
- Secure SMTP communication
- Email uniqueness validation
- Username uniqueness validation
- Protected dashboard access
- Token expiration management

---

# Application Workflow

```text
User Registration
        │
        ▼
Email Validation
        │
        ▼
OTP Generation
        │
        ▼
Email Verification
        │
        ▼
Account Activation
        │
        ▼
Secure Login
        │
        ▼
JWT Session Created
        │
        ▼
Protected Dashboard
        │
        ▼
Emotional Analysis &
Well-being Recommendations
```

---

# Project Objectives

- Analyze emotional tone from textual communication.
- Support employee wellness initiatives.
- Improve organizational awareness through emotional analytics.
- Deliver secure authentication and user management.
- Maintain privacy through encrypted credential storage.
- Provide scalable cloud-based infrastructure.

---

# Privacy and Security

MoodMentor prioritizes user privacy through multiple security layers:

- Passwords are never stored in plain text.
- Authentication uses JWT-based authorization.
- OTP verification prevents unauthorized account activation.
- Secure SMTP protocols protect email communication.
- PostgreSQL ensures reliable relational data management.

---

---

# Use Cases

MoodMentor can be applied in:

- Corporate wellness programs
- Human Resources analytics
- Employee engagement monitoring
- Organizational research
- Workplace mental well-being 
- Internal communication analysis

---

# License

