School Attendance System
This is a 10-part code-along project to build a console-based school attendance system in Java.

## Session 1: Introduction and Orientation
- Verified Java and Git setup.
- Initialized Git repository for the project.
- Created basic project structure with Main.java.
- Compiled and ran the initial "Welcome" program.
- Pushed initial setup to a part-01 branch on GitHub and created a PR.

### How to Run
1. Navigate to the project root directory (AttendanceSystem).
2. Compile: javac src/com/school/Main.java
3. Run: java -cp src com.school.Main



## Part 9: SOLID Service Layer: RegistrationService & AttendanceService Separation
- Applied the Single Responsibility Principle (SRP) by creating dedicated service classes.
- Created `RegistrationService.java` to handle the registration, management (lists, lookups), and saving of `Student`, `Teacher`, `Staff`, and `Course` entities.
- Modified `Teacher.java` and `Staff.java` to implement `Storable` for file persistence.
- Refactored `AttendanceService.java`:
    - It now depends on `RegistrationService` for looking up students/courses by ID.
    - Removed internal lookup helper methods, delegating this to `RegistrationService`.
    - Its primary focus is now solely on managing attendance records.
- Updated `Main.java` to act as an orchestrator, instantiating and using these services. Direct entity list management was removed from `Main`.
- Demonstrated improved code organization and clearer separation of concerns.

### How to Run
1. Navigate to the project root directory.
2. Compile: `javac src/com/school/*.java`
3. Run: `java -cp src com.school.Main`
4. Check for `students.txt`, `teachers.txt`, `staff.txt`, `courses.txt`, and `attendance_log.txt`.
