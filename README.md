Campus Course & Records Manager (CCRM)

A console-based Java SE application for managing students, courses, enrollments, grades, and academic records.
This project demonstrates Java fundamentals, OOP concepts, advanced APIs, design patterns, and file handling.

📌 Features

Student Management → Add, list, update, deactivate students
Course Management → Add, list, update, assign instructors, filter/search with Streams
Enrollment & Grades → Enroll students, assign grades, calculate GPA, print transcripts
File Operations → Import/export data (CSV), backup system with timestamps
Reports → Recursive folder size calculation, GPA distributions, listing backups
Menu-Driven CLI → Simple interactive console with switch and loops


🛠️ Technologies Used

Java SE 21 (JDK 21)
OOP (Abstraction, Inheritance, Encapsulation, Polymorphism)
Java NIO.2 for file I/O
Date/Time API for enrollment dates & backup timestamps
Streams & Lambdas for reports and filtering

🚀 How to Compile & Run

From project root:

# Compile all .java files into 'out/' directory
javac -d out src/edu/ccrm/**/*.java

# Run the program
java -cp out edu.ccrm.cli.Main

If using VS Code with Java Extension Pack:
Right-click Main.java → Run Java

📂 Project Structure
src/edu/ccrm/
 ├─ cli/          # CLI entry point (Main.java)
 ├─ domain/       # Entities: Student, Instructor, Course, Enrollment, Enums
 ├─ service/      # Business logic interfaces + implementations
 ├─ io/           # Import/Export, Backup services
 ├─ util/         # Validators, Comparators, Recursion utilities
 └─ config/       # AppConfig (Singleton), CourseBuilder (Builder Pattern)

📖 Required Notes

1. Evolution of Java (Timeline)

1995 → Java 1.0 released by Sun Microsystems
2004 → Java 5 (Generics, Annotations, Enums)
2014 → Java 8 (Lambdas, Streams, Date/Time API)
2017 → Java 9 (Modules, JShell)
2018 → Oracle shifts to 6-month release cycle
2021 → Java 17 (LTS) released
2023 → Java 21 (LTS) released with Virtual Threads (Project Loom)

2. Java Editions (ME vs SE vs EE)
| Edition                  | Purpose            | Example Use Cases                        |
| ------------------------ | ------------------ | ---------------------------------------- |
| **Java ME**              | Micro Edition      | Mobile devices, IoT, embedded systems    |
| **Java SE**              | Standard Edition   | Desktop apps, CLI tools, core Java APIs  |
| **Java EE (Jakarta EE)** | Enterprise Edition | Web apps, servers, enterprise-scale apps |

3. JDK vs JRE vs JVM

JVM (Java Virtual Machine): Executes Java bytecode, platform-independent runtime.
JRE (Java Runtime Environment): JVM + standard libraries (only for running apps).
JDK (Java Development Kit): JRE + compiler (javac) + dev tools (needed to code & compile).

4. Installation Steps (Windows)

Download JDK from Oracle
Install (default path: C:\Program Files\Java\jdk-21)
Add jdk-21/bin to PATH (if not set automatically)
Verify in terminal:
java -version
javac -version

5. IDE Setup (VS Code)

Install VS Code Extension Pack for Java
Open project folder → VS Code will auto-detect JDK
Run Main.java directly from editor
Design Patterns → Singleton (AppConfig), Builder (CourseBuilder)
Exception Handling → Checked, Unchecked, and Custom Exceptions

📋 Mapping: Requirement → File/Class

Encapsulation → Student.java (private fields + getters/setters)
Abstraction → Person.java (abstract class)
Polymorphism → printProfile() in Student & Instructor
Inheritance → Student and Instructor extend Person
Nested Classes → can be added in Course.java or TranscriptService
Interfaces → StudentService, CourseService, etc.
Lambdas/Streams → Comparators.java, filtering courses
Anonymous Inner Class → CLI input listeners (if extended)
Enums → Grade.java, Semester.java
Singleton → AppConfig.java
Builder Pattern → CourseBuilder.java
Custom Exceptions → (e.g. DuplicateEnrollmentException)
Recursion → RecursionUtils.getFolderSize()
NIO.2 File I/O → BackupService.java


📸 Screenshots to Include

java -version output
VS Code project structure (src/edu/ccrm/...)
Running CLI menu (adding student & listing)
Backup folder created by BackupService
Sample transcript / GPA calculation

✅ Deliverables Checklist

Source code (src/)
README.md (this file)
Screenshots folder
Sample data/ folder (CSV files)
GitHub repo link

Author: Naina Yadav
Course: Programming in Java
Year: 2025
