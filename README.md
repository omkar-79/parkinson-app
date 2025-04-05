# Parkinson's Tracking System

A comprehensive medical tracking system for monitoring Parkinson's disease patients, featuring a web dashboard for doctors, real-time data processing, and secure data storage.

**Youtube Video Link:-** https://youtu.be/uiO4Wf9B4lc

## System Architecture

The system consists of several microservices:

- **Web Dashboard** ([`web_app`](web_app/)) - Next.js frontend for doctors
- **Backend API** ([`backend`](backend/)) - FastAPI service handling authentication and data
- **Processing Service** ([`processing`](processing/)) - ML-based analysis of patient data
- **Database** ([`database`](database/)) - PostgreSQL database with medical records

## Getting Started

### Prerequisites

- Docker and Docker Compose
- Node.js 19+ (for local development)
- Python 3.9+ (for local development)
- PostgreSQL 13+ (for local development)

### Installation

1. Clone the repository:
```sh
git clone https://github.com/omkar-79/parkinson-app.git
cd parkinson-tracking-system
```

2. Start the services using Docker Compose:
```sh
cd backend
docker-compose build
docker-compose up -d
```

3. The following services will be available:
- Web Dashboard: http://localhost:3000
- Backend API: http://localhost:8000
- Database: localhost:5432

### Development Setup

#### Web Dashboard

```sh
cd web_app
npm install
npm run dev
```



## Features

- **Doctor Dashboard**
  - Patient management
  - Real-time data visualization
  - Test results tracking
  - Secure authentication

- **Patient Data Processing**
  - Clock Drawing Test (CDT) analysis
  - Speech processing
  - Movement analysis
  - Real-time scoring


## Database Schema

The PostgreSQL database includes tables for:
- Doctors
- Patients
- Test Records
- Images


