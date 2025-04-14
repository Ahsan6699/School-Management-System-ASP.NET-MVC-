# 🎓 School Management System (ASP.NET MVC)

This is a simple **School Management System** built using **ASP.NET MVC**. It allows the management of **Students** and their associated **Enrollments** using a **ViewModel-centric** approach with dynamic add/delete functionality in the UI.

---

## 🚀 Features

- Full **CRUD operations for students**  
- Dynamically manage **enrollments** during create/edit actions  
- Uses a **ViewModel (StudentVM)** to structure and pass data between View and Controller  
- Enrollment list add/delete handled via an `Operation` string  
- Uses **Entity Framework** for database interactions  

---

## 📁 Project Structure

**ViewModel/StudentVM.cs**  
Contains the ViewModel for students, including transformation logic between the domain model and the view model.

**Controllers/StudentsController.cs**  
Handles all student-related operations such as Create, Read, Update, and Delete — including dynamic list actions for enrollments.

---

## 💡 How It Works

### Student Creation

- On **Create**, enrollments are added or removed dynamically using the `Operation` field (e.g., `Add`, `Delete-0`)  
- `StudentVM` is converted into a `Student` entity before being saved  

### Student Editing

- Existing student is removed and a new one is saved with updated enrollments  
- Ensures consistency and prevents orphaned records  

---

## 🛠️ Tech Stack

- ASP.NET MVC 5  
- Entity Framework 6  
- C#  
- Razor Views  
