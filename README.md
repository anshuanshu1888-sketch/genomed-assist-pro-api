# 🏥 Genomed Assist Pro API

A secure healthcare management backend built with **FastAPI** for managing doctors, patients, and appointments.

> **Version:** 2.1
>
> **Status:** Prototype / Educational Project

---

## Overview

Genomed Assist Pro API is a backend healthcare management system developed as a learning project.

It demonstrates:

- REST API development
- JWT Authentication
- Secure password hashing with bcrypt
- Patient record management
- Appointment scheduling
- Data encryption using Fernet
- SQLite database integration
- FastAPI backend architecture

This project focuses on secure backend development practices rather than providing medical advice.

---

## Features

### Doctor Management

- Doctor Registration
- Secure Login
- JWT Authentication
- Doctor Profile

### Patient Management

- Add Patient
- View Patients
- View Individual Patient
- Delete Patient
- Encrypted Diagnosis Storage

### Appointment Management

- Book Appointment
- View Appointments
- Update Appointment Status

### Security

- bcrypt password hashing
- JWT authentication
- Fernet encryption
- Environment variable configuration
- Protected API endpoints

### User Experience

- Tutorial endpoint
- FAQ endpoint
- Health check endpoint

---

## Technology Stack

- Python
- FastAPI
- SQLite
- JWT
- Passlib (bcrypt)
- Cryptography (Fernet)
- Pydantic
- Uvicorn
- Python-dotenv

---

## Project Structure

```
genomed-assist-pro-api/
│
├── main.py
├── requirements.txt
├── README.md
├── LICENSE
├── .env.example
└── genomed.db
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/anshuanshu1888-sketch/genomed-assist-pro-api.git

cd genomed-assist-pro-api
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Create Environment File

Create a file named:

```
.env
```

Example:

```
GENOMED_SECRET_KEY=your_secret_key

GENOMED_ENCRYPTION_KEY=your_encryption_key
```

### Run Server

```bash
python main.py
```

or

```bash
uvicorn main:app --reload
```

---

## API Endpoints

### General

| Method | Endpoint |
|---------|----------|
| GET | / |
| GET | /health |

---

### Doctors

| Method | Endpoint |
|---------|----------|
| POST | /doctor/register |
| POST | /doctor/login |
| GET | /doctor/profile |
| GET | /doctor/my-patients |

---

### Patients

| Method | Endpoint |
|---------|----------|
| POST | /patient/add |
| GET | /patients |
| GET | /patient/{id} |
| DELETE | /patient/{id} |

---

### Appointments

| Method | Endpoint |
|---------|----------|
| POST | /appointment/book |
| GET | /appointments |
| PUT | /appointment/{id} |

---

### Help

| Method | Endpoint |
|---------|----------|
| GET | /tutorial |
| GET | /tutorial/again |
| GET | /help |
| GET | /faq |

---

## Authentication

Protected endpoints require a JWT Bearer Token.

Example:

```
Authorization: Bearer YOUR_ACCESS_TOKEN
```

---

## Security Features

- bcrypt password hashing
- JWT authentication
- Encrypted medical data
- Environment variable support
- Secure password verification

---

## Medical Disclaimer

Genomed Assist Pro is a prototype healthcare management system created for educational purposes.

It does **not** provide medical diagnosis or replace professional healthcare advice.

Always consult qualified healthcare professionals for medical decisions.

---

## Current Status

Current Version:

**v2.1**

Implemented:

- Doctor authentication
- Patient management
- Appointment management
- Encryption
- Tutorial system
- FAQ system
- Health check

---

## Contributing

Contributions, suggestions, and issue reports are welcome.

If you find bugs or have improvement ideas, feel free to open an Issue or Pull Request.

---

## License

This project is licensed under the MIT License.

See the LICENSE file for details.

---

## Author

**Anshu**

Independent Student Developer

India

---

## Acknowledgements

Built using:

- FastAPI
- Passlib
- Cryptography
- SQLite
- Pydantic
- Uvicorn

Special thanks to the open-source community for making these tools freely available.

---

⭐ If you found this project interesting, consider giving it a star.
