
# 🏥Console-Based Hospital Management System 

A simple **Hospital Management System** built using **Core Java**, **JDBC**, and **MySQL** to manage patients, doctors, appointments, and billing.

---

## 📌 Features

- Add, view, update, and delete:
  - Patients
  - Doctors
  - Appointments
  - Bills
- Search patient or doctor by name or ID
- Relational database using MySQL
- Uses **JDBC** for database communication
- Menu-driven console interface

---

## 🛠 Technologies Used

- **Java** (Core Java)
- **JDBC** (Java Database Connectivity)
- **MySQL** (RDBMS)
- **IntelliJ IDEA / Eclipse** (Recommended IDE)

---

## 🗃 Database Schema

### Tables

#### 🧑‍⚕️ `doctors`
| Column     | Type        | Description           |
|------------|-------------|-----------------------|
| id         | INT (PK)    | Doctor ID             |
| name       | VARCHAR     | Doctor Name           |
| specialization | VARCHAR | Area of specialization|
| phone      | VARCHAR     | Contact number        |

#### 🧑‍🤝‍🧑 `patients`
| Column     | Type        | Description     |
|------------|-------------|-----------------|
| id         | INT (PK)    | Patient ID      |
| name       | VARCHAR     | Patient Name    |
| age        | INT         | Age             |
| gender     | VARCHAR     | Gender          |
| disease    | VARCHAR     | Diagnosed Issue |

#### 📅 `appointments`
| Column     | Type        | Description       |
|------------|-------------|-------------------|
| id         | INT (PK)    | Appointment ID    |
| patient_id | INT (FK)    | Linked to patient |
| doctor_id  | INT (FK)    | Linked to doctor  |
| date       | DATE        | Appointment Date  |

#### 💳 `bills`
| Column     | Type        | Description      |
|------------|-------------|------------------|
| id         | INT (PK)    | Bill ID          |
| patient_id | INT (FK)    | Linked to patient|
| amount     | DOUBLE      | Total Amount     |
| date       | DATE        | Billing Date     |

---

## 🚀 How to Run

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/hospital-management-system.git
   cd hospital-management-system

  ```
---
## 2 Setup MySQL Database

- Create a database (e.g., hospital_db)

- Import the SQL schema provided in the /sql folder

---

## 3 Update Database Credentials
- In the Java file where JDBC connection is configured, update:
```
String url = "jdbc:mysql://localhost:3306/hospital_db";
String user = "root";
String password = "yourpassword";
```
---
## 4. Compile and Run

- Open in IntelliJ or any Java IDE

- Run the Main.java or HospitalManagementSystem.java file

---

## 📂 Project Structure
- (We can create project structure Dao, Pojo, Utility layer )

hospital-management-system/
├── src/
│   ├── model/
│   │   ├── Doctor.java
│   │   ├── Patient.java
│   │   └── Appointment.java
│   ├── dao/
│   │   ├── DoctorDAO.java
│   │   ├── PatientDAO.java
│   │   └── AppointmentDAO.java
│   ├── util/
│   │   └── DBConnection.java
│   └── HospitalManagementSystem.java
├── sql/
│   └── schema.sql
└── README.md

---

📜 License
This project is open-source and available under the MIT License.




