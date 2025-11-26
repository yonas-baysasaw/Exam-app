# 🛠️ Exam Prep App – Backend (Django)

This repository contains the backend service for the **Exam Prep App**, a mobile/web application that provides students with organized access to past exam papers across Natural Science and Social Science streams.

The backend is built using **Django** and provides APIs for departments, subjects, and exam papers, with clean, scalable architecture suitable for future features.

---

# 📌 Project Purpose

The backend powers the main functionalities of the Exam Prep App:

- Manage **departments** (Natural, Social)
- Manage **subjects** under each department
- Store and serve **past exam papers** with file URLs
- Provide secure REST APIs for the frontend (mobile/web)
- Handle authentication (optional)
- Serve structured JSON responses

---

# 📁 Features (Backend-Specific)

### ✅ Department Management
- Create and list Natural / Social departments.

### ✅ Subject Management
- Each subject linked to a department.

### ✅ Exam Paper Management
- Upload or link past exam files (PDF, images, documents)
- Organize by subject and year
- Provide file access to the frontend

### ✅ API Endpoints
- REST API for frontend consumption
- Department → Subject → Exam Paper structure
- Pagination & filtering support

### ✅ Clean Django Architecture
- Modular app structure
- DRF serializers & viewsets
- Optional JWT authentication support

---

# 🧱 Data Model (Django)

### **departments**
| Field | Type | Description |
|------|------|-------------|
| department_id | UUID | Primary key |
| department_name | CharField | Natural / Social |

### **subjects**
| Field | Type | Description |
|------|------|-------------|
| subject_id | UUID | Primary key |
| subject_name | CharField | Subject name |
| department | FK | Linked to department |

### **exam_papers**
| Field | Type | Description |
|------|------|-------------|
| paper_id | UUID | Primary key |
| subject | FK | Linked to subject |
| year | Integer | Exam year |
| file_url | URL/FileField | Link to stored file |
| description | TextField | Optional |
| uploaded_at | DateTime | Timestamp |

---

# 📦 Tech Stack

### **Backend**
- Django 5+
- Django REST Framework (DRF)
- PostgreSQL / SQLite / MySQL (your choice)
- Django CORS Headers
- Python 3.10+

### **File Storage Options**
- Local storage (development)
- AWS S3 / Cloudinary / Firebase Storage (production)

---

# 🧩 Project Structure

