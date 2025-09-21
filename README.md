# Enterprise-Cloud-Architecture

An enterprise-grade application for educational institutions, designed using a microservices architecture with Spring Boot and React. The system highlights modern distributed design patterns and supports deployment across multiple cloud platforms.

<p align="left">
  <strong>👤 Dimuth Hirushan</strong><br>
  🎓 Student ID: <code>2301682090</code><br>
  📧 Email: <>dimuthsamaranayaka756@gmail.com</a>
</p>

## 📺 Demo Video
[**Watch Project Demo**](https://drive.google.com/file/d/1oO1yEvJao6yhiZX4ZmfwTIl-2-QvTrlt/view?usp=sharing)

## About the Project

This is a **microservices architecture** project consisting of:

- **Course Service** (Port: 8081) - Course management with MySQL database
- **Student Service** (Port: 8082) - Student management with MongoDB database
- **Media Service** (Port: 8083) - File upload and media management
- **Frontend App** (Port: 5173) - React with TypeScript and Material-UI

### Technology Stack
- **Backend**: Spring Boot 3.5.5, Java 21, Maven
- **Frontend**: React 18, TypeScript, Vite, Material-UI
- **Databases**: MySQL, MongoDB
- **Cloud**: AWS, GCP deployment configurations

## How to Run

### Prerequisites
- Java 21
- Node.js 18+
- Maven 3.8+
- MySQL Server
- MongoDB

### 1. Clone Repository
```bash
git clone https://github.com/DmHirushan/ECA.git
cd Enterprise-Cloud-Architecture
```

### 2. Database Setup

**MySQL (Course Service):**
```sql
CREATE DATABASE eca_courses;
CREATE USER 'eca_user'@'localhost' IDENTIFIED BY 'eca_password';
GRANT ALL PRIVILEGES ON eca_courses.* TO 'eca_user'@'localhost';
```

**MongoDB (Student Service):**
```bash
# Start MongoDB on port 16000
mongod --port 16000
```

### 3. Start Services

**Backend Services:**
```bash
# Build all services
mvn clean install

# Start Course Service (Terminal 1)
cd course-service && mvn spring-boot:run

# Start Student Service (Terminal 2)  
cd student-service && mvn spring-boot:run

# Start Media Service (Terminal 3)
cd media-service && mvn spring-boot:run
```

**Frontend Application:**
```bash
# Terminal 4
cd frontend-app
npm install
npm run dev
```

### 4. Access Application
- **Frontend**: http://localhost:5173
- **Course Service**: http://localhost:8081
- **Student Service**: http://localhost:8082
- **Media Service**: http://localhost:8083

## Project Structure
```
Enterprise-Cloud-Architecture/
├── course-service/          # Course management microservice
├── student-service/         # Student management microservice
├── media-service/          # Media/file management microservice
├── frontend-app/           # React frontend application
├── pom.xml                # Parent Maven configuration
└── README.md
```
