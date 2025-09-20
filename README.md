Cloud-Enabled Deployment in Action with AWS

This repository demonstrates a cloud-enabled full-stack deployment using Spring Boot, React, and AWS.
It consists of four independent projects working together:

course-service → Spring Boot + MySQL

student-service → Spring Boot + MongoDB

media-service → Spring Boot + Local/S3/MinIO file storage

frontend-app → React + TypeScript

📌 Project Overview
1. Course Service (Spring Boot + MySQL)

Entity: Course(id, name, duration)

REST Endpoints:

GET /courses → Fetch all courses

GET /courses/{id} → Fetch course by ID

POST /courses → Add new course

DELETE /courses/{id} → Delete course

Default Port: 8081

Configuration: Requires MySQL settings

2. Student Service (Spring Boot + MongoDB)

Document: Student(registrationNumber, fullName, address, contact, email)

REST Endpoints:

GET /students → Fetch all students

GET /students/{id} → Fetch student by ID

POST /students → Add new student

DELETE /students/{id} → Delete student

Default Port: 8082

Configuration: Requires MongoDB settings

3. Media Service (Spring Boot + File Storage)

Resource: files

REST Endpoints:

POST /files → Upload file (multipart/form-data)

GET /files → List all uploaded files

GET /files/{id} → Download specific file

DELETE /files/{id} → Delete file

Default Port: 8083

Storage:

By default → ./data/media (local disk)

Can override with env var → MEDIA_STORAGE_DIR

Extendable to AWS S3 / MinIO

4. Frontend Application (React + TypeScript + Vite + MUI)

Sections: Courses | Students | Media

Built with: React, TypeScript, MUI, Axios, Vite

Scripts:

npm run dev → Start Vite dev server

npm run build → TypeScript + Vite production build

npm run preview → Preview production build

⚙️ Build & Deployment

Each service can be built and deployed separately.
Ensure that databases (MySQL, MongoDB) are configured before starting backend services.
The frontend consumes APIs from the above services.

👤 Student Information

Name: Your Name Here

Student ID: Your Student ID Here

🎥 Demo Video

Watch the demo video here: Demo Video Link

- Backend: run `mvn -q -e -DskipTests package` at repo root to build services.
- Frontend: run `npm install` then `npm run dev` inside `frontend-app`.
