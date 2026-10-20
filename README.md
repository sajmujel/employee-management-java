Employee Management System (Java)

A console application in Java for managing employees of two groups – data analysts and security specialists – and the collaboration between them. School project for the course PC2T (Programming and Computer Science Techniques) at BUT Brno.

Features
Add and remove employees (data analyst / security specialist)
Record collaboration between two employees with a level: good, average, bad
Look up an employee by ID, including collaboration counts per level
Use each employee's special skill (different for each group):
Data analyst – finds the colleague with whom they share the most common collaborators
Security specialist – calculates a risk score based on collaboration levels
Sorted listing by group and surname, statistics and per-group counts
Save to / load from a text file, and automatic persistence in a SQLite database
What I practised
Object-oriented design: abstract class Zamestnanec with two subclasses, enums
Polymorphism (each subclass implements its own skill)
Collections (HashMap, lists, sorting with comparators)
File I/O and database access through JDBC
Input validation
Project structure
pc2t projekt/src/
├── Main.java                      # program loop and menu
├── Menu.java                      # user input and output
├── Databaza.java                  # data storage, statistics, file + SQLite I/O
├── Zamestnanec.java               # abstract base class
├── DataAnalitik.java              # data analyst
├── BezpecnostnySpecialista.java   # security specialist
├── TypSkupiny.java                # enum of groups
└── UrovenSpoluprace.java          # enum of collaboration levels
Build and run

Requires JDK 17+ (or any version supporting switch expressions) and the SQLite JDBC driver on the classpath. Easiest way: import the project into Eclipse, add the driver .jar to the build path and run Main.

Note: identifiers and the console UI are in Slovak (school assignment).

Author

Samuel Bachratý – first-year Information Security student at BUT Brno (FEKT).
