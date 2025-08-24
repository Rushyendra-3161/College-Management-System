# College Management System (FastAPI)


A production-ready starter for a College Management System built with **FastAPI**, **SQLAlchemy**, and **JWT** auth.
Includes role-based access control (Admin / Teacher / Student), and modules for courses, enrollments, attendance, and grades.


## Features
- User auth with JWT (password hashing, token refresh pattern ready)
- Role-Based Access Control (RBAC): Admin, Teacher, Student
- Entities: Users, Courses, Enrollments, Attendance, Grades
- Pagination, filtering, and basic validation
- .env-based configuration (SQLite by default; Postgres ready via Docker Compose)
- CORS enabled; structured routers per domain
- Ready-to-dockerize with `Dockerfile` + `docker-compose.yml`


## Quickstart (Local)
1. **Python 3.10+** recommended. Create and activate a virtualenv.
2. Install deps:
```bash
pip install -r requirements.txt
```
3. Create a .env (copy from .env.example) and edit values as needed.
4. Run:
```bash
uvicorn app.main:app --reload
```
5. Visit: http://127.0.0.1:8000/docs

## Quickstart (Docker + Postgres)
```bash
cp .env.example .env   # edit secrets
docker compose up --build
```

## Default Roles & Access
- Admin: manage users, courses, everything.
- Teacher: manage own courses; mark attendance & grades for their courses.
- Student: view own enrollments, attendance, and grades.
