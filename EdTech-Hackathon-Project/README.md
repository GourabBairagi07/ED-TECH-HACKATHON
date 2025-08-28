# EdTech-Hackathon-Project
# ED-TECH-HACKATHON

# EdTech Hackathon Project

## Project Overview
This is a hackathon-level EdTech platform where learners can access 100+ technical courses, track their progress, take quizzes, and receive certificates upon course completion. The system includes adaptive learning recommendations powered by a Flask ML microservice and a Node.js backend API.  

**Team Roles:**
- **Gourab (Leader):** Backend + Flask ML microservice + Certificate generation  
- **Sukanya:** Frontend UI (React + Tailwind) + Database setup  
- **Debasis:** Frontend support + minor ML visualizations + Database integration  
- **Senior Integrators/Testers:** Integration, debugging, testing  

---

## Project Directory Structure

### **1. Backend**
**Folder:** `backend/`

#### Node.js (Core API)
- **`app.js`** → Entry point for Express server  
- **`routes/`** → API endpoints  
  - `authRoutes.js` → Signup/Login APIs  
  - `courseRoutes.js` → Course APIs (list, details, progress)  
  - `certificateRoutes.js` → Certificate generation/download APIs  
- **`controllers/`** → Logic for API endpoints  
- **`models/`** → Database schemas (User, Course, Progress)  
- **`services/`** → Helper services (certificate generation, progress tracking)  
- **`config/`** → DB connection (`db.js`), Firebase setup (`firebase.js`)  
- **`utils/`** → Helper functions  
- **`.env`** → Environment variables (DB credentials, API keys)  

**Member Responsibility:**  
- **Gourab** develops APIs, certificate logic, and backend integration with Flask ML microservice.  
- **Debasis** can assist with database integration and minor API testing.  

---

#### Flask (ML / Recommendations)
- **`app.py`** → Entry point for Flask ML microservice  
- **`models/`** → ML models (`recommendation_model.py`, `difficulty_model.py`)  
- **`routes/`** → Endpoints for recommendations and analytics  
- **`utils/`** → Preprocessing and helper scripts  
- **`datasets/`** → Static datasets for testing (e.g., `courses.csv`, `student_activity.csv`)  

**Member Responsibility:**  
- **Gourab** develops ML models and endpoints.  
- **Debasis** can assist with ML visualizations (20–30%).  

---

### **2. Frontend**
**Folder:** `frontend/`

- **`public/`** → Static files (HTML, favicon, images)  
- **`src/`**  
  - `index.js` & `App.js` → Main React files  
  - `assets/` → Images, logos, icons  
  - `components/` → Reusable components (Navbar, Footer, CourseCard, CertificateDownload)  
  - `pages/` → Main pages (Home, Courses, CourseDetail, Profile, Certificate, AdminDashboard)  
  - `services/api.js` → API calls to Node.js backend  
  - `styles/` → Tailwind and custom CSS  

**Member Responsibility:**  
- **Sukanya** builds pages and connects to APIs.  
- **Debasis** assists with components and minor ML visualizations.  

---

### **3. Certificates**
**Folder:** `certificates/`  
- Stores dynamically generated PDF certificates for users.  
- Example files: `Gourab_Bairagi_DS.pdf`, `User_XYZ_Java.pdf`  

**Member Responsibility:**  
- **Gourab** generates certificates through Node.js backend.  

---

### **4. Datasets**
**Folder:** `datasets/`  
- Static datasets for hackathon use, e.g., `courses.csv`, `sample_users.csv`  
- Used for ML training, course population, and demo data.  

**Member Responsibility:**  
- **Gourab** prepares datasets for ML microservice.  
- **Sukanya & Debasis** can use datasets to populate frontend for demo.  

---

### **5. Docs**
**Folder:** `docs/`  
- `README.md` → Project overview & instructions  
- `PROJECT_PLAN.md` → Timeline, roles, task assignments  
- `API_DOCS.md` → API endpoints documentation  

**Member Responsibility:**  
- All members contribute documentation updates.  

---

### **6. Version Control**
- Use **Git** with separate branches for each member:
  - `backend-node` → Gourab  
  - `frontend` → Sukanya  
  - `frontend-support` → Debasis  
- Seniors handle **merge, integration, debugging, and final testing**.  

---

### **7. Development Guidelines**
- Always pull latest changes before starting work.  
- Use mock APIs if the other module is not ready.  
- Keep consistent coding style and naming conventions.  
- For hackathon MVP, focus on **core functionality first**:  
  - Signup/Login → Course list → Quiz → Progress → Certificate  

---

**By following this structure, each team member can work independently, while integration is smooth and efficient.**
