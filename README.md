# javaproject
Campus Course &amp; Records Manager (CCRM)
![Java](https://img.shields.io/badge/Java-17%2B-orange?style=flat-square&logo=java)
![Platform](https://img.shields.io/badge/Platform-CLI-lightgrey?style=flat-square)
![License](https://img.shields.io/badge/License-Educational-blue?style=flat-square)

A comprehensive console-based Java SE application for managing academic records, built to demonstrate advanced Java programming concepts and modern software development practices.

## ✨ Features

### 📊 Core Management
- **Student Management**: Add, update, list, and deactivate student records
- **Course Administration**: Comprehensive course catalog management
- **Enrollment System**: Handle course enrollments and withdrawals
- **Grade Recording**: Input and manage student grades with GPA calculation
- **Transcript Generation**: Generate detailed academic transcripts

### 🔄 Data Operations
- **CSV Import/Export**: Bulk data operations using CSV files
- **Automated Backups**: Timestamped backup system with recursive operations
- **Data Validation**: Robust input validation and error handling

### 📈 Reporting & Analytics
- **GPA Distribution**: Statistical analysis of student performance
- **Top Students**: Identify high-performing students
- **Academic Reports**: Comprehensive reporting capabilities

## 🏗️ Architecture Highlights

### Design Patterns Implemented
| Pattern | Implementation | Purpose |
|---------|----------------|---------|
| **Singleton** | `AppConfig`, `DataStore` | Centralized configuration and data management |
| **Builder** | `Course.Builder`, `Transcript.Builder` | Flexible object creation with fluent interface |
| **Service Layer** | `StudentService`, `CourseService` | Separation of business logic |

### Key Java Concepts Demonstrated
- **OOP Principles**: Encapsulation, Inheritance, Abstraction, Polymorphism
- **Advanced Features**: Lambdas, Streams, NIO.2, Date/Time API
- **Exception Handling**: Custom exceptions with proper error management
- **Collections Framework**: Advanced data structures and algorithms

## 🚀 Quick Start

### Prerequisites
- **JDK 17 or higher** installed
- Java added to PATH environment variable

### Installation & Compilation

#### Using PowerShell
```powershell
# Create output directory
mkdir out

# Compile all Java files
javac -d out -encoding UTF-8 $(Get-ChildItem -Recurse src\main\java\*.java | ForEach-Object { $_.FullName })

# Run the application
java -cp out edu.ccrm.cli.Main
```

### Project Structure
```
src/main/java/edu/ccrm/
├── cli/                 # Command-line interface
├── domain/              # Core domain models
│   ├── Person.java      # Abstract base class
│   ├── Student.java     # Student entity
│   ├── Course.java      # Course with Builder pattern
│   └── Enrollment.java  # Enrollment management
├── service/             # Business logic layer
├── io/                  # Import/export operations
├── util/                # Utilities and helpers
└── config/              # Configuration management
```
