# 🎓 University Examination System

This project presents a **relational database schema** for a University Examination System. It is designed to manage and maintain information about departments, faculty members, students, courses, and examinations. The system is built using standard SQL with proper entity relationships and constraints.

---

## 🗃️ Features and Entities

### 📌 Department
- Each department has a unique name.
- Headed by a faculty member (who may have other roles too).
- Offers multiple courses.

### 👨‍🏫 Faculty
- Has an Employee ID, Name, and Designation.
- Can **teach multiple courses**, **coordinate a course**, and **head a department** simultaneously.

### 📚 Course
- Each course has a unique `Course_Code`, `Title`, and belongs to a department.
- Coordinated by a faculty member.
- Taught by multiple faculty members.

### 👨‍🎓 Student
- Identified by `Roll_No` and `Name`.
- Belongs to one department.
- Can enroll in multiple courses (from their department).
- Each enrollment tracks `Attendance_Percentage`.

### 📝 Exam
- Created by a faculty member.
- Linked to a specific course.
- Stores `Title`, `Subject_Name`, `Duration`, `Date`, and `Exam_Type` (Internal or External).

### 🎯 Student Exam Attempt
- Students can appear in multiple exams.
- Multiple attempts allowed per exam.
- Tracks `Attempt_Date` and `Marks`.

---

## 🛠️ SQL Tables Overview

- `Department`
- `Faculty`
- `Course`
- `Faculty_Course_Teaching` (many-to-many between faculty and courses)
- `Student`
- `Student_Course_Enrollment` (many-to-many with attendance tracking)
- `Exam` (created by faculty, tied to a course)
- `Student_Exam_Attempt` (captures student attempts with marks)

---

## ⚙️ Schema Relationships

| Relationship | Description |
|--------------|-------------|
| Department–Faculty | One-to-one (head of department) |
| Department–Course | One-to-many |
| Faculty–Course | Many-to-many (teaching) |
| Faculty–Coordinator | One-to-one (each course has one coordinator) |
| Student–Department | Many-to-one |
| Student–Course | Many-to-many (with attendance) |
| Faculty–Exam | Many-to-many (via creation) |
| Exam–Course | Many-to-one |
| Student–Exam | Many-to-many with attempts |

---

## 🧪 Example Use Cases

- Track which faculty member coordinates or teaches which courses.
- Monitor student attendance across courses.
- Record multiple exam attempts per student with marks.
- Link exams to their respective creators and subjects.

---

## 🧰 Technologies Used

- SQL (MySQL / PostgreSQL compatible)
- Relational Database Design
- ER Modeling & Normalization

---

## 📂 How to Use

1. Clone this repository.
2. Import SQL schema into your RDBMS.
3. Extend or populate with sample data for testing or development.

---

Feel free to ⭐ star or fork this repository for academic or real-world extension projects.


  ![image](https://github.com/user-attachments/assets/2fd33799-bf2b-43e4-8463-28db00ce40b3)
  ![image](https://github.com/user-attachments/assets/bee4df01-92d5-4a50-94fb-8939a2b95c0c)


