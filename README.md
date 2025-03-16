# Parkinson's Tracking System

A comprehensive medical tracking system for monitoring Parkinson's disease patients, featuring a web dashboard for doctors, real-time data processing, and secure data storage.

## System Architecture

The system consists of several microservices:

- **Web Dashboard** ([`web_app`](web_app/)) - Next.js frontend for doctors
- **Backend API** ([`backend`](backend/)) - FastAPI service handling authentication and data
- **Processing Service** ([`processing`](processing/)) - ML-based analysis of patient data
- **Database** ([`database`](database/)) - PostgreSQL database with medical records
- **Nginx** ([`nginx`](nginx/)) - Reverse proxy for routing requests

## Getting Started

### Prerequisites

- Docker and Docker Compose
- Node.js 19+ (for local development)
- Python 3.9+ (for local development)
- PostgreSQL 13+ (for local development)

### Installation

1. Clone the repository:
```sh
git clone git@github.com:omkar-79/parkinson-app.git
cd parkinson-tracking-system
```

2. Start the services using Docker Compose:
```sh
docker-compose up -d
```

3. The following services will be available:
- Web Dashboard: http://localhost:3000
- Backend API: http://localhost:8000
- Database: localhost:5432
- Nginx: http://localhost:80

### Development Setup

#### Web Dashboard

```sh
cd web_app
npm install
npm run dev
```

#### Backend API

```sh
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

#### Processing Service

```sh
cd processing
pip install -r requirements.txt
python server.py
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

- **Security**
  - JWT-based authentication
  - Role-based access control 
  - Encrypted data storage
  - HIPAA compliance measures

## API Documentation

The backend API documentation is available at:
- Swagger UI: http://localhost:8000/docs
- ReDoc: http://localhost:8000/redoc

## Database Schema

The PostgreSQL database includes tables for:
- Doctors
- Patients
- Test Records
- Medical Data

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

Your Name - your.email@example.com
Project Link: https://github.com/omkar-79/parkinson-app
