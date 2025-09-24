# Java-Project-Anmol
# Campus Course & Records Manager (CCRM)

## Project Overview
This is my Java SE console project named **Campus Course & Records Manager (CCRM)**.  
It is a menu-driven program where an institute can manage:
- Students (add, update, list, enroll, transcripts)
- Courses (create, update, assign instructors, search/filter)
- Enrollment & Grades (record marks, calculate GPA, print transcript)
- File utilities (import/export CSV, create backup folders, recursive folder size)

I tried to cover all important concepts from the syllabus like OOP, Exception Handling, Streams, NIO.2, Date/Time API, Singleton and Builder patterns etc. The project is written completely in Java without any external frameworks.

---

## How to Run
### Requirements
- JDK 17 (or higher) installed
- Any IDE (I used Eclipse), or you can run from terminal
- Git (if you want to clone repo)

### Steps (Eclipse)
1. Open Eclipse → **File → Import → Existing Project**  
2. Browse this repo folder and finish  
3. Right click `MainApp` (inside `edu.ccrm.cli`) → Run As → Java Application  

### Steps (Terminal)
```bash
# Compile
find src -name "*.java" > sources.txt
javac -d bin @sources.txt

# Run (main class may vary, in my case:)
java -cp bin edu.ccrm.cli.MainApp


Demo Workflow

When you run the project, you will see a text menu.
Suggested flow to test:

Add a new Student

Add a Course

Enroll student into the course

Record grades and generate transcript

Export data into exports/ folder

Run Backup option → creates new timestamped folder in backups/

Use recursive utility to check backup folder size

Screenshots of all these steps are kept in /screenshots

JDK vs JRE vs JVM

JDK = compiler + dev tools + JRE

JRE = libraries + JVM (to run Java)

JVM = runs bytecode, platform independent

src/edu/ccrm
 ├─ cli/        → menu, input loop
 ├─ domain/     → Student, Instructor, Course, Enrollment, enums
 ├─ service/    → StudentService, CourseService, EnrollmentService
 ├─ io/         → Import/Export, Backup
 ├─ util/       → helpers, comparators, recursion utils
 └─ config/     → AppConfig (singleton), builders

test-data/      → sample CSVs
screenshots/    → all project screenshots
