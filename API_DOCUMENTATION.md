# Genomed Assist Pro API Documentation

![Version](https://img.shields.io/badge/version-v2.1-blue)
![Python](https://img.shields.io/badge/Python-3.11+-green)
![FastAPI](https://img.shields.io/badge/FastAPI-Latest-success)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

# Overview

Genomed Assist Pro is an AI-assisted **Clinical Decision Support System (CDSS)** developed for educational, research, and open-source collaboration.

The platform is designed to assist healthcare professionals with:

- Patient Record Management
- Medical Image Analysis Support
- Prescription History Management
- AI-Assisted Clinical Summaries
- Doctor Authentication
- Audit Logging
- Drug Recommendation Support

> **Important**
>
> Genomed Assist Pro is **NOT a replacement for physicians.**
>
> AI-generated outputs are clinical decision support recommendations only and must always be reviewed by a licensed healthcare professional.

---

# Version

**Current Version:** v2.1

---

# Base URL

### Development

```
http://localhost:8000
```

### Production

Currently not deployed.

This project is intended for local development, educational demonstrations, and open-source collaboration.

---

# Interactive API Documentation

After running the FastAPI server:

### Swagger UI

```
http://localhost:8000/docs
```

### ReDoc

```
http://localhost:8000/redoc
```

---

# Authentication

The API uses **JWT (JSON Web Token)** authentication.

## Login

**POST**

```
/doctor/login
```

### Example Request

```json
{
  "username": "doctor1",
  "password": "Doctor123!"
}
```

### Example Response

```json
{
  "access_token": "JWT_TOKEN",
  "token_type": "bearer"
}
```

---

# Doctor Endpoints

## Register Doctor

**POST**

```
/doctor/register
```

Example

```json
{
  "username": "doctor3",
  "password": "StrongPassword123!",
  "name": "Dr Emily Carter",
  "specialization": "Neurology"
}
```

Response

```json
{
  "message": "Doctor registered successfully"
}
```

---

## Login Doctor

**POST**

```
/doctor/login
```

Returns a JWT Access Token for authenticated requests.

---

# Patient Endpoints

## Add Patient

**POST**

```
/patient/add
```

Example

```json
{
  "id": "P001",
  "name": "John Doe",
  "age": 45,
  "sex": "Male"
}
```

---

## View Patient

**GET**

```
/patient/{patient_id}
```

Example

```
/patient/P001
```

---

# Prescription Endpoints

## Save Prescription

**POST**

```
/prescription/add
```

Example

```json
{
  "patient_id": "P001",
  "doctor_username": "doctor1",
  "drug_name": "Metformin",
  "dosage": "500 mg",
  "frequency": "Twice Daily",
  "duration": "30 Days",
  "reason": "Type 2 Diabetes"
}
```

---

## View Prescriptions

**GET**

```
/prescriptions
```

---

# Medical Image Endpoints

## Analyze Medical Image

**POST**

```
/image/analyze
```

Supported medical documents include:

- X-Ray
- MRI
- CT Scan
- Ultrasound
- ECG
- Blood Test Report
- Urine Test
- Liver Function Test
- Kidney Function Test
- Prescription Images

AI-generated findings are stored in the patient record for physician review.

---

# Audit Log

**GET**

```
/audit
```

Tracks:

- Doctor Login
- Patient Registration
- Prescription History
- Medical Image Analysis
- Record Updates

---

# Health Check

**GET**

```
/
```

Example Response

```json
{
  "system": "Genomed Assist Pro",
  "mode": "Clinical Decision Support ONLY",
  "status": "running"
}
```

---

# Demo Accounts

## Doctor 1

Username

```
doctor1
```

Password

```
Doctor123!
```

---

## Doctor 2

Username

```
doctor2
```

Password

```
Doctor123!
```

---

# HTTP Response Codes

| Code | Meaning |
|------|---------|
| 200 | Success |
| 201 | Created |
| 400 | Bad Request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

---

# Technology Stack

- Python
- FastAPI
- OpenAI API
- SQLite / JSON Storage (current development version)
- JWT Authentication
- Passlib
- Bcrypt
- Pydantic
- Uvicorn

---

# Security Features

- JWT Authentication
- Password Hashing using bcrypt
- Audit Logging
- Input Validation using Pydantic
- Secure Doctor Authentication
- Clinical Decision Support (CDSS) Architecture

---

# Current Project Structure

```
genomed-assist-pro-api/

├── app.py
├── requirements.txt
├── README.md
├── API_DOCUMENTATION.md
├── LICENSE
├── genomed_hospital.json
└── .gitignore
```

---

# Disclaimer

Genomed Assist Pro is an educational and research project created to demonstrate secure healthcare backend development and AI-assisted Clinical Decision Support.

This software **does not diagnose diseases, prescribe medications, or replace licensed healthcare professionals.**

All AI-generated outputs are recommendations only and must be independently verified by qualified physicians before clinical use.

---

# License

Released under the **MIT License**.

---

# Author

**Anshu**

Independent AI/ML Researcher

Open-Source Healthcare AI Developer

GitHub:

https://github.com/anshuanshu1888-sketch/genomed-assist-pro-api
